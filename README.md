# BNM Bench
 In this benchmark, all of the llms got the same prompt + all the BNM docs over at https://bynamemodding.github.io.

 Most benchmarks have a "score" system, but I am not sure how I would do that automatically, so I made a ranking from 1-7 of how well they did.
 
 Here is the ranking of how accurately it got the code.
 1. Kimi K2 Thinking: Kimi K2 not only did the task at hand with little to no errors, but even gave the full code that used JNI OnLoad.
    
 2. Gemini 3 Pro Preview: Gemini 3 Pro did the task exactly how it was asked, and even showed how you can use Utils.hpp to modify a Mono::String's value with CreateMonoString.
    
 3. MiniMax M2: M2 did the task at hand very well, and correctly called the nameField to get the value whilst still putting the instance.
    
 4. Claude Opus 4.5: Opus 4.5 did the task very well and included everything perfectly, however it failed to call the playerNameField to get the value and instead only put in the instance.
    
 5. GPT 5.1 Codex Max: 5.1 Codex Max did nearly the same as Opus 4.5 with the same misinput of not calling the field for its value, however it sent the code in steps and it was much more simple. It did however show how you would use Image for loading a class that is in a different assembly.
    
 6. DeepSeek v3.2: DeepSeek did most of it correctly, and even included the image, however incorrectly used CreateNewInstance for the player instance (instead of using a current instance) and also did not call the field for its value (it did when not putting in an instance for a static field though).
     
 7. Nova 2 Lite v1 (free): Nova did a bit of it correctly, and even called the field for its value, but it thought BNM_OBFUSCATE_TEMP was for the game's obfuscate instead of it being for obfuscating your own code. It also used auto for the field and did the generics with GetField which is incorrect.

The current benchmark source repo is private, but you can see the results folder here.
