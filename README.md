# BNM Bench
 In this benchmark, all of the llms got the same prompt + all the BNM docs over at https://bynamemodding.github.io.

 Most benchmarks have a "score" system, but I am not sure how I would do that automatically, so I made a ranking from 1-10 of how well they did.
 
 Here is the ranking of how accurately it got the code.
 1. Kimi K2 Thinking: Kimi K2 not only did the task at hand with little to no errors, but even gave the full code that used JNI OnLoad.
    
 2. Claude Opus 4.5 (high): Opus 4.5 (high) did the task very well and included everything. It used static types and generics for the classes and fields, correctly called the field for its value, and showed correct alternative syntax. It did exactly what was asked.   

 3. Gemini 3 Pro Preview: Gemini 3 Pro did the task exactly how it was asked, and even showed how you can modify a Mono::String's value with CreateMonoString. It was structured very nice and also showed examples for properties (for when it's NOT a field). 

 4. Grok 4.1 Fast: 4.1 Fast also did the task very well, although it did overload with comments. It correctly included files for everything including logging, and showed examples for logging, setting to an std::string, and setting the value of the field with CreateMonoString. It showed a lot more examples too like using GetComponent for player instance.
 
 5. MiniMax M2: M2 did the task at hand very well, and correctly called the nameField to get the value whilst still putting the instance. It also added examples for static fields and with better static typing.
    
 6. Claude Opus 4.5: Opus 4.5 did the task very well and included everything perfectly, however it failed to call the playerNameField to get the value and instead only put in the instance.
 
 7. Claude Sonnet AND Haiku 4.5 (both results were basically the same): Sonnet AND Haiku 4.5 did the task very well and structured the code nicely, however it also failed to call the field for its value. However, it did provide other methods which use .SetInstance and then called the field for its value which does work. It provided method(s) for getting and setting the fields value. Similar quality to Opus 4.5 but Opus had better structuring.
    
 8. GPT 5.1 Codex Max: 5.1 Codex Max did nearly the same as Opus and Sonnet 4.5 with the same misinput of not calling the field for its value, however it sent the code in steps and it was much more simple. It did however show how you would use Image for loading a class that is in a different assembly.
    
 9. DeepSeek v3.2: DeepSeek did most of it correctly, and even included the image, however incorrectly used CreateNewInstance for the player instance (instead of using a current instance) and also did not call the field for its value (it did when not putting in an instance for a static field though).
     
 10. Nova 2 Lite v1 (free): Nova did a bit of it correctly, and even called the field for its value, but it thought BNM_OBFUSCATE_TEMP was for the game's obfuscate instead of it being for obfuscating your own code. It also used auto for the field and did the generics with GetField which is incorrect.

The current benchmark source repo is private, but you can see the results folder here.
