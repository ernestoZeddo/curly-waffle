# curly-waffle
PPPPPPPPPPPPistol


// Damage Given/Taken
con_filter_text damage
con_filter_enable 2

BindToggle j gameinstructor_enable

snd_headphone_pan_exponent 3
sv_voicecodec vaudio_celt


// Hud
hud_showtargetid "1" //Enables display of target names, important
cl_hud_bomb_under_radar "1" //Draws bomb under radar, convenient
cl_hud_radar_scale "0.8" //Radar Size, not too big and not too small
cl_radar_scale "0.6" //Radar Map Scale Size, 0.3 is perfect on all maps
cl_radar_always_centered "0" //Centers map instead of player in radar, important
cl_hud_playercount_showcount "0" //Shows player avatars instead of numbers left
cl_hud_playercount_pos "0" //Puts player information in the bottom instead of top
cl_hud_healthammo_style "1" //Simplified information on HP/AP and ammo
cl_hud_background_alpha "0.2" //Hidden but still visible black bars, easy on the eyes
cl_loadout_colorweaponnames "1" //Weapon names are colored in loadout to match their rarity, cool feature
cl_radar_icon_scale_min "0.8" //Sets the minimum player icon scale, this value feels good
cl_showloadout "1" //So it doesnt fade out the weapon slots, very annoying otherwise
hud_scaling "0.8" //Scales hud elements to maximum value
safezonex "0.85" //Centers the hud closer to the middle
safezoney "0.85" //Centers the hud closer to the middle


// Bob
cl_bob_lower_amt "5" //How much the viewmodel lowers when running, set to lowest for less distraction
cl_bobamt_lat "0.1" //How much the viewmodel moves side to side when running, set to lowest for less distraction
cl_bobamt_vert "0.1" //How much the viewmodel moves up and down when running, set to lowest for less distraction
cl_bobcycle "0.98" //The frequency at which the viewmodel bobs, set to default
cl_viewmodel_shift_left_amt "1" //Removes shifting of arms
cl_viewmodel_shift_right_amt "1" //Removes shifting of arms

// Bindings
bind "mouse3" "+voicerecord" //More comfortable way of talking with your teammates
bind "f1" "autobuy" //Autobuy weapons if you have lots of money with F1
bind "f3" "buy flashbang;buy smokegrenade;buy flashbang;buy hegrenade" //Buy all the important grenades with F3
bind "f4" "ignoremsg" //Ignore chat by turning off enemies, teams and both
bind "f" "+lookatweapon" //Inspect your weapon with F
bind mwheelup +jump //Makes bunnyhopping better
bind mwheeldown +jump //Makes bunnyhopping better
unbind "i" //So you don't accidentally enable hud fade, which is very annoying
bind "f6" "incrementvar sensitivity 1.76 10000 9998.24"
bind "f7" "incrementvar voice_loopback 0 1 1"
bind "f8" "incrementvar r_drawothermodels 1 2 1" 



// Rates (Settings are optimized for best networking experience)
rate "128000" //Max bytes per second the host can receive data
cl_cmdrate "128" //Max number of command packets sent to server per second
cl_updaterate "128" //Number of packets per second you are requesting from the server
cl_interp_ratio "1" //Sets the interpolation amount (final amount is cl_interp_ratio / cl_updaterate)
cl_interp "0" //Sets the interpolation amount, always set this to 0
cl_lagcompensation "1" //Lag compensation helps by eliminating combat latency from client side view
cl_predict "1" //Skip waiting for server feedback and simulate client side movement in real-time
cl_predictweapons "1" //Skip waiting for server feedback and perform client side prediction of weapon effects

// Video
mat_monitorgamma "1.6" //Brightness, use this value for best brightness
mat_monitorgamma_tv_enabled "0" //Turn off TV Mode

// Sound
voice_scale "0.5" //Turns down the volume of other players voice to 40%
snd_mixahead "0.05" //Makes sound as instant as it can get, making it easier to hear small things
snd_musicvolume "0" //Turns off all music, easier to focus

// Net
fps_max "600" //Setting this to 0 will uncap it but will load maps 90 seconds slower. 600 gave me the best results.
fps_max_menu "60" //Frame limiting my menu to 300 because I can
net_graph "1" //Shows my network usage data
net_graphheight "990" //Changes height, used together with script
net_graphmsecs "400" //The latency graph represents this many milliseconds
net_graphpos "2" //Positioning of Net Graph
net_graphproportionalfont "0" //Makes font smaller
net_graphshowinterp "1" //Shows interpolation value
net_graphshowlatency "1" //Shows latency value
net_graphsolid "1" //Solid Net Graph
net_graphtext "1" //Shows text fields
net_maxroutable "1200" //Requested max packet size before packets are 'split'
net_scale "5" //Makes font smaller

// Other
r_drawtracers_firstperson "1" //Hides bullet tracers in first person view
lobby_voice_chat_enabled "0" //Turns microphone off in lobby, really useful
cl_use_opens_buy_menu "0" //Disables E from opening buy-menu, really useful
mm_dedicated_search_maxping "50" //Maxping Search in Matchmaking
con_enable "1" // Enables console

// Mouse
sensitivity 2.05
m_rawinput "1" //Enable Raw Input for perfect precision (Raw input is unavailable on OSX)
m_mouseaccel2 "0" //Disables windows mouse acceleration initial threshold, safety precaution
m_mouseaccel1 "0" //Disables windows mouse acceleration initial threshold, safety precaution
m_customaccel "0" //Custom mouse acceleration disabled

// Grenade Bind
alias +jumpsmoke "+jump; -attack"
alias -jumpsmoke "-jump"
bind "h" "+jumpsmoke"

// Show netgraph when checking scoreboard script
alias "+scorenet" "+showscores; net_graphheight 0"
alias "-scorenet" "-showscores; net_graphheight 9999"
bind "TAB" "+scorenet" //Bind TAB to whatever you prefer

// Display Damage with Switch Script
alias displaydamage "displaydamage_on"
alias displaydamage_on "con_filter_text Damage Given To; con_filter_text_out Player:; con_filter_enable 2; developer 1; playvol buttons\blip1 0.5; alias displaydamage "displaydamage_off""
alias displaydamage_off "con_filter_enable 0; developer 0; playvol buttons\blip2 0.5; alias displaydamage "displaydamage_on""
bind "F5" "displaydamage" //Bind F5 to whatever you prefer
