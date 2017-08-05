# iOSInterviewQuestions（面试题学习交流群：515295083）

IOSInterviewQuestions (interview questions exchange group: 515295083)



IOS Review Questions (with answers)

First: "hiring a fly iOS" - refer to the answer (on)

Part II: "Recruiting a Kaopu iOS" - Reference answer (below)

Interview questions are the source microblogging @ I called the Sunny how this blog: "Recruitment of a fly iOS" , in which a total of 55 questions, in addition to the first question, entitled correction, other 54 are short answer questions.

Bowen gives a high quality face questions, but no answers, I tried to summarize the next answer, two points made: This is Part I , which is next . Please keep an eye on microblogging .

enter image description here
July 4, 2015
Nearly a year after another interview a lot of people, from the interviewer to the interviewer changes I have iOS recruitment have more feelings. After some time ago a big wave of interviews, we finally found a like-minded little partner, the interview also temporarily come to an end. Summary of the following test the feelings of the process, you can also read our resume, algorithm, character, iOS foundation, the underlying knowledge of the views and some frequently asked questions.

A reliable resume

Resume can reflect a person's character and level, compared to how many awards you get in school, work experience, project experience, familiar with the technology is more critical, if there are blog and some Github on the project, But remember to go to the interview before the next, we really will one by one review your open source code. We also like to focus on some of the details, such as resume keywords spelling, seemingly insignificant but it is able to reflect on their own requirements, often see a resume iOS three letters spelling appeared IOS, iOS, ios three kinds Of the very can not bear, and then list a few common problems:

IPhone -> IPHONE iphone 
Xcode -> XCode xcode 
Objective-C -> Object-C 
JSON -> Json 
HTTP -> Http

Also, pay attention to the Chinese and English with a half-size space separated, layout will be pretty many, resume is not only content, as well as details and attitudes, these points are often reflected in the interviewer's code style, serious work. Of course, the resume is very beautiful to write, but after the chat found that there will be nothing, and even come to interview up with me that the resume is false, would like to ask for an interview this opportunity -

Interview

Do not be late, do not be late, do not be late, the important thing to say three times. There is a change in advance notice HR, encountered a temporary something did not come, and who do not say anything, call the past also asked to change the time, this direct worship. 
When the interview is best to prepare paper, pen, resume, may not be used, but it can reflect the degree of seriousness. Conditional with Mac and source code, the phone installed in all the appearances in the resume App.

About the algorithm

We are pragmatism, iOS development rarely need to write their own complex algorithm, so not in the interview assessment standards.

Code specification

This is a key study items, once in the microblogging made a style error correction:



Also in the interview when people turn over the spot, a lot of groove, to have more than 10 to modify the basic standards (Virgo in this performance are very good

A great distinction between the interview questions

Look at an interviewer based on Zeyang, basically asked a @property enough:

What are the modifiers behind @property?
What is the use of weak keywords, compared to assign what is the difference?
How to use the copy keyword?
What is the problem with this writing: @property (copy) NSMutableArray *array;
How to make your class with copy modifier? How to rewrite the setter with the copy keyword?
This set of problems is relatively large, if the above questions can be answered correctly, you can extend to ask more in-depth points:

What is the essence of @property? Ivar, getter, setter is generated and added to this class
@protocol and category how to use @property
How does the runtime implement the weak attribute
Everyone is good at the field is not the same, we usually from the resume to find their own good skills to talk, if they are not very familiar, it is best not to write out or pull out, if the interviewer is very proficient in the exposed here.

Checklist

Summed up a number of questions, did not stick to it, then these when the checklist, when the interview is really no time to talk when a reminder, language, framework, the nature of the operating mechanism:

[※] What attribute keywords are there in @property? 
[※] weak attributes need to set in the dealloc nil? 
[@ ※] @synthesize and @dynamic, respectively, what role? 
[※ ※ ※] ARC, do not explicitly specify any attribute keywords, the default keywords are what? 
[@ ※ ※] with @property statement NSString(or NSArray, NSDictionary) often use copykeywords, why? strongWhat can I do if I switch to keywords? 
[※ ※ ※] @synthesize What is the rule of the synthetic instance variable? If the property name foo, there is a variable named _foo variable, then it will automatically synthesize new variables? 
[※※※※※] With the automatic synthesis of the property after the instance variables, @ synthesize what use the scene?

[※ ※] objc to send a message to a nil object will happen? 
[※ ※ ※] objc to an object to send messages [obj foo]and objc_msgSend()functions between what is the relationship? 
[※ ※ ※] When will the reported unrecognized selectorabnormal? 
[※ ※ ※ ※ an objc object how to carry out memory layout? (Consider the case of the parent class) 
[※ ※ ※ ※ An objc object isapointer to what? what's the effect? 
[※ ※ ※ ※] The following code output what?

@implementation  Son : Father
 - ( ID ) the init
{ Self = [ Super the init]; IF ( Self ) { NSLog ( @ "% @" , NSStringFromClass ([ Self class])); NSLog ( @ "% @" , NSStringFromClass ( [ Super class]));    } return self ;} @end
    
    
        
        

     


[※※※※] runtime How to find the corresponding IMP address through the selector? (Respectively, consider the method and instance method) 
[※ ※ ※ ※] use the runtime Associatemethod associated with the object, the need to release the main object dealloc? 
[※ ※ ※ ※ ※ objc in the class method and instance method What is the essential difference and contact? 
[※※※※※] _objc_msgForwardfunction is what to do, call it directly what will happen? 
[※※※※※] runtime how to achieve weak variables automatically set nil? 
[※※※※※] Can be added to the class after adding examples of variables? Can I add instance variables to classes created at run time? why?

[※ ※ ※ Runloop and thread what is the relationship? 
[※ ※ ※] What is the role of runloop mode? 
[※ ※ ※ ※] in + scheduledTimerWithTimeInterval...the way to trigger the timer, slide the list on the page, the timer will tentative callback, why? How to solve? 
[※ ※ ※ ※ ※] guess runloop internal is how to achieve?

[*] What mechanism does objc use to manage object memory? 
How does the ARC help developers manage memory? 
[※ ※ ※ Do not manually specify autoreleasepool under the premise of an autorealese object at what time to release? (Such as in a vc viewDidLoad created) 
[※ ※ ※ ※ BAD_ACCESS under what circumstances? 
[※ ※ ※ ※ ※ how to achieve autoreleasepool?

[※ ※] What happens when the use of block reference cycle, how to solve? 
[※ ※] How to amend the block outside the block external variables? 
[※ ※ ※] use some of the system block api (such as UIViewthe block version of the write animation), whether also consider the reference cycle?

[※ ※] GCD's queue (dispatch_queue_t) points which two types? 
[※ ※ ※ ※ How to use GCD synchronization several asynchronous call? (Such as according to a number of url asynchronously loading multiple pictures, and then after the completion of the download to complete a whole picture) 
[※ ※ ※ ※ dispatch_barrier_async what is the role? 
[※※※※※] Why should the apple dispatch_get_current_queue? 
[※ ※ ※ ※ ※ The following code to run the results of how?

- ( void ) the viewDidLoad 
{ 
    [ Super the viewDidLoad]; NSLog ( @ ". 1" ); dispatch_sync (dispatch_get_main_queue (), {^ NSLog ( @ "2" );     }); NSLog ( @ ". 3" ); }
    
    
        

    

[※ ※] addObserver:forKeyPath:options:context:What is the role of each parameter, observer need to achieve which method to get KVO callback? 
[※ ※ ※ How to manually trigger a value of KVO 
[※ ※ ※] If a class has a case variable NSString *_foo, call setValue:forKey:, fooor _fooas a key? 
[※ ※ ※ ※ KVC keyPathin the set of operators how to use? 
[※ ※ ※ ※ KVC and KVO keyPathmust be a property? 
[※※※※※] How to turn off the default KVO default implementation and enter the custom KVO implementation? 
[※※※※※] apple in what way to achieve an object of KVO?

[※ ※] IBOutlet even out of the view why the property can be set to weak? [※ ※ ※ ※ ※ how to use 
IB User Defined Runtime Attributes?

[※ ※ ※ how to debug BAD_ACCESS error 
[※ ※ ※ lldb (gdb) commonly used debugging orders?

These small questions can be used as the entrance to the discussion, according to the interviewer's answer and then continue to talk. Some of the questions compared to the bottom, is left to Cock Cocker's interviewer or test rating with the general situation is not the focus of the study.

Operational capacity

After all, the usual job content is not runtime, runloop, not how to use the bottom of the black magic, 80% of the time and build pages, write business logic, network requests to deal with. 
Ask the interviewer to be able to skillfully build UI, I will find a interviewer made a page so that he analyzed the next page structure, constraints or frame layout of the law and calculation methods; sometimes let the interviewer talk about UITableView commonly used several delegate And the data source proxy method, the dynamic Cell height calculation of what; Next, in the phone casually find an App page, so that the interviewer on the spot if he should write what UI components and layout methods. Ask a few questions will be able to understand the business ability, and we hereby use IB and AutoLayout, if the interviewer still use the code code UI also to the ok, "good" will be good ~

Program architecture and some design patterns If the interviewer himself is not good, then will talk, but kneeling do not say Singleton, and the more the level of the more skeptical. I am generally asked about the design pattern of self-confidence, abstract factory pattern in the Cocoa SDK which class reflected? 
MVC MV MV or MVP or the MVP is to be able to talk about their views, anyway, there is no correct answer, as long as do not engage in too outrageous on the line, such as some people say that the network request and the best operation of the database into UIView Subclasses inside dry.

Network requests, databases and other countries have a mature package, basically know ye use on the line. In addition, we will ask the next step in addition to iOS development, but also what other programming languages, or familiar with what kind of scripting language and Terminal operation, and even ask how to over the wall - believe that these skills are Is very important.

character

We are writing procedures, nothing to use strange, difficult problem difficult for each other, more critical or character, and Team's style is not and to come. A good attitude of the interviewer need to have a normal heart, not Jiaojiao do not kneel licking, the expression to be normal, often asked to ask a question after a minute or two has been in a state of contemplation, do not say a word, It is very Biequ; there is a very Cock, obviously do not understand is still forced to argue, the town of the interviewer worth mentioning, hit the muzzle on the blame it. Decided to either a person basically talk about 5 minutes to be sure, like the feeling of water into the can see the block can not stop.

Recruitment come to an end, there will be more exciting things happen later. Finally, thank you again for your support and trust in me.


["Recruiting a Kaopu iOS"] (http://blog.sunnyxx.com/2015/07/04/ios-interview/) - Reference answer (on)


(Http://weibo.com/u/1364395395) of this blog: ["recruit a Kaopu iOS"] (http: //), the interview source is [microblogging @ I called Sunny how] Blog.sunnyxx.com/2015/07/04/ios-interview/), of which a total of 55 questions, in addition to the first title for the error correction, the other 54 are simple answer.


Sunny (sunnyxx), currently working in Baidu, responsible for Baidu know iOS client development work, the technology like to ask the root and sum up the best practice, love to share and open source, to maintain an open source group called forkingdog.

The answer is [microblogging @ iOS program 犭 Yuan] (http://weibo.com/luohanchenyilong/) finishing, without the subject of proofreading, if flawed, please [microblogging @ iOS program 犭 Yuan] (http: //weibo.com/luohanchenyilong/) corrections.

----------

# Index

 1. [style error correction] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS" interview questions reference Answer (on) .md # 1-style error correction questions)

  1. [Optimization section] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS" interview questions Answer ( On) .md # optimization section)
  2. [Mysterious part] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS" interview questions Answer answer (On) .md # Mishap)
 2. [What is the use of weak keywords, compared to assign what is the difference? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 2 - what is the use of -weak-keyword compared to -assign- what is the difference)
 3. [How to use the copy keyword? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # How to use -copy-keywords)
 4. [This writing will be what the problem: @property (copy) NSMutableArray * array;] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruit a Kaopu iOS" interview questions / "Recruiting a Kaopu iOS" interview questions reference answer (on) .md # 4- this writing will be what the problem -property-copy-nsmutablearray-array)
 5. [How to make your own class with copy modifier? How to rewrite the setter with the copy keyword? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 5 - how to make their own class with -copy-modifier how to rewrite the -copy-keyword -setter)
 6. What is the essence of @property? Ivar, getter, setter is how to generate and add to this class] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview question Answer / "Recruitment of a (On) .md # 6-property- What is the nature of ivargettersetter-how to generate and add to this class)
 7. [@protocol and category how to use @property] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu IOS "interview questions reference answer (on) .md # 7-protocol- and -category- how to use -property)
 8. [runtime how to achieve weak attributes] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS" interview questions Reference answer (on) .md # 8-runtime- how to achieve -weak-attribute)
 9. What are the attribute keywords in [@property? / @property behind which can be modified? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 9-property in which the property keyword -property-what can be followed by the modifier)
 10. [weak attributes need to set in the dealloc nil? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 10-weak attributes need to set in the dealloc nil Mody)
 11. [@synthesize and @dynamic, respectively, what role? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 11-synthesize and dynamic, respectively, what role)
 12. [ARC, do not explicitly specify any attribute keywords, the default keywords are what? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 12-arc does not explicitly specify any attribute keywords when the default keywords are what)
 13. [Using Nostring (or NSArray, NSDictionary) declared with @property often use the copy keyword, why? What can I do if I use the strong keyword instead? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 13 - with the property declared nsstring or nsarraynsdictionary often use the copy keyword why if the use of strong keywords may cause any problems)
  1. [copy operation for non-collection class objects] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS "Answer questions (on) .md # 1 on the non-collection class object copy operation)
  2. [Collection class object copy and mutableCopy] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS" Interview questions reference answer (on) .md # 2 collection class object copy and mutablecopy)
 14. [@synthesize What is the rule for synthesizing instance variables? If the property name foo, there is a variable named _foo variable, then it will automatically synthesize new variables? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 14-synthesize the rules of the case of synthetic variables What if the property name foo there is a variable named _foo then it will automatically synthesize the new variables Mody)
 15. [With the automatic synthesis of attribute instance variables, @ synthesize what are the use of the scene? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 15- synthesize what happens when you have the autoincrement attribute instance variable)
 16. [objc send a message to an nil object what will happen? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 16-objc to send messages to an nil object what will happen)
 17. What is the relationship between objc sending an message [obj foo] to an object and the objc_msgSend () function? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 17-objc What is the relationship between the obj-foo and objc_msgsend functions that send a message to an object)
 18. [When will the unrecognized selector be reported? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 18 - when will the reported unrecognized-selector the exception)
 19. [An objc object how to carry out memory layout? (Consider the case of a parent class)] (https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" interview questions Answer / "Recruiting a Kaopu iOS" Reference to the above (.) .md # 19 - an objc object how to carry out memory layout Consider the case of a parent class)
 20. [What does an objc object's isa pointer point to? what's the effect? ] (Https://github.com/ChenYilong/iOSInterviewQuestions/blob/master/01 "Recruiting a Kaopu iOS" Interview Questions Answer / "Recruiting a Kaopu iOS" Interview Questions Answer (on) .md # 20 - an objc object isa pointer to what is the role)
 21. [What is the following code output? ] (Https://github.com/ChenY
