# Codvote-B3-plugin
Vote plugin for Call of Duty Servers

Usage:
!vote map <map name> - will immediately change map to <map name>
!vote nextmap <map name> - will change the next map in rotation to <map name> 
!vote kick <player> - kick <player> from server (admins cannot be kicked by vote)
!vote maprestart - clear all scores and reset time on map
!vote maprotate - cycle to next map on rotation
!vote killcam <on/off> - turn killcam on or off (can also use 1 or 0)
!vote timelimit <number> - change length of time until map ends to <number>
!vote scorelimit <number> - Change score needed for victory to <number>
!vote roundlength <number> - Change length of rounds to <number> in ctf and sd modes
!vote roundlimit <number> - change amount of rounds game will go on for in ctf and sd modes to <number>
!veto - Cancels the vote in progress


Plugin behavior:
- A vote will remain active for "votetime" specified in config. The vote will fail if not enough players vote within that time.
  An extra 5 seconds for players to read what they are voting for will be added.

- Only players that were in the server at the time the vote was called will be able to vote.
   If anyone enters the server after vote is initiated will not be allowed to vote.

- Admin at level 20 and up will not be affected by a kick vote. The plugin will refuse to initiate the vote against an admin.

- There must be more than 1 players in game for vote to work. Unless vote is called by superadmin.
