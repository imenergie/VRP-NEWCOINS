Installation:
1. Make a backup of your .lua files for the first time just in case.
2. copy the hologram folder to the resources folder on the server.
2. copy the vrp folder files to the resources server where the vrp folder on the server is located except for the vrp/cfg/groups.lua and vrp/cfg/blips_markers.lua files. I say this because it is better for you to modify these two files because it is possible that your files on the server will be different.
3. in the resources folder on your server enter the vrp/cfg/folder and modify groups.lua by adding the line:

"player.givediamante",

Example:
cfg.groups = {
  ["superadmin"] = {
    _config = {onspawn = function(player) vRPclient.notify(player,{"You are superadmin."}) end},
    "player.group.add",
    "player.group.remove",
    "player.givemoney",
    "player.givediamante",
    "player.giveitem"
  },

4. in the blis_markers.lua from same place adding the lines:

  {-622.97601318359,-233.21601867676,38.057048797607,108,1,"Diamante Exchange"},
  {-624.58612060547,-230.85711669922,38.057048797607,108,1,"Money Exchange"},
  
Example:
cfg.blips = {
  {-1202.96252441406,-1566.14086914063,4.61040639877319,311,17,"Body training"},
  {460.190338134766,-993.888488769531,24.914867401123,60,38,"Police Station"},
  {1853.21, 3689.51, 34.2671,60,17,"Police Station"},
  {391.541442871094,-1615.154296875,29.291934967041,60,38,"Police Station"}, 
  {-261.40533447266,-965.15747070313,31.224115371704,315,4,"Driver License"},
  {244.1099395752,-1382.8720703125,39.534328460693,61,3,"Hospital Station"},
  {415.2883605957,-1652.4112548828,29.291698455811,446,47,"Repair Station"},
  {236.41926574707,216.96081542969,106.28672790527,434,4,"Bank Driver Station"},  
  {1049.39819,-555.6142,59.1099167,410,47,"Park"},
  {449.81854248047,-993.30865478516,30.689584732056,73,3,"Police Outfits"},
  {575.40698242188,-3121.94921875,18.768627166748,433,1,"Bounty Hunter"},
  {138.28096008301,-764.61865234375,45.752029418945,88,5,"FBI"},
  {-622.97601318359,-233.21601867676,38.057048797607,108,1,"Diamante Exchange"},
  {-624.58612060547,-230.85711669922,38.057048797607,108,1,"Money Exchange"},
  {743.19586181641,3895.3967285156,30.556676864624,68,28,"Fisherman"}
}

5. Go to the database from http://localhost/phpmyadmin and get in your database name from the server. Enter in vrp_user_moneys and export him for backup and then import the file called vrp_user_moneys.sql from mine folder.
6. Open the server and see if it works. If it gives you the same error ask someone who is better at databases or if you are not interested in what you have in the database you can simply delete everything that starts with vrp_ and then start the server. That will definitely work. Good luck!
