# naoCustom

## How to use

Just add a new Json object to the Json array.
For example: 

```javascript
 {
    "words": ["behavior"],
    "proxy": "ALBehaviorManager",
    "method": "runBehavior",
    "args": ["animations/Sit/Waiting/Music_HighwayToHell_1"]
  }
```

Parameter:
- **words**: array of strings, is a collection of hot phrases. so if the ASR recognizes one of this phrases the assistant will trigger the custom action. The string must be exactly the recognized text from the ASR. (only upper and lower case and "." are ignored). The string must be in lower case! If multiple custom actions have the same hot phrase only the first action will be triggered. If an ASR result is matched with a hot phrase it will not send to the OTTO backend!
- **proxy**: string, is the name of the module. see http://doc.aldebaran.com/2-8/naoqi/index.html for example "ALBehaviorManager" btw. the name will never ends with the suffix "Proxy"! For example: "ALBehaviorManagerProxy" -> "ALBehaviorManager"
- **method**: string, is the name of the modul method. for example "runBehavior" see http://doc.aldebaran.com/2-8/naoqi/core/albehaviormanager-api.html#ALBehaviorManagerProxy::runBehavior__ssCR. (Yes the modul name in the API is "ALBehaviorManagerProxy" but it is really "ALBehaviorManager"!
- **args**: array of objecs. this array contains all arguments for the method. The order of args must be the same as described in the API! 
  - **string**: `"foobar"`
  - **float** / **double**: `42.42`
  - **int**: `42`
  - **object**: `{"property": <<value>>}`
  - **array** / **list**: `[<<value>>, <<value>>, ...]`
  
## current behaviors

* aldebaran_auto_diagnostic-fe5347
* animationMode
* animations/LED/CircleEyes
* animations/Sit/BodyTalk/Listening/Listening_1
* animations/Sit/BodyTalk/Listening/Listening_2
* animations/Sit/BodyTalk/Listening/Listening_3
* animations/Sit/BodyTalk/Listening/Listening_4
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_1
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_10
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_11
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_12
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_2
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_3
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_4
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_5
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_6
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_7
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_8
* animations/Sit/BodyTalk/BodyLanguage/BodyTalk_9
* animations/Sit/BodyTalk/Speaking/BodyTalk_1
* animations/Sit/BodyTalk/Speaking/BodyTalk_10
* animations/Sit/BodyTalk/Speaking/BodyTalk_11
* animations/Sit/BodyTalk/Speaking/BodyTalk_12
* animations/Sit/BodyTalk/Speaking/BodyTalk_2
* animations/Sit/BodyTalk/Speaking/BodyTalk_3
* animations/Sit/BodyTalk/Speaking/BodyTalk_4
* animations/Sit/BodyTalk/Speaking/BodyTalk_5
* animations/Sit/BodyTalk/Speaking/BodyTalk_6
* animations/Sit/BodyTalk/Speaking/BodyTalk_7
* animations/Sit/BodyTalk/Speaking/BodyTalk_8
* animations/Sit/BodyTalk/Speaking/BodyTalk_9
* animations/Sit/BodyTalk/Thinking/Remember_1
* animations/Sit/BodyTalk/Thinking/Remember_2
* animations/Sit/BodyTalk/Thinking/Remember_3
* animations/Sit/BodyTalk/Thinking/ThinkingLoop_1
* animations/Sit/BodyTalk/Thinking/ThinkingLoop_2
* animations/Sit/Emotions/Negative/Angry_1
* animations/Sit/Emotions/Negative/Fear_1
* animations/Sit/Emotions/Negative/Frustrated_1
* animations/Sit/Emotions/Negative/Hurt_1
* animations/Sit/Emotions/Negative/Late_1
* animations/Sit/Emotions/Negative/Sad_1
* animations/Sit/Emotions/Negative/Surprise_1
* animations/Sit/Emotions/Neutral/AskForAttention_1
* animations/Sit/Emotions/Neutral/AskForAttention_2
* animations/Sit/Emotions/Neutral/AskForAttention_3
* animations/Sit/Emotions/Neutral/Sneeze_1
* animations/Sit/Emotions/Positive/Happy_1
* animations/Sit/Emotions/Positive/Happy_2
* animations/Sit/Emotions/Positive/Happy_3
* animations/Sit/Emotions/Positive/Happy_4
* animations/Sit/Emotions/Positive/Hungry_1
* animations/Sit/Emotions/Positive/Laugh_1
* animations/Sit/Emotions/Positive/Laugh_2
* animations/Sit/Emotions/Positive/Mocker_1
* animations/Sit/Emotions/Positive/Shy_1
* animations/Sit/Emotions/Positive/Winner_1
* animations/Sit/Gestures/ComeOn_1
* animations/Sit/Gestures/Hey_3
* animations/Sit/Gestures/Me_7
* animations/Sit/Gestures/You_4
* animations/Sit/Reactions/BumperLeft_1
* animations/Sit/Reactions/BumperRight_1
* animations/Sit/Reactions/Bumpers_1
* animations/Sit/Reactions/Bumpers_2
* animations/Sit/Reactions/Bumpers_3
* animations/Sit/Reactions/EthernetOff_1
* animations/Sit/Reactions/EthernetOn_1
* animations/Sit/Reactions/Heat_1
* animations/Sit/Reactions/LightShine_1
* animations/Sit/Reactions/LightShine_2
* animations/Sit/Reactions/LightShine_3
* animations/Sit/Reactions/LightShine_4
* animations/Sit/Reactions/SeeColor_1
* animations/Sit/Reactions/SeeColor_2
* animations/Sit/Reactions/SeeColor_3
* animations/Sit/Reactions/ShakeBody_1
* animations/Sit/Reactions/ShakeBody_2
* animations/Sit/Reactions/ShakeBody_3
* animations/Sit/Reactions/TouchHead_1
* animations/Sit/Reactions/TouchHead_2
* animations/Sit/Reactions/TouchHead_3
* animations/Sit/Reactions/TouchHead_4
* animations/Sit/Waiting/AutoFormat_1
* animations/Sit/Waiting/Binoculars_1
* animations/Sit/Waiting/Bored_1
* animations/Sit/Waiting/CallSomeone_1
* animations/Sit/Waiting/CatchFly_1
* animations/Sit/Waiting/Cramp_1
* animations/Sit/Waiting/DriveCar_1
* animations/Sit/Waiting/FalseStop_1
* animations/Sit/Waiting/FalseStop_2
* animations/Sit/Waiting/Fitness_1
* animations/Sit/Waiting/GeoCircle_1
* animations/Sit/Waiting/GeoSquare_1
* animations/Sit/Waiting/GeoTriangle_1
* animations/Sit/Waiting/KnockEye_1
* animations/Sit/Waiting/KnockKnee_1
* animations/Sit/Waiting/KnockKnee_2
* animations/Sit/Waiting/LookHand_1
* animations/Sit/Waiting/LookHand_2
* animations/Sit/Waiting/Music_HighwayToHell_1
* animations/Sit/Waiting/Music_VieEnRose_1
* animations/Sit/Waiting/MysticalPower_1
* animations/Sit/Waiting/Oar_1
* animations/Sit/Waiting/Phone_1
* animations/Sit/Waiting/PlayHands_1
* animations/Sit/Waiting/PlayHands_2
* animations/Sit/Waiting/PlayHands_3
* animations/Sit/Waiting/Pong_1
* animations/Sit/Waiting/PoorlySeated_1
* animations/Sit/Waiting/Puppet_1
* animations/Sit/Waiting/Relaxation_1
* animations/Sit/Waiting/Relaxation_2
* animations/Sit/Waiting/Relaxation_3
* animations/Sit/Waiting/Rest_1
* animations/Sit/Waiting/Robot_1
* animations/Sit/Waiting/ScratchBack_1
* animations/Sit/Waiting/ScratchEye_1
* animations/Sit/Waiting/ScratchHand_1
* animations/Sit/Waiting/ScratchHead_1
* animations/Sit/Waiting/ScratchLeg_1
* animations/Sit/Waiting/ScratchTorso_1
* animations/Sit/Waiting/TakePicture_1
* animations/Sit/Waiting/Think_1
* animations/Sit/Waiting/Think_2
* animations/Sit/Waiting/Think_3
* animations/Sit/Waiting/WakeUp_1
* animations/Sit/Waiting/Yawn_1
* animations/Sit/Waiting/ZenCircles_1
* animations/SitOnPod/BodyTalk/Listening/Listening_1
* animations/SitOnPod/BodyTalk/Listening/Listening_2
* animations/SitOnPod/BodyTalk/Listening/Listening_3
* animations/SitOnPod/BodyTalk/Listening/Listening_4
* animations/SitOnPod/BodyTalk/Listening/Listening_5
* animations/SitOnPod/BodyTalk/Listening/Listening_6
* animations/SitOnPod/BodyTalk/Listening/Listening_7
* animations/SitOnPod/BodyTalk/Listening/Listening_8
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_1
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_10
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_11
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_12
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_2
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_3
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_4
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_5
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_6
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_7
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_8
* animations/SitOnPod/BodyTalk/Speaking/BodyTalk_9
* animations/SitOnPod/BodyTalk/Thinking/Remember_1
* animations/SitOnPod/BodyTalk/Thinking/Remember_2
* animations/SitOnPod/BodyTalk/Thinking/Remember_3
* animations/SitOnPod/BodyTalk/Thinking/ThinkingLoop_1
* animations/SitOnPod/BodyTalk/Thinking/ThinkingLoop_2
* animations/SitOnPod/Emotions/Neutral/Hello_1
* animations/SitOnPod/Gestures/Choice_1
* animations/SitOnPod/Gestures/CountThree_1
* animations/SitOnPod/Gestures/CountThree_2
* animations/SitOnPod/Gestures/CountTwo_1
* animations/SitOnPod/Gestures/CountTwo_2
* animations/SitOnPod/Gestures/Everything_1
* animations/SitOnPod/Gestures/Everything_2
* animations/SitOnPod/Gestures/Everything_3
* animations/SitOnPod/Gestures/Everything_4
* animations/SitOnPod/Gestures/Everything_6
* animations/SitOnPod/Gestures/HeSays_1
* animations/SitOnPod/Gestures/HeSays_2
* animations/SitOnPod/Gestures/HeSays_3
* animations/SitOnPod/Gestures/Hey_1
* animations/SitOnPod/Gestures/Hey_2
* animations/SitOnPod/Gestures/Hey_3
* animations/SitOnPod/Gestures/Hey_4
* animations/SitOnPod/Gestures/Hey_6
* animations/SitOnPod/Gestures/Hey_7
* animations/SitOnPod/Gestures/Me_1
* animations/SitOnPod/Gestures/Me_2
* animations/SitOnPod/Gestures/Me_4
* animations/SitOnPod/Gestures/Me_7
* animations/SitOnPod/Gestures/Me_8
* animations/SitOnPod/Gestures/No_1
* animations/SitOnPod/Gestures/No_2
* animations/SitOnPod/Gestures/No_3
* animations/SitOnPod/Gestures/No_4
* animations/SitOnPod/Gestures/No_5
* animations/SitOnPod/Gestures/No_6
* animations/SitOnPod/Gestures/No_7
* animations/SitOnPod/Gestures/No_8
* animations/SitOnPod/Gestures/No_9
* animations/SitOnPod/Gestures/This_1
* animations/SitOnPod/Gestures/This_10
* animations/SitOnPod/Gestures/This_11
* animations/SitOnPod/Gestures/This_12
* animations/SitOnPod/Gestures/This_13
* animations/SitOnPod/Gestures/This_14
* animations/SitOnPod/Gestures/This_15
* animations/SitOnPod/Gestures/This_2
* animations/SitOnPod/Gestures/This_3
* animations/SitOnPod/Gestures/This_4
* animations/SitOnPod/Gestures/This_5
* animations/SitOnPod/Gestures/This_6
* animations/SitOnPod/Gestures/This_7
* animations/SitOnPod/Gestures/This_8
* animations/SitOnPod/Gestures/This_9
* animations/SitOnPod/Gestures/WhatSThis_1
* animations/SitOnPod/Gestures/WhatSThis_10
* animations/SitOnPod/Gestures/WhatSThis_11
* animations/SitOnPod/Gestures/WhatSThis_12
* animations/SitOnPod/Gestures/WhatSThis_13
* animations/SitOnPod/Gestures/WhatSThis_14
* animations/SitOnPod/Gestures/WhatSThis_15
* animations/SitOnPod/Gestures/WhatSThis_16
* animations/SitOnPod/Gestures/WhatSThis_2
* animations/SitOnPod/Gestures/WhatSThis_3
* animations/SitOnPod/Gestures/WhatSThis_4
* animations/SitOnPod/Gestures/WhatSThis_5
* animations/SitOnPod/Gestures/WhatSThis_6
* animations/SitOnPod/Gestures/WhatSThis_7
* animations/SitOnPod/Gestures/WhatSThis_8
* animations/SitOnPod/Gestures/WhatSThis_9
* animations/SitOnPod/Gestures/Yes_1
* animations/SitOnPod/Gestures/Yes_2
* animations/SitOnPod/Gestures/Yes_3
* animations/SitOnPod/Gestures/You_1
* animations/SitOnPod/Gestures/You_2
* animations/SitOnPod/Gestures/You_3
* animations/SitOnPod/Gestures/You_4
* animations/SitOnPod/Gestures/You_5
* animations/Stand/BodyTalk/Listening/Listening_2
* animations/Stand/BodyTalk/Listening/ListeningLeft_1
* animations/Stand/BodyTalk/Listening/ListeningLeft_3
* animations/Stand/BodyTalk/Listening/ListeningRight_1
* animations/Stand/BodyTalk/Listening/ListeningRight_3
* animations/Stand/BodyTalk/Speaking/BodyTalk_1
* animations/Stand/BodyTalk/Speaking/BodyTalk_10
* animations/Stand/BodyTalk/Speaking/BodyTalk_11
* animations/Stand/BodyTalk/Speaking/BodyTalk_12
* animations/Stand/BodyTalk/Speaking/BodyTalk_13
* animations/Stand/BodyTalk/Speaking/BodyTalk_14
* animations/Stand/BodyTalk/Speaking/BodyTalk_15
* animations/Stand/BodyTalk/Speaking/BodyTalk_16
* animations/Stand/BodyTalk/Speaking/BodyTalk_17
* animations/Stand/BodyTalk/Speaking/BodyTalk_18
* animations/Stand/BodyTalk/Speaking/BodyTalk_19
* animations/Stand/BodyTalk/Speaking/BodyTalk_2
* animations/Stand/BodyTalk/Speaking/BodyTalk_20
* animations/Stand/BodyTalk/Speaking/BodyTalk_21
* animations/Stand/BodyTalk/Speaking/BodyTalk_22
* animations/Stand/BodyTalk/Speaking/BodyTalk_3
* animations/Stand/BodyTalk/Speaking/BodyTalk_4
* animations/Stand/BodyTalk/Speaking/BodyTalk_5
* animations/Stand/BodyTalk/Speaking/BodyTalk_6
* animations/Stand/BodyTalk/Speaking/BodyTalk_7
* animations/Stand/BodyTalk/Speaking/BodyTalk_8
* animations/Stand/BodyTalk/Speaking/BodyTalk_9
* animations/Stand/BodyTalk/Thinking/Remember_1
* animations/Stand/BodyTalk/Thinking/Remember_2
* animations/Stand/BodyTalk/Thinking/Remember_3
* animations/Stand/BodyTalk/Thinking/ThinkingLoop_1
* animations/Stand/BodyTalk/Thinking/ThinkingLoop_2
* animations/Stand/Emotions/Negative/Angry_1
* animations/Stand/Emotions/Negative/Angry_2
* animations/Stand/Emotions/Negative/Angry_3
* animations/Stand/Emotions/Negative/Angry_4
* animations/Stand/Emotions/Negative/Anxious_1
* animations/Stand/Emotions/Negative/Bored_1
* animations/Stand/Emotions/Negative/Bored_2
* animations/Stand/Emotions/Negative/Disappointed_1
* animations/Stand/Emotions/Negative/Exhausted_1
* animations/Stand/Emotions/Negative/Exhausted_2
* animations/Stand/Emotions/Negative/Fear_1
* animations/Stand/Emotions/Negative/Fear_2
* animations/Stand/Emotions/Negative/Fearful_1
* animations/Stand/Emotions/Negative/Frustrated_1
* animations/Stand/Emotions/Negative/Humiliated_1
* animations/Stand/Emotions/Negative/Hurt_1
* animations/Stand/Emotions/Negative/Hurt_2
* animations/Stand/Emotions/Negative/Late_1
* animations/Stand/Emotions/Negative/Sad_1
* animations/Stand/Emotions/Negative/Sad_2
* animations/Stand/Emotions/Negative/Shocked_1
* animations/Stand/Emotions/Negative/Sorry_1
* animations/Stand/Emotions/Negative/Surprise_1
* animations/Stand/Emotions/Negative/Surprise_2
* animations/Stand/Emotions/Negative/Surprise_3
* animations/Stand/Emotions/Neutral/Alienated_1
* animations/Stand/Emotions/Neutral/Annoyed_1
* animations/Stand/Emotions/Neutral/AskForAttention_1
* animations/Stand/Emotions/Neutral/AskForAttention_2
* animations/Stand/Emotions/Neutral/AskForAttention_3
* animations/Stand/Emotions/Neutral/Cautious_1
* animations/Stand/Emotions/Neutral/Confused_1
* animations/Stand/Emotions/Neutral/Determined_1
* animations/Stand/Emotions/Neutral/Embarrassed_1
* animations/Stand/Emotions/Neutral/Hello_1
* animations/Stand/Emotions/Neutral/Hesitation_1
* animations/Stand/Emotions/Neutral/Innocent_1
* animations/Stand/Emotions/Neutral/Lonely_1
* animations/Stand/Emotions/Neutral/Mischievous_1
* animations/Stand/Emotions/Neutral/Puzzled_1
* animations/Stand/Emotions/Neutral/Sneeze
* animations/Stand/Emotions/Neutral/Stubborn_1
* animations/Stand/Emotions/Neutral/Suspicious_1
* animations/Stand/Emotions/Positive/Amused_1
* animations/Stand/Emotions/Positive/Confident_1
* animations/Stand/Emotions/Positive/Ecstatic_1
* animations/Stand/Emotions/Positive/Enthusiastic_1
* animations/Stand/Emotions/Positive/Excited_1
* animations/Stand/Emotions/Positive/Excited_2
* animations/Stand/Emotions/Positive/Excited_3
* animations/Stand/Emotions/Positive/Happy_1
* animations/Stand/Emotions/Positive/Happy_2
* animations/Stand/Emotions/Positive/Happy_3
* animations/Stand/Emotions/Positive/Happy_4
* animations/Stand/Emotions/Positive/Hungry_1
* animations/Stand/Emotions/Positive/Hysterical_1
* animations/Stand/Emotions/Positive/Interested_1
* animations/Stand/Emotions/Positive/Interested_2
* animations/Stand/Emotions/Positive/Laugh_1
* animations/Stand/Emotions/Positive/Laugh_2
* animations/Stand/Emotions/Positive/Laugh_3
* animations/Stand/Emotions/Positive/Mocker_1
* animations/Stand/Emotions/Positive/Optimistic_1
* animations/Stand/Emotions/Positive/Peaceful_1
* animations/Stand/Emotions/Positive/Proud_1
* animations/Stand/Emotions/Positive/Proud_2
* animations/Stand/Emotions/Positive/Proud_3
* animations/Stand/Emotions/Positive/Relieved_1
* animations/Stand/Emotions/Positive/Shy_1
* animations/Stand/Emotions/Positive/Shy_2
* animations/Stand/Emotions/Positive/Sure_1
* animations/Stand/Emotions/Positive/Winner_1
* animations/Stand/Emotions/Positive/Winner_2
* animations/Stand/Gestures/Angry_1
* animations/Stand/Gestures/Angry_2
* animations/Stand/Gestures/Angry_3
* animations/Stand/Gestures/Applause_1
* animations/Stand/Gestures/BowShort_1
* animations/Stand/Gestures/But_1
* animations/Stand/Gestures/CalmDown_1
* animations/Stand/Gestures/CalmDown_2
* animations/Stand/Gestures/CalmDown_3
* animations/Stand/Gestures/CalmDown_4
* animations/Stand/Gestures/CalmDown_5
* animations/Stand/Gestures/CalmDown_6
* animations/Stand/Gestures/Caress_1
* animations/Stand/Gestures/Caress_2
* animations/Stand/Gestures/CatchFly_1
* animations/Stand/Gestures/CatchFly_2
* animations/Stand/Gestures/Choice_1
* animations/Stand/Gestures/Choice_2
* animations/Stand/Gestures/Claw_1
* animations/Stand/Gestures/Claw_2
* animations/Stand/Gestures/Coaxing_1
* animations/Stand/Gestures/Coaxing_2
* animations/Stand/Gestures/ComeOn_1
* animations/Stand/Gestures/Confused_1
* animations/Stand/Gestures/Confused_2
* animations/Stand/Gestures/CountFive_1
* animations/Stand/Gestures/CountFive_2
* animations/Stand/Gestures/CountFour_1
* animations/Stand/Gestures/CountFour_2
* animations/Stand/Gestures/CountMore_1
* animations/Stand/Gestures/CountMore_2
* animations/Stand/Gestures/CountOne_1
* animations/Stand/Gestures/CountOne_2
* animations/Stand/Gestures/CountThree_1
* animations/Stand/Gestures/CountThree_2
* animations/Stand/Gestures/CountTwo_1
* animations/Stand/Gestures/CountTwo_2
* animations/Stand/Gestures/Desperate_1
* animations/Stand/Gestures/Desperate_2
* animations/Stand/Gestures/Desperate_3
* animations/Stand/Gestures/Desperate_4
* animations/Stand/Gestures/Desperate_5
* animations/Stand/Gestures/Enthusiastic_1
* animations/Stand/Gestures/Enthusiastic_2
* animations/Stand/Gestures/Enthusiastic_3
* animations/Stand/Gestures/Enthusiastic_4
* animations/Stand/Gestures/Enthusiastic_5
* animations/Stand/Gestures/Everything_1
* animations/Stand/Gestures/Everything_2
* animations/Stand/Gestures/Everything_3
* animations/Stand/Gestures/Everything_4
* animations/Stand/Gestures/Everything_5
* animations/Stand/Gestures/Everything_6
* animations/Stand/Gestures/Excited_1
* animations/Stand/Gestures/Explain_1
* animations/Stand/Gestures/Explain_10
* animations/Stand/Gestures/Explain_11
* animations/Stand/Gestures/Explain_2
* animations/Stand/Gestures/Explain_3
* animations/Stand/Gestures/Explain_4
* animations/Stand/Gestures/Explain_5
* animations/Stand/Gestures/Explain_6
* animations/Stand/Gestures/Explain_7
* animations/Stand/Gestures/Explain_8
* animations/Stand/Gestures/Explain_9
* animations/Stand/Gestures/Far_1
* animations/Stand/Gestures/Far_2
* animations/Stand/Gestures/Far_3
* animations/Stand/Gestures/Follow_1
* animations/Stand/Gestures/Freeze_1
* animations/Stand/Gestures/Give_1
* animations/Stand/Gestures/Give_2
* animations/Stand/Gestures/Give_3
* animations/Stand/Gestures/Give_4
* animations/Stand/Gestures/Give_5
* animations/Stand/Gestures/Give_6
* animations/Stand/Gestures/Great_1
* animations/Stand/Gestures/HeSays_1
* animations/Stand/Gestures/HeSays_2
* animations/Stand/Gestures/HeSays_3
* animations/Stand/Gestures/Hey_1
* animations/Stand/Gestures/Hey_2
* animations/Stand/Gestures/Hey_3
* animations/Stand/Gestures/Hey_4
* animations/Stand/Gestures/Hey_5
* animations/Stand/Gestures/Hey_6
* animations/Stand/Gestures/Hey_7
* animations/Stand/Gestures/Hide_1
* animations/Stand/Gestures/Hungry_1
* animations/Stand/Gestures/IDontKnow_1
* animations/Stand/Gestures/IDontKnow_2
* animations/Stand/Gestures/IDontKnow_3
* animations/Stand/Gestures/IDontKnow_4
* animations/Stand/Gestures/IDontKnow_5
* animations/Stand/Gestures/IDontKnow_6
* animations/Stand/Gestures/JointHands_1
* animations/Stand/Gestures/JointHands_2
* animations/Stand/Gestures/JointHands_3
* animations/Stand/Gestures/Joy_1
* animations/Stand/Gestures/Kisses_1
* animations/Stand/Gestures/Look_1
* animations/Stand/Gestures/Look_2
* animations/Stand/Gestures/Maybe_1
* animations/Stand/Gestures/Me_1
* animations/Stand/Gestures/Me_2
* animations/Stand/Gestures/Me_3
* animations/Stand/Gestures/Me_4
* animations/Stand/Gestures/Me_5
* animations/Stand/Gestures/Me_6
* animations/Stand/Gestures/Me_7
* animations/Stand/Gestures/Me_8
* animations/Stand/Gestures/Mime_1
* animations/Stand/Gestures/Mime_2
* animations/Stand/Gestures/Next_1
* animations/Stand/Gestures/No_1
* animations/Stand/Gestures/No_2
* animations/Stand/Gestures/No_3
* animations/Stand/Gestures/No_4
* animations/Stand/Gestures/No_5
* animations/Stand/Gestures/No_6
* animations/Stand/Gestures/No_7
* animations/Stand/Gestures/No_8
* animations/Stand/Gestures/No_9
* animations/Stand/Gestures/Nothing_1
* animations/Stand/Gestures/Nothing_2
* animations/Stand/Gestures/OnTheEvening_1
* animations/Stand/Gestures/OnTheEvening_2
* animations/Stand/Gestures/OnTheEvening_3
* animations/Stand/Gestures/OnTheEvening_4
* animations/Stand/Gestures/OnTheEvening_5
* animations/Stand/Gestures/Please_1
* animations/Stand/Gestures/Please_2
* animations/Stand/Gestures/Please_3
* animations/Stand/Gestures/Reject_1
* animations/Stand/Gestures/Reject_2
* animations/Stand/Gestures/Reject_3
* animations/Stand/Gestures/Reject_4
* animations/Stand/Gestures/Reject_5
* animations/Stand/Gestures/Reject_6
* animations/Stand/Gestures/Salute_1
* animations/Stand/Gestures/Salute_2
* animations/Stand/Gestures/Salute_3
* animations/Stand/Gestures/Shoot_1
* animations/Stand/Gestures/ShowFloor_1
* animations/Stand/Gestures/ShowFloor_2
* animations/Stand/Gestures/ShowFloor_3
* animations/Stand/Gestures/ShowFloor_4
* animations/Stand/Gestures/ShowFloor_5
* animations/Stand/Gestures/ShowSky_1
* animations/Stand/Gestures/ShowSky_10
* animations/Stand/Gestures/ShowSky_11
* animations/Stand/Gestures/ShowSky_12
* animations/Stand/Gestures/ShowSky_2
* animations/Stand/Gestures/ShowSky_3
* animations/Stand/Gestures/ShowSky_4
* animations/Stand/Gestures/ShowSky_5
* animations/Stand/Gestures/ShowSky_6
* animations/Stand/Gestures/ShowSky_7
* animations/Stand/Gestures/ShowSky_8
* animations/Stand/Gestures/ShowSky_9
* animations/Stand/Gestures/Shy_1
* animations/Stand/Gestures/Stretch_1
* animations/Stand/Gestures/Stretch_2
* animations/Stand/Gestures/Surprised_1
* animations/Stand/Gestures/Take_1
* animations/Stand/Gestures/Thinking_1
* animations/Stand/Gestures/Thinking_2
* animations/Stand/Gestures/Thinking_3
* animations/Stand/Gestures/Thinking_4
* animations/Stand/Gestures/Thinking_5
* animations/Stand/Gestures/Thinking_6
* animations/Stand/Gestures/Thinking_7
* animations/Stand/Gestures/Thinking_8
* animations/Stand/Gestures/This_1
* animations/Stand/Gestures/This_10
* animations/Stand/Gestures/This_11
* animations/Stand/Gestures/This_12
* animations/Stand/Gestures/This_13
* animations/Stand/Gestures/This_14
* animations/Stand/Gestures/This_15
* animations/Stand/Gestures/This_2
* animations/Stand/Gestures/This_3
* animations/Stand/Gestures/This_4
* animations/Stand/Gestures/This_5
* animations/Stand/Gestures/This_6
* animations/Stand/Gestures/This_7
* animations/Stand/Gestures/This_8
* animations/Stand/Gestures/This_9
* animations/Stand/Gestures/WhatSThis_1
* animations/Stand/Gestures/WhatSThis_10
* animations/Stand/Gestures/WhatSThis_11
* animations/Stand/Gestures/WhatSThis_12
* animations/Stand/Gestures/WhatSThis_13
* animations/Stand/Gestures/WhatSThis_14
* animations/Stand/Gestures/WhatSThis_15
* animations/Stand/Gestures/WhatSThis_16
* animations/Stand/Gestures/WhatSThis_2
* animations/Stand/Gestures/WhatSThis_3
* animations/Stand/Gestures/WhatSThis_4
* animations/Stand/Gestures/WhatSThis_5
* animations/Stand/Gestures/WhatSThis_6
* animations/Stand/Gestures/WhatSThis_7
* animations/Stand/Gestures/WhatSThis_8
* animations/Stand/Gestures/WhatSThis_9
* animations/Stand/Gestures/Wings_1
* animations/Stand/Gestures/Wings_2
* animations/Stand/Gestures/Wings_3
* animations/Stand/Gestures/Wings_4
* animations/Stand/Gestures/Wings_5
* animations/Stand/Gestures/Yes_1
* animations/Stand/Gestures/Yes_2
* animations/Stand/Gestures/Yes_3
* animations/Stand/Gestures/You_1
* animations/Stand/Gestures/You_2
* animations/Stand/Gestures/You_3
* animations/Stand/Gestures/You_4
* animations/Stand/Gestures/You_5
* animations/Stand/Gestures/YouKnowWhat_1
* animations/Stand/Gestures/YouKnowWhat_2
* animations/Stand/Gestures/YouKnowWhat_3
* animations/Stand/Gestures/YouKnowWhat_4
* animations/Stand/Gestures/YouKnowWhat_5
* animations/Stand/Gestures/YouKnowWhat_6
* animations/Stand/Gestures/Yum_1
* animations/Stand/Reactions/BumperLeft_1
* animations/Stand/Reactions/BumperRight_1
* animations/Stand/Reactions/Bumpers_1
* animations/Stand/Reactions/Bumpers_2
* animations/Stand/Reactions/Bumpers_3
* animations/Stand/Reactions/EthernetOff_1
* animations/Stand/Reactions/EthernetOn_1
* animations/Stand/Reactions/Heat_1
* animations/Stand/Reactions/Heat_2
* animations/Stand/Reactions/LightShine_1
* animations/Stand/Reactions/LightShine_2
* animations/Stand/Reactions/LightShine_3
* animations/Stand/Reactions/LightShine_4
* animations/Stand/Reactions/SeeColor_1
* animations/Stand/Reactions/SeeColor_2
* animations/Stand/Reactions/SeeColor_3
* animations/Stand/Reactions/SeeSomething_1
* animations/Stand/Reactions/SeeSomething_3
* animations/Stand/Reactions/SeeSomething_4
* animations/Stand/Reactions/SeeSomething_5
* animations/Stand/Reactions/SeeSomething_6
* animations/Stand/Reactions/SeeSomething_7
* animations/Stand/Reactions/SeeSomething_8
* animations/Stand/Reactions/ShakeBody_1
* animations/Stand/Reactions/ShakeBody_2
* animations/Stand/Reactions/ShakeBody_3
* animations/Stand/Reactions/TouchHead_1
* animations/Stand/Reactions/TouchHead_2
* animations/Stand/Reactions/TouchHead_3
* animations/Stand/Reactions/TouchHead_4
* animations/Stand/Waiting/AirGuitar_1
* animations/Stand/Waiting/AirJuggle_1
* animations/Stand/Waiting/BackRubs_1
* animations/Stand/Waiting/Bandmaster_1
* animations/Stand/Waiting/Binoculars_1
* animations/Stand/Waiting/CallSomeone_1
* animations/Stand/Waiting/Drink_1
* animations/Stand/Waiting/DriveCar_1
* animations/Stand/Waiting/Fitness_1
* animations/Stand/Waiting/Fitness_2
* animations/Stand/Waiting/Fitness_3
* animations/Stand/Waiting/FunnyDancer_1
* animations/Stand/Waiting/FunnySlide_1
* animations/Stand/Waiting/HappyBirthday_1
* animations/Stand/Waiting/Headbang_1
* animations/Stand/Waiting/Helicopter_1
* animations/Stand/Waiting/HideEyes_1
* animations/Stand/Waiting/HideHands_1
* animations/Stand/Waiting/Innocent_1
* animations/Stand/Waiting/Knight_1
* animations/Stand/Waiting/KnockEye_1
* animations/Stand/Waiting/KungFu_1
* animations/Stand/Waiting/LookHand_1
* animations/Stand/Waiting/LookHand_2
* animations/Stand/Waiting/LoveYou_1
* animations/Stand/Waiting/Monster_1
* animations/Stand/Waiting/MysticalPower_1
* animations/Stand/Waiting/PlayHands_1
* animations/Stand/Waiting/PlayHands_2
* animations/Stand/Waiting/PlayHands_3
* animations/Stand/Waiting/Relaxation_1
* animations/Stand/Waiting/Relaxation_2
* animations/Stand/Waiting/Relaxation_3
* animations/Stand/Waiting/Relaxation_4
* animations/Stand/Waiting/Rest_1
* animations/Stand/Waiting/Robot_1
* animations/Stand/Waiting/ScratchBack_1
* animations/Stand/Waiting/ScratchBottom_1
* animations/Stand/Waiting/ScratchEye_1
* animations/Stand/Waiting/ScratchHand_1
* animations/Stand/Waiting/ScratchHead_1
* animations/Stand/Waiting/ScratchLeg_1
* animations/Stand/Waiting/ScratchTorso_1
* animations/Stand/Waiting/ShowMuscles_1
* animations/Stand/Waiting/ShowMuscles_2
* animations/Stand/Waiting/ShowMuscles_3
* animations/Stand/Waiting/ShowMuscles_4
* animations/Stand/Waiting/ShowMuscles_5
* animations/Stand/Waiting/ShowSky_1
* animations/Stand/Waiting/ShowSky_2
* animations/Stand/Waiting/SpaceShuttle_1
* animations/Stand/Waiting/Stretch_1
* animations/Stand/Waiting/Stretch_2
* animations/Stand/Waiting/Stretch_3
* animations/Stand/Waiting/TakePicture_1
* animations/Stand/Waiting/Taxi_1
* animations/Stand/Waiting/Think_1
* animations/Stand/Waiting/Think_2
* animations/Stand/Waiting/Think_3
* animations/Stand/Waiting/Think_4
* animations/Stand/Waiting/Vacuum_1
* animations/Stand/Waiting/Waddle_1
* animations/Stand/Waiting/Waddle_2
* animations/Stand/Waiting/WakeUp_1
* animations/Stand/Waiting/WalkInTheShit_1
* animations/Stand/Waiting/Zombie_1
* animations/Stand/Enumeration/NAO/Center_Neutral_ENU_06
* animations/Stand/Enumeration/NAO/Left_Neutral_ENU_05
* animations/Stand/Enumeration/NAO/Left_Neutral_ENU_02
* animations/Stand/Enumeration/NAO/Center_Slow_ENU_02
* animations/Stand/Enumeration/NAO/Center_Slow_ENU_04
* animations/Stand/Enumeration/NAO/Right_Neutral_ENU_03
* animations/Stand/Enumeration/NAO/Left_Neutral_ENU_03
* animations/Stand/Enumeration/NAO/Right_Strong_ENU_04
* animations/Stand/Enumeration/NAO/Center_Neutral_ENU_02
* animations/Stand/Enumeration/NAO/Right_Neutral_ENU_02
* animations/Stand/Enumeration/NAO/Right_Neutral_ENU_01
* animations/Stand/Enumeration/NAO/Right_Neutral_ENU_04
* animations/Stand/Enumeration/NAO/Left_Neutral_ENU_04
* animations/Stand/Enumeration/NAO/Center_Strong_ENU_02
* animations/Stand/Enumeration/NAO/Right_Strong_ENU_02
* animations/Stand/Enumeration/NAO/Left_Neutral_ENU_01
* animations/Stand/Enumeration/NAO/Center_Strong_ENU_01
* animations/Stand/Enumeration/NAO/Center_Neutral_ENU_01
* animations/Stand/Enumeration/NAO/Center_Neutral_ENU_04
* animations/Stand/Enumeration/NAO/Center_Strong_ENU_03
* animations/Stand/Enumeration/NAO/Center_Slow_ENU_01
* animations/Stand/Enumeration/NAO/Center_Slow_ENU_03
* animations/Stand/Enumeration/NAO/Center_Neutral_ENU_07
* animations/Stand/Enumeration/NAO/Left_Strong_ENU_03
* animations/Stand/Enumeration/NAO/Right_Strong_ENU_03
* animations/Stand/Enumeration/NAO/Center_Neutral_ENU_03
* animations/Stand/Enumeration/NAO/Left_Strong_ENU_02
* animations/Stand/Enumeration/NAO/Right_Neutral_ENU_05
* animations/Stand/Enumeration/NAO/Left_Strong_ENU_04
* animations/Stand/Self & others/NAO/Right_Strong_SAO_05
* animations/Stand/Self & others/NAO/Left_Neutral_SAO_03
* animations/Stand/Self & others/NAO/Left_Neutral_SAO_01
* animations/Stand/Self & others/NAO/Left_Slow_SAO_02
* animations/Stand/Self & others/NAO/Right_Slow_SAO_02
* animations/Stand/Self & others/NAO/Left_Neutral_SAO_06
* animations/Stand/Self & others/NAO/Right_Neutral_SAO_04
* animations/Stand/Self & others/NAO/Right_Strong_SAO_02
* animations/Stand/Self & others/NAO/Left_Slow_SAO_01
* animations/Stand/Self & others/NAO/Center_Strong_SAO_02
* animations/Stand/Self & others/NAO/Right_Neutral_SAO_03
* animations/Stand/Self & others/NAO/Right_Strong_SAO_04
* animations/Stand/Self & others/NAO/Right_Strong_SAO_03
* animations/Stand/Self & others/NAO/Left_Neutral_SAO_05
* animations/Stand/Self & others/NAO/Right_Neutral_SAO_02
* animations/Stand/Self & others/NAO/Left_Neutral_SAO_02
* animations/Stand/Self & others/NAO/Center_Neutral_SAO_05
* animations/Stand/Self & others/NAO/Center_Strong_SAO_01
* animations/Stand/Self & others/NAO/Right_Slow_SAO_01
* animations/Stand/Self & others/NAO/Left_Neutral_SAO_04
* animations/Stand/Self & others/NAO/Left_Strong_SAO_05
* animations/Stand/Self & others/NAO/Left_Strong_SAO_04
* animations/Stand/Self & others/NAO/Left_Strong_SAO_03
* animations/Stand/Self & others/NAO/Center_Neutral_SAO_01
* animations/Stand/Self & others/NAO/Left_Strong_SAO_02
* animations/Stand/Self & others/NAO/Right_Neutral_SAO_06
* animations/Stand/Self & others/NAO/Center_Neutral_SAO_02
* animations/Stand/Self & others/NAO/Left_Strong_SAO_01
* animations/Stand/Self & others/NAO/Center_Neutral_SAO_04
* animations/Stand/Self & others/NAO/Center_Neutral_SAO_03
* animations/Stand/Self & others/NAO/Right_Strong_SAO_01
* animations/Stand/Self & others/NAO/Right_Neutral_SAO_01
* animations/Stand/Self & others/NAO/Right_Neutral_SAO_05
* animations/Stand/Negation/NAO/Center_Neutral_NEG_01
* animations/Stand/Negation/NAO/Left_Strong_NEG_01
* animations/Stand/Negation/NAO/Left_Strong_NEG_03
* animations/Stand/Negation/NAO/Center_Slow_NEG_01
* animations/Stand/Negation/NAO/Right_Neutral_NEG_01
* animations/Stand/Negation/NAO/Right_Strong_NEG_04
* animations/Stand/Negation/NAO/Center_Strong_NEG_03
* animations/Stand/Negation/NAO/Right_Strong_NEG_02
* animations/Stand/Negation/NAO/Center_Neutral_NEG_02
* animations/Stand/Negation/NAO/Left_Strong_NEG_04
* animations/Stand/Negation/NAO/Left_Strong_NEG_02
* animations/Stand/Negation/NAO/Center_Strong_NEG_01
* animations/Stand/Negation/NAO/Right_Strong_NEG_03
* animations/Stand/Negation/NAO/Center_Neutral_NEG_04
* animations/Stand/Negation/NAO/Center_Strong_NEG_04
* animations/Stand/Negation/NAO/Center_Neutral_NEG_03
* animations/Stand/Negation/NAO/Center_Strong_NEG_05
* animations/Stand/Negation/NAO/Right_Strong_NEG_01
* animations/Stand/Negation/NAO/Center_Slow_NEG_02
* animations/Stand/Negation/NAO/Left_Neutral_NEG_01
* animations/Stand/Exclamation/NAO/Left_Neutral_EXC_02
* animations/Stand/Exclamation/NAO/Right_Strong_EXC_01
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_05
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_09
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_04
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_08
* animations/Stand/Exclamation/NAO/Right_Neutral_EXC_02
* animations/Stand/Exclamation/NAO/Left_Strong_EXC_04
* animations/Stand/Exclamation/NAO/Right_Neutral_EXC_05
* animations/Stand/Exclamation/NAO/Left_Strong_EXC_03
* animations/Stand/Exclamation/NAO/Left_Strong_EXC_01
* animations/Stand/Exclamation/NAO/Left_Neutral_EXC_05
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_06
* animations/Stand/Exclamation/NAO/Center_Slow_EXC_01
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_03
* animations/Stand/Exclamation/NAO/Right_Strong_EXC_03
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_03
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_05
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_10
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_08
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_07
* animations/Stand/Exclamation/NAO/Right_Strong_EXC_02
* animations/Stand/Exclamation/NAO/Left_Strong_EXC_02
* animations/Stand/Exclamation/NAO/Center_Slow_EXC_02
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_02
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_06
* animations/Stand/Exclamation/NAO/Center_Slow_EXC_03
* animations/Stand/Exclamation/NAO/Center_Strong_EXC_04
* animations/Stand/Exclamation/NAO/Center_Neutral_EXC_01
* animations/Stand/Exclamation/NAO/Right_Strong_EXC_04
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_08
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_09
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_07
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_06
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Neutral_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_04
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Neutral_AFF_06
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_06
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_08
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Neutral_AFF_05
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Slow_AFF_01
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Slow_AFF_05
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_07
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Neutral_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Neutral_AFF_06
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_11
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Slow_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_13
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Strong_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Strong_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Slow_AFF_03
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_05
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Neutral_AFF_05
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Slow_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_10
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Slow_AFF_02
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_01
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Slow_AFF_01
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Neutral_AFF_04
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_04
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Slow_AFF_01
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Slow_AFF_06
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_05
* animations/Stand/BodyTalk/BodyLanguage/NAO/Left_Neutral_AFF_04
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Strong_AFF_01
* animations/Stand/BodyTalk/BodyLanguage/NAO/Right_Slow_AFF_03
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Neutral_AFF_12
* animations/Stand/BodyTalk/BodyLanguage/NAO/Center_Slow_AFF_03
* animations/Stand/Question/NAO/Center_Neutral_QUE_09
* animations/Stand/Question/NAO/Right_Neutral_QUE_02
* animations/Stand/Question/NAO/Center_Strong_QUE_03
* animations/Stand/Question/NAO/Left_Neutral_QUE_01
* animations/Stand/Question/NAO/Right_Neutral_QUE_03
* animations/Stand/Question/NAO/Right_Neutral_QUE_01
* animations/Stand/Question/NAO/Center_Neutral_QUE_06
* animations/Stand/Question/NAO/Center_Neutral_QUE_04
* animations/Stand/Question/NAO/Center_Slow_QUE_01
* animations/Stand/Question/NAO/Center_Slow_QUE_02
* animations/Stand/Question/NAO/Center_Strong_QUE_01
* animations/Stand/Question/NAO/Center_Neutral_QUE_10
* animations/Stand/Question/NAO/Center_Neutral_QUE_03
* animations/Stand/Question/NAO/Left_Neutral_QUE_02
* animations/Stand/Question/NAO/Center_Neutral_QUE_02
* animations/Stand/Question/NAO/Center_Neutral_QUE_08
* animations/Stand/Question/NAO/Center_Neutral_QUE_05
* animations/Stand/Question/NAO/Left_Neutral_QUE_03
* animations/Stand/Question/NAO/Center_Strong_QUE_02
* animations/Stand/Question/NAO/Center_Neutral_QUE_01
* animations/Stand/Question/NAO/Center_Slow_QUE_03
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_06
* animations/Stand/Space & time/NAO/Left_Strong_SAT_02
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_03
* animations/Stand/Space & time/NAO/Left_Slow_SAT_01
* animations/Stand/Space & time/NAO/Center_Slow_SAT_02
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_08
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_05
* animations/Stand/Space & time/NAO/Left_Strong_SAT_03
* animations/Stand/Space & time/NAO/Center_Neutral_SAT_01
* animations/Stand/Space & time/NAO/Right_Strong_SAT_02
* animations/Stand/Space & time/NAO/Right_Strong_SAT_06
* animations/Stand/Space & time/NAO/Center_Neutral_SAT_04
* animations/Stand/Space & time/NAO/Left_Strong_SAT_05
* animations/Stand/Space & time/NAO/Center_Slow_SAT_03
* animations/Stand/Space & time/NAO/Center_Strong_SAT_02
* animations/Stand/Space & time/NAO/Right_Strong_SAT_04
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_08
* animations/Stand/Space & time/NAO/Left_Strong_SAT_06
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_04
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_01
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_10
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_04
* animations/Stand/Space & time/NAO/Center_Neutral_SAT_03
* animations/Stand/Space & time/NAO/Center_Strong_SAT_01
* animations/Stand/Space & time/NAO/Center_Slow_SAT_01
* animations/Stand/Space & time/NAO/Left_Strong_SAT_01
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_03
* animations/Stand/Space & time/NAO/Left_Strong_SAT_04
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_07
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_09
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_05
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_02
* animations/Stand/Space & time/NAO/Right_Slow_SAT_01
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_01
* animations/Stand/Space & time/NAO/Center_Neutral_SAT_02
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_09
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_07
* animations/Stand/Space & time/NAO/Right_Strong_SAT_03
* animations/Stand/Space & time/NAO/Right_Strong_SAT_05
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_10
* animations/Stand/Space & time/NAO/Left_Neutral_SAT_02
* animations/Stand/Space & time/NAO/Right_Neutral_SAT_06
* animations/Stand/Space & time/NAO/Right_Strong_SAT_01
* boot-config
* boot-config/animations/onNextPage
* boot-config/animations/onPrevPage
* boot-config/animations/poseInit
* boot-config/animations/ok
* boot-config/animations/success
* boot-config/animations/poseInitUp
* boot-config/animations/turnTabletOn_end
* boot-config/animations/turnTabletOn_start
* boot-config/animations/warning
* boot-config/animations/warningValidate
* boot-config/animations/nok
* boot-config/animations/updateLoop
* boot-config/animations/updateOut
* boot-config/animations/networkLoop
* boot-config/animations/networkOut
* boot-config/animations/inviteTablet
* boot-config/animations/hello
* boot-config/animations/updateFailed
* boot-config/animations/finishWizard
* boot-config/animations/onPlugged
* boot-config/animations/onUnPlugged
* boot-config/animations/shutdown
* boot-config/animations/bipGentle
* boot-config/animations/endReco
* run_dialog_dev
* run_dialog_dev/init
* sleep-reactions/Animations/Start_ShakeHead
* sleep-reactions/Animations/End_ShakeHead
* sleep-reactions/TouchHand
* sleep-reactions/RandomHand
* .lastUploadedChoregrapheBehavior/behavior_1
