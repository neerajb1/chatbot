## happy path 1
* greet: hello there!
    - utter_greet   <!-- predicted: find_facility_types -->
* mood_great: amazing
    - utter_happy   <!-- predicted: action_default_ask_affirmation -->


## happy path 2
* greet: hello there!
    - utter_greet   <!-- predicted: find_facility_types -->
* mood_great: amazing
    - utter_happy   <!-- predicted: action_default_ask_affirmation -->
* goodbye: bye-bye!
    - utter_goodbye   <!-- predicted: action_default_fallback -->


## sad path 1
* greet: hello
    - utter_greet   <!-- predicted: find_facility_types -->
* mood_unhappy: not good
    - utter_cheer_up   <!-- predicted: action_default_fallback -->
    - utter_did_that_help   <!-- predicted: action_listen -->
* affirm: yes
    - utter_happy   <!-- predicted: action_default_fallback -->


## sad path 2
* greet: hello
    - utter_greet   <!-- predicted: find_facility_types -->
* mood_unhappy: not good
    - utter_cheer_up   <!-- predicted: action_default_fallback -->
    - utter_did_that_help   <!-- predicted: action_listen -->
* deny: not really
    - utter_goodbye   <!-- predicted: action_default_fallback -->


## sad path 3
* greet: hi
    - utter_greet   <!-- predicted: find_facility_types -->
* mood_unhappy: very terrible
    - utter_cheer_up   <!-- predicted: action_default_fallback -->
    - utter_did_that_help   <!-- predicted: action_listen -->
* deny: no
    - utter_goodbye   <!-- predicted: action_default_fallback -->


## bot challenge
* bot_challenge: are you a bot?   <!-- predicted: thanks: are you a bot? -->
    - utter_iamabot   <!-- predicted: utter_noworries -->


