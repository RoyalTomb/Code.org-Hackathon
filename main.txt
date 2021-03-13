//Variables
var id = getColumn("Top 200 USA", "id");
var trackName = getColumn("Top 200 USA", "Track Name");
var artist = getColumn("Top 200 USA", "Artist");
var position = getColumn("Top 200 USA", "Position");
var numberStreams = getColumn("Top 200 USA", "Streams");
var link = getColumn("Top 200 USA", "URL");
var songnumber = getNumber("slider1");
var songnumber2 = getNumber("slider2");
//New [filtered] lists
var idFiltered = [];
var trackNameFiltered = [];
var artistFiltered = [];
var positionFiltered = [];
var numberStreamsFiltered = [];
var linkFiltered = [];
//Screen Buttons (screen-to-screen)
screenbuttonsFunction();
//Screen 1
onEvent("slider1", "mousemove", function( ) {
  songnumber = getNumber ("slider1");
  setText("songlist01", "# " + songnumber);
  updatetracksScreen01();
});

onEvent("listbutton01", "click", function( ) {
  setText("songlist01", "#1 " + trackName [0]) ;
  setText("songlist02", "#2 " + trackName [1]);
  setText("songlist03", "#3 " + trackName [2]);
});
//Screen 2
var filteredartistList = [];
var placement = 0;
onEvent("enterButton", "click", function( ) {
  playSound("sound://category_app/app_button_2.mp3", false);
  placement = getNumber("text_input1");
  for (var i = 0; i < id.length; i++) {
    if (id[i] <= 200) {
      appendItem(filteredartistList, artist[i]);
    }
    if (placement <= 200 && placement >= 1) {
      setText("topfiftysongList", ((("Click Search to find a random artist near the top" +  " ") + placement + ":")  + " ")  + filteredartistList[(randomNumber (1, filteredartistList.length - 1))]);
    }
  }
});
//Screen 3
onEvent("slider2", "mousemove", function( ) {
   songnumber2 = getNumber("slider2");
  setText("label2", "# " + songnumber2);
  updateScreen3();
});

//Functions
function updatetracksScreen01() {
  if (songnumber == 100) {
    setText("songlist02", trackName[99]);
    setText("songlist03", artist [99]);
  } else if (songnumber == 99) {
    setText("songlist02", trackName[98]);
    setText("songlist03", artist [98]);
  } else if (songnumber == 98) {
    setText("songlist02", trackName[97]);
    setText("songlist03", artist [97]);
  } else if (songnumber == 97) {
     setText("songlist02", trackName[96]);
     setText("songlist03", artist [96]);
  } else if (songnumber == 96) {
     setText("songlist02", trackName[95]);
     setText("songlist03", artist [95]);
  } else if (songnumber == 95) {
     setText("songlist02", trackName[94]);
     setText("songlist03", artist [94]);
  } else if ((songnumber == 94)) {
     setText("songlist02", trackName[93]);
     setText("songlist03", artist [93]);
  } else if ((songnumber == 93)) {
     setText("songlist02", trackName[92]);
     setText("songlist03", artist [92]);
  } else if (songnumber == 92) {
     setText("songlist02", trackName[91]);
     setText("songlist03", artist [91]);
  } else if (songnumber == 91) {
     setText("songlist02", trackName[90]);
     setText("songlist03", artist [90]);
  } else if (songnumber == 90) {
     setText("songlist02", trackName[89]);
     setText("songlist03", artist [89]);
  } else if (songnumber == 89) {
     setText("songlist02", trackName[88]);
     setText("songlist03", artist [88]);
  } else if (songnumber == 88) {
     setText("songlist02", trackName[87]);
     setText("songlist03", artist [87]);
  } else if (songnumber == 87) {
     setText("songlist02", trackName[86]);
     setText("songlist03", artist [86]);
  } else if (songnumber == 86) {
     setText("songlist02", trackName[85]);
     setText("songlist03", artist [85]);
  } else if (songnumber == 85) {
     setText("songlist02", trackName[84]);
     setText("songlist03", artist [84]);
  } else if (songnumber == 84) {
     setText("songlist02", trackName[83]);
     setText("songlist03", artist [83]);
  } else if (songnumber == 83) {
     setText("songlist02", trackName[82]);
     setText("songlist03", artist [82]);
  } else if (songnumber == 82) {
     setText("songlist02", trackName[81]);
     setText("songlist03", artist [81]);
  } else if (songnumber == 81) {
     setText("songlist02", trackName[80]);
     setText("songlist03", artist [80]);
  } else if (songnumber == 80) {
     setText("songlist02", trackName[79]);
     setText("songlist03", artist [79]);
  } else if (songnumber == 79) {
     setText("songlist02", trackName[78]);
     setText("songlist03", artist [78]);
  } else if (songnumber == 78) {
     setText("songlist02", trackName[77]);
     setText("songlist03", artist [77]);
  } else if (songnumber == 77) {
     setText("songlist02", trackName[76]);
     setText("songlist03", artist [76]);
  } else if (songnumber == 76) {
     setText("songlist02", trackName[75]);
     setText("songlist03", artist [75]);
  } else if (songnumber == 75) {
     setText("songlist02", trackName[74]);
     setText("songlist03", artist [74]);
  } else if (songnumber == 74) {
     setText("songlist02", trackName[73]);
     setText("songlist03", artist [73]);
  } else if (songnumber == 73) {
     setText("songlist02", trackName[72]);
     setText("songlist03", artist [72]);
  } else if (songnumber == 72) {
     setText("songlist02", trackName[71]);
     setText("songlist03", artist [71]);
  } else if (songnumber == 71) {
     setText("songlist02", trackName[70]);
     setText("songlist03", artist [70]);
  } else if (songnumber == 70) {
     setText("songlist02", trackName[69]);
     setText("songlist03", artist [69]);
  } else if (songnumber == 69) {
     setText("songlist02", trackName[68]);
     setText("songlist03", artist [68]);
  } else if (songnumber == 68) {
     setText("songlist02", trackName[67]);
     setText("songlist03", artist [67]);
  } else if (songnumber == 67) {
     setText("songlist02", trackName[66]);
     setText("songlist03", artist [66]);
  } else if (songnumber == 66) {
     setText("songlist02", trackName[65]);
     setText("songlist03", artist [65]);
  } else if (songnumber == 65) {
     setText("songlist02", trackName[64]);
     setText("songlist03", artist [64]);
  } else if (songnumber == 64) {
     setText("songlist02", trackName[63]);
     setText("songlist03", artist [63]);
  } else if (songnumber == 63) {
     setText("songlist02", trackName[62]);
     setText("songlist03", artist [62]);
  } else if (songnumber == 62) {
     setText("songlist02", trackName[61]);
     setText("songlist03", artist [61]);
  } else if (songnumber == 61) {
     setText("songlist02", trackName[60]);
     setText("songlist03", artist [60]);
  } else if (songnumber == 60) {
     setText("songlist02", trackName[59]);
     setText("songlist03", artist [59]);
  } else if (songnumber == 59) {
     setText("songlist02", trackName[58]);
     setText("songlist03", artist [58]);
  } else if (songnumber == 58) {
     setText("songlist02", trackName[57]);
     setText("songlist03", artist [57]);
  } else if (songnumber == 57) {
     setText("songlist02", trackName[56]);
     setText("songlist03", artist [56]);
  } else if (songnumber == 56) {
     setText("songlist02", trackName[55]);
     setText("songlist03", artist [55]);
  } else if (songnumber == 55) {
     setText("songlist02", trackName[54]);
     setText("songlist03", artist [54]);
  } else if (songnumber == 54) {
     setText("songlist02", trackName[53]);
     setText("songlist03", artist [53]);
  } else if (songnumber == 53) {
     setText("songlist02", trackName[52]);
     setText("songlist03", artist [52]);
  } else if (songnumber == 52) {
     setText("songlist02", trackName[51]);
     setText("songlist03", artist [51]);
  } else if (songnumber == 51) {
     setText("songlist02", trackName[50]);
     setText("songlist03", artist [50]);
  } else if (songnumber == 50) {
     setText("songlist02", trackName[49]);
     setText("songlist03", artist [49]);
  } else if (songnumber == 49) {
     setText("songlist02", trackName[48]);
     setText("songlist03", artist [48]);
  } else if (songnumber == 48) {
     setText("songlist02", trackName[47]);
     setText("songlist03", artist [47]);
  } else if (songnumber == 47) {
     setText("songlist02", trackName[46]);
     setText("songlist03", artist [46]);
  } else if (songnumber == 46) {
     setText("songlist02", trackName[45]);
     setText("songlist03", artist [45]);
  } else if (songnumber == 45) {
     setText("songlist02", trackName[44]);
     setText("songlist03", artist [44]);
  } else if (songnumber == 44) {
     setText("songlist02", trackName[43]);
     setText("songlist03", artist [43]);
  } else if (songnumber == 43) {
     setText("songlist02", trackName[42]);
     setText("songlist03", artist [42]);
  } else if (songnumber == 42) {
     setText("songlist02", trackName[41]);
     setText("songlist03", artist [41]);
  } else if (songnumber == 41) {
     setText("songlist02", trackName[40]);
     setText("songlist03", artist [40]);
  } else if (songnumber == 40) {
     setText("songlist02", trackName[39]);
     setText("songlist03", artist [39]);
  } else if (songnumber == 39) {
     setText("songlist02", trackName[38]);
     setText("songlist03", artist [38]);
  } else if (songnumber == 38) {
     setText("songlist02", trackName[37]);
     setText("songlist03", artist [37]);
  } else if (songnumber == 37) {
     setText("songlist02", trackName[36]);
     setText("songlist03", artist [36]);
  } else if (songnumber == 36) {
     setText("songlist02", trackName[35]);
     setText("songlist03", artist [35]);
  } else if (songnumber == 35) {
     setText("songlist02", trackName[34]);
     setText("songlist03", artist [34]);
  } else if (songnumber == 34) {
     setText("songlist02", trackName[33]);
     setText("songlist03", artist [33]);
  } else if (songnumber == 33) {
     setText("songlist02", trackName[32]);
     setText("songlist03", artist [32]);
  } else if (songnumber == 32) {
     setText("songlist02", trackName[31]);
     setText("songlist03", artist [31]);
  } else if (songnumber == 31) {
     setText("songlist02", trackName[30]);
     setText("songlist03", artist [30]);
  } else if (songnumber ==30) {
     setText("songlist02", trackName[29]);
     setText("songlist03", artist [29]);
  } else if (songnumber == 29) {
     setText("songlist02", trackName[28]);
     setText("songlist03", artist [28]);
  } else if (songnumber == 28) {
     setText("songlist02", trackName[27]);
     setText("songlist03", artist [27]);
  } else if ((songnumber == 27)) {
     setText("songlist02", trackName[26]);
     setText("songlist03", artist [26]);
  } else if (songnumber == 26) {
     setText("songlist02", trackName[25]);
     setText("songlist03", artist [25]);
  } else if (songnumber == 25) {
     setText("songlist02", trackName[24]);
     setText("songlist03", artist [24]);
  } else if (songnumber == 24) {
     setText("songlist02", trackName[23]);
     setText("songlist03", artist [23]);
  } else if (songnumber == 23) {
     setText("songlist02", trackName[22]);
     setText("songlist03", artist [22]);
  } else if (songnumber == 22) {
     setText("songlist02", trackName[21]);
     setText("songlist03", artist [21]);
  } else if (songnumber == 21) {
     setText("songlist02", trackName[20]);
     setText("songlist03", artist [20]);
  } else if (songnumber == 20) {
     setText("songlist02", trackName[19]);
     setText("songlist03", artist [19]);
  } else if (songnumber == 19) {
     setText("songlist02", trackName[18]);
     setText("songlist03", artist [18]);
  } else if (songnumber == 18) {
     setText("songlist02", trackName[17]);
     setText("songlist03", artist [17]);
  } else if (songnumber == 17) {
     setText("songlist02", trackName[16]);
     setText("songlist03", artist [16]);
  } else if (songnumber == 16) {
     setText("songlist02", trackName[15]);
     setText("songlist03", artist [15]);
  } else if (songnumber == 15) {
     setText("songlist02", trackName[14]);
     setText("songlist03", artist [14]);
  } else if (songnumber == 14) {
     setText("songlist02", trackName[13]);
     setText("songlist03", artist [13]);
  } else if (songnumber == 13) {
     setText("songlist02", trackName[12]);
     setText("songlist03", artist [12]);
  } else if (songnumber == 12) {
     setText("songlist02", trackName[11]);
     setText("songlist03", artist [11]);
  } else if (songnumber == 11) {
     setText("songlist02", trackName[10]);
     setText("songlist03", artist [10]);
  } else if (songnumber == 10) {
     setText("songlist02", trackName[9]);
     setText("songlist03", artist [9]);
  } else if (songnumber == 9) {
     setText("songlist02", trackName[8]);
     setText("songlist03", artist [8]);
  } else if (songnumber == 8) {
     setText("songlist02", trackName[7]);
     setText("songlist03", artist [7]);
  } else if (songnumber == 7) {
     setText("songlist02", trackName[6]);
     setText("songlist03", artist [6]);
  } else if (songnumber == 6) {
     setText("songlist02", trackName[5]);
     setText("songlist03", artist [5]);
  } else if (songnumber == 5) {
     setText("songlist02", trackName[4]);
     setText("songlist03", artist [4]);
  } else if (songnumber == 4) {
     setText("songlist02", trackName[3]);
     setText("songlist03", artist [3]);
  } else if (songnumber == 3) {
     setText("songlist02", trackName[2]);
     setText("songlist03", artist [2]);
  } else if (songnumber == 2) {
     setText("songlist02", trackName[1]);
     setText("songlist03", artist [1]);
  } else if (songnumber == 1) {
     setText("songlist02", trackName[0]);
     setText("songlist03", artist [0]);
  } else if (songnumber == 0) {
     setText("songlist02", "Ha, you actually thought there's a #0 song");
     setText("songlist03", " ");
  }
}
function screenbuttonsFunction() {
  onEvent("secondpagebutton01", "click", function( ) {
    setScreen("topfiftyScreen");
  });
  onEvent("listentosongs01", "click", function( ) {
    setScreen("linkScreen");
  });
  onEvent("returnbutton01", "click", function( ) {
    setScreen("tophundredScreen");
  });
  onEvent("returnbutton02", "click", function( ) {
    setScreen("topfiftyScreen");
  });
  onEvent("backbutton02", "click", function( ) {
    setScreen("tophundredScreen");
  });
}

function updateScreen2() {
  if (songnumber == 100) {
    setText("artistTopsong", trackName[99]);
  } else if (songnumber == 99) {
    setText("artistTopsong", trackName[98]);
  } else if (songnumber == 98) {
    setText("artistTopsong", trackName[97]);
  } else if (songnumber == 97) {
     setText("artistTopsong", trackName[96]);
  } else if (songnumber == 96) {
     setText("artistTopsong", trackName[95]);
  } else if (songnumber == 95) {
     setText("artistTopsong", trackName[94]);
  } else if ((songnumber == 94)) {
     setText("artistTopsong", trackName[93]);
  } else if ((songnumber == 93)) {
     setText("artistTopsong", trackName[92]);
  } else if (songnumber == 92) {
     setText("artistTopsong", trackName[91]);
  } else if (songnumber == 91) {
     setText("artistTopsong", trackName[90]);
  } else if (songnumber == 90) {
     setText("artistTopsong", trackName[89]);
  } else if (songnumber == 89) {
     setText("artistTopsong", trackName[88]);
  } else if (songnumber == 88) {
     setText("artistTopsong", trackName[87]);
  } else if (songnumber == 87) {
     setText("artistTopsong", trackName[86]);
  } else if (songnumber == 86) {
     setText("artistTopsong", trackName[85]);
  } else if (songnumber == 85) {
     setText("artistTopsong", trackName[84]);
  } else if (songnumber == 84) {
     setText("artistTopsong", trackName[83]);
  } else if (songnumber == 83) {
     setText("artistTopsong", trackName[82]);
  } else if (songnumber == 82) {
     setText("artistTopsong", trackName[81]);
  } else if (songnumber == 81) {
     setText("artistTopsong", trackName[80]);
  } else if (songnumber == 80) {
     setText("artistTopsong", trackName[79]);
  } else if (songnumber == 79) {
     setText("artistTopsong", trackName[78]);
  } else if (songnumber == 78) {
     setText("artistTopsong", trackName[77]);
  } else if (songnumber == 77) {
     setText("artistTopsong", trackName[76]);
  } else if (songnumber == 76) {
     setText("artistTopsong", trackName[75]);
  } else if (songnumber == 75) {
     setText("artistTopsong", trackName[74]);
  } else if (songnumber == 74) {
     setText("artistTopsong", trackName[73]);
  } else if (songnumber == 73) {
     setText("artistTopsong", trackName[72]);
  } else if (songnumber == 72) {
     setText("artistTopsong", trackName[71]);
  } else if (songnumber == 71) {
     setText("artistTopsong", trackName[70]);
  } else if (songnumber == 70) {
     setText("artistTopsong", trackName[69]);
  } else if (songnumber == 69) {
     setText("artistTopsong", trackName[68]);
  } else if (songnumber == 68) {
     setText("artistTopsong", trackName[67]);
  } else if (songnumber == 67) {
     setText("artistTopsong", trackName[66]);
  } else if (songnumber == 66) {
     setText("artistTopsong", trackName[65]);
  } else if (songnumber == 65) {
     setText("artistTopsong", trackName[64]);
  } else if (songnumber == 64) {
     setText("artistTopsong", trackName[63]);
  } else if (songnumber == 63) {
     setText("artistTopsong", trackName[62]);
  } else if (songnumber == 62) {
     setText("artistTopsong", trackName[61]);
  } else if (songnumber == 61) {
     setText("artistTopsong", trackName[60]);
  } else if (songnumber == 60) {
     setText("artistTopsong", trackName[59]);
  } else if (songnumber == 59) {
     setText("artistTopsong", trackName[58]);
  } else if (songnumber == 58) {
     setText("artistTopsong", trackName[57]);
  } else if (songnumber == 57) {
     setText("artistTopsong", trackName[56]);
  } else if (songnumber == 56) {
     setText("artistTopsong", trackName[55]);
  } else if (songnumber == 55) {
     setText("artistTopsong", trackName[54]);
  } else if (songnumber == 54) {
     setText("artistTopsong", trackName[53]);
  } else if (songnumber == 53) {
     setText("artistTopsong", trackName[52]);
  } else if (songnumber == 52) {
     setText("artistTopsong", trackName[51]);
  } else if (songnumber == 51) {
     setText("artistTopsong", trackName[50]);
  } else if (songnumber == 50) {
     setText("artistTopsong", trackName[49]);
  } else if (songnumber == 49) {
     setText("artistTopsong", trackName[48]);
  } else if (songnumber == 48) {
     setText("artistTopsong", trackName[47]);
  } else if (songnumber == 47) {
     setText("artistTopsong", trackName[46]);
  } else if (songnumber == 46) {
     setText("artistTopsong", trackName[45]);
  } else if (songnumber == 45) {
     setText("artistTopsong", trackName[44]);
  } else if (songnumber == 44) {
     setText("artistTopsong", trackName[43]);
  } else if (songnumber == 43) {
     setText("artistTopsong", trackName[42]);
  } else if (songnumber == 42) {
     setText("artistTopsong", trackName[41]);
  } else if (songnumber == 41) {
     setText("artistTopsong", trackName[40]);
  } else if (songnumber == 40) {
     setText("artistTopsong", trackName[39]);
  } else if (songnumber == 39) {
     setText("artistTopsong", trackName[38]);
  } else if (songnumber == 38) {
     setText("artistTopsong", trackName[37]);
  } else if (songnumber == 37) {
     setText("artistTopsong", trackName[36]);
  } else if (songnumber == 36) {
     setText("artistTopsong", trackName[35]);
  } else if (songnumber == 35) {
     setText("artistTopsong", trackName[34]);
  } else if (songnumber == 34) {
     setText("artistTopsong", trackName[33]);
  } else if (songnumber == 33) {
     setText("artistTopsong", trackName[32]);
  } else if (songnumber == 32) {
     setText("artistTopsong", trackName[31]);
  } else if (songnumber == 31) {
     setText("artistTopsong", trackName[30]);
  } else if (songnumber ==30) {
     setText("artistTopsong", trackName[29]);
  } else if (songnumber == 29) {
     setText("artistTopsong", trackName[28]);
  } else if (songnumber == 28) {
     setText("artistTopsong", trackName[27]);
  } else if ((songnumber == 27)) {
     setText("artistTopsong", trackName[26]);
  } else if (songnumber == 26) {
     setText("artistTopsong", trackName[25]);
  } else if (songnumber == 25) {
     setText("artistTopsong", trackName[24]);
  } else if (songnumber == 24) {
     setText("artistTopsong", trackName[23]);
  } else if (songnumber == 23) {
     setText("artistTopsong", trackName[22]);
  } else if (songnumber == 22) {
     setText("artistTopsong", trackName[21]);
  } else if (songnumber == 21) {
     setText("artistTopsong", trackName[20]);
  } else if (songnumber == 20) {
     setText("artistTopsong", trackName[19]);
  } else if (songnumber == 19) {
     setText("artistTopsong", trackName[18]);
  } else if (songnumber == 18) {
     setText("artistTopsong", trackName[17]);
  } else if (songnumber == 17) {
     setText("artistTopsong", trackName[16]);
  } else if (songnumber == 16) {
     setText("artistTopsong", trackName[15]);
  } else if (songnumber == 15) {
     setText("artistTopsong", trackName[14]);
  } else if (songnumber == 14) {
     setText("artistTopsong", trackName[13]);
  } else if (songnumber == 13) {
     setText("artistTopsong", trackName[12]);
  } else if (songnumber == 12) {
     setText("artistTopsong", trackName[11]);
  } else if (songnumber == 11) {
     setText("artistTopsong", trackName[10]);
  } else if (songnumber == 10) {
     setText("artistTopsong", trackName[9]);
  } else if (songnumber == 9) {
     setText("artistTopsong", trackName[8]);
  } else if (songnumber == 8) {
     setText("artistTopsong", trackName[7]);
  } else if (songnumber == 7) {
     setText("artistTopsong", trackName[6]);
  } else if (songnumber == 6) {
     setText("artistTopsong", trackName[5]);
  } else if (songnumber == 5) {
     setText("artistTopsong", trackName[4]);
  } else if (songnumber == 4) {
     setText("artistTopsong", trackName[3]);
  } else if (songnumber == 3) {
     setText("artistTopsong", trackName[2]);
  } else if (songnumber == 2) {
     setText("artistTopsong", trackName[1]);
  } else if (songnumber == 1) {
     setText("artistsSongTable", trackName[0]);
  }
}

function updateScreen3() {
  if (songnumber2 == 100) {
    setText("artistTopsong", artist [99]);
    setText("streamsLabel", numberStreams [99]);
    setText("urlTable", link [99]);
  } else if (songnumber2 == 99) {
    setText("artistTopsong", artist [98]);
    setText("streamsLabel", numberStreams [98]);
    setText("urlTable", link [98]);
  } else if (songnumber2 == 98) {
    setText("artistTopsong", artist [97]);
    setText("streamsLabel", numberStreams [97]);
    setText("urlTable", link [97]);
  } else if (songnumber2 == 97) {
    setText("artistTopsong", artist [96]);
setText("streamsLabel", numberStreams [96]);
setText("urlTable", link [96]);
  } else if (songnumber2 == 96) {
    setText("artistTopsong", artist [95]);
    setText("streamsLabel", numberStreams [95]);
    setText("urlTable", link [95]);
  } else if (songnumber2 == 95) {
    setText("artistTopsong", artist [94]);
    setText("streamsLabel", numberStreams [94]);
    setText("urlTable", link [94]);
  } else if (songnumber2 == 94) {
    setText("artistTopsong", artist [93]);
    setText("streamsLabel", numberStreams [93]);
    setText("urlTable", link [93]);
  } else if (songnumber2 == 93) {
    setText("artistTopsong", artist [92]);
    setText("streamsLabel", numberStreams [92]);
    setText("urlTable", link [92]);
  } else if (songnumber2 == 92) {
    setText("artistTopsong", artist [91]);
    setText("streamsLabel", numberStreams [91]);
    setText("urlTable", link [91]);
  } else if (songnumber2 == 91) {
    setText("artistTopsong", artist [90]);
    setText("streamsLabel", numberStreams [90]);
    setText("urlTable", link [90]);
  } else if (songnumber2 == 90) {
    setText("artistTopsong", artist [89]);
    setText("streamsLabel", numberStreams [89]);
    setText("urlTable", link [89]);
  } else if (songnumber2 == 89) {
    setText("artistTopsong", artist [88]);
    setText("streamsLabel", numberStreams [88]);
    setText("urlTable", link [88]);
  } else if (songnumber2 == 88) {
    setText("artistTopsong", artist [87]);
    setText("streamsLabel", numberStreams [87]);
    setText("urlTable", link [87]);
  } else if (songnumber2 == 87) {
    setText("artistTopsong", artist [86]);
    setText("streamsLabel", numberStreams [86]);
    setText("urlTable", link [86]);
  } else if (songnumber2 == 86) {
    setText("artistTopsong", artist [85]);
    setText("streamsLabel", numberStreams [85]);
    setText("urlTable", link [85]);
  } else if (songnumber2 == 85) {
    setText("artistTopsong", artist [84]);
    setText("streamsLabel", numberStreams [84]);
    setText("urlTable", link [84]);
  } else if (songnumber2 == 84) {
    setText("artistTopsong", artist [83]);
    setText("streamsLabel", numberStreams [83]);
    setText("urlTable", link [83]);
  } else if (songnumber2 == 83) {
    setText("artistTopsong", artist [82]);
    setText("streamsLabel", numberStreams [82]);
    setText("urlTable", link [82]);
  } else if (songnumber2 == 82) {
    setText("artistTopsong", artist [81]);
    setText("streamsLabel", numberStreams [81]);
    setText("urlTable", link [81]);
  } else if (songnumber2 == 81) {
    setText("artistTopsong", artist [80]);
    setText("streamsLabel", numberStreams [80]);
    setText("urlTable", link [80]);
  } else if (songnumber2 == 80) {
    setText("artistTopsong", artist [79]);
    setText("streamsLabel", numberStreams [79]);
    setText("urlTable", link [79]);
  } else if (songnumber2 == 79) {
    setText("artistTopsong", artist [78]);
    setText("streamsLabel", numberStreams [78]);
    setText("urlTable", link [78]);
  } else if (songnumber2 == 78) {
    setText("artistTopsong", artist [77]);
    setText("streamsLabel", numberStreams [77]);
    setText("urlTable", link [77]);
  } else if (songnumber2 == 77) {
    setText("artistTopsong", artist [76]);
    setText("streamsLabel", numberStreams [76]);
    setText("urlTable", link [76]);
  } else if (songnumber2 == 76) {
    setText("artistTopsong", artist [75]);
    setText("streamsLabel", numberStreams [75]);
    setText("urlTable", link [75]);
  } else if (songnumber2 == 75) {
    setText("artistTopsong", artist [74]);
    setText("streamsLabel", numberStreams [74]);
    setText("urlTable", link [74]);
  } else if (songnumber2 == 74) {
    setText("artistTopsong", artist [73]);
    setText("streamsLabel", numberStreams [73]);
    setText("urlTable", link [73]);
  } else if (songnumber2 == 73) {
    setText("artistTopsong", artist [72]);
    setText("streamsLabel", numberStreams [72]);
    setText("urlTable", link [72]);
  } else if (songnumber2 == 72) {
    setText("artistTopsong", artist [71]);
    setText("streamsLabel", numberStreams [71]);
    setText("urlTable", link [71]);
  } else if (songnumber2 == 71) {
    setText("artistTopsong", artist [70]);
    setText("streamsLabel", numberStreams [70]);
    setText("urlTable", link [70]);
  } else if (songnumber2 == 70) {
    setText("artistTopsong", artist [69]);
    setText("streamsLabel", numberStreams [69]);
    setText("urlTable", link [69]);
  } else if (songnumber2 == 69) {
    setText("artistTopsong", artist [68]);
    setText("streamsLabel", numberStreams [68]);
    setText("urlTable", link [68]);
  } else if (songnumber2 == 68) {
    setText("artistTopsong", artist [67]);
    setText("streamsLabel", numberStreams [67]);
    setText("urlTable", link [67]);
  } else if (songnumber2 == 67) {
    setText("artistTopsong", artist [66]);
    setText("streamsLabel", numberStreams [66]);
    setText("urlTable", link [66]);
  } else if (songnumber2 == 66) {
    setText("artistTopsong", artist [65]);
    setText("streamsLabel", numberStreams [65]);
    setText("urlTable", link [65]);
  } else if (songnumber2 == 65) {
    setText("artistTopsong", artist [64]);
    setText("streamsLabel", numberStreams [64]);
    setText("urlTable", link [64]);
  } else if (songnumber2 == 64) {
    setText("artistTopsong", artist [63]);
    setText("streamsLabel", numberStreams [63]);
    setText("urlTable", link [63]);
  } else if (songnumber2 == 63) {
    setText("artistTopsong", artist [62]);
    setText("streamsLabel", numberStreams [62]);
    setText("urlTable", link [62]);
  } else if (songnumber2 == 62) {
    setText("artistTopsong", artist [61]);
    setText("streamsLabel", numberStreams [61]);
    setText("urlTable", link [61]);
  } else if (songnumber2 == 61) {
    setText("artistTopsong", artist [60]);
    setText("streamsLabel", numberStreams [60]);
    setText("urlTable", link [60]);
  } else if (songnumber2 == 60) {
    setText("artistTopsong", artist [59]);
    setText("streamsLabel", numberStreams [59]);
    setText("urlTable", link [59]);
  } else if (songnumber2 == 59) {
    setText("artistTopsong", artist [58]);
    setText("streamsLabel", numberStreams [58]);
    setText("urlTable", link [58]);
  } else if (songnumber2 == 58) {
    setText("artistTopsong", artist [57]);
    setText("streamsLabel", numberStreams [57]);
    setText("urlTable", link [57]);
  } else if (songnumber2 == 57) {
    setText("artistTopsong", artist [56]);
    setText("streamsLabel", numberStreams [56]);
    setText("urlTable", link [56]);
  } else if (songnumber2 == 56) {
    setText("artistTopsong", artist [55]);
    setText("streamsLabel", numberStreams [55]);
    setText("urlTable", link [55]);
  } else if (songnumber2 == 55) {
    setText("artistTopsong", artist [54]);
    setText("streamsLabel", numberStreams [54]);
    setText("urlTable", link [54]);
  } else if (songnumber2 == 54) {
    setText("artistTopsong", artist [53]);
    setText("streamsLabel", numberStreams [53]);
    setText("urlTable", link [53]);
  } else if (songnumber2 == 53) {
    setText("artistTopsong", artist [52]);
    setText("streamsLabel", numberStreams [52]);
    setText("urlTable", link [52]);
  } else if (songnumber2 == 52) {
    setText("artistTopsong", artist [51]);
    setText("streamsLabel", numberStreams [51]);
    setText("urlTable", link [51]);
  } else if (songnumber2 == 51) {
    setText("artistTopsong", artist [50]);
    setText("streamsLabel", numberStreams [50]);
    setText("urlTable", link [50]);
  } else if (songnumber2 == 50) {
    setText("artistTopsong", artist [49]);
    setText("streamsLabel", numberStreams [49]);
    setText("urlTable", link [49]);
  } else if (songnumber2 == 49) {
    setText("artistTopsong", artist [48]);
    setText("streamsLabel", numberStreams [48]);
    setText("urlTable", link [48]);
  } else if (songnumber2 == 48) {
    setText("artistTopsong", artist [47]);
    setText("streamsLabel", numberStreams [47]);
    setText("urlTable", link [47]);
  } else if (songnumber2 == 47) {
    setText("artistTopsong", artist [46]);
    setText("streamsLabel", numberStreams [46]);
    setText("urlTable", link [46]);
  } else if (songnumber2 == 46) {
    setText("artistTopsong", artist [45]);
    setText("streamsLabel", numberStreams [45]);
    setText("urlTable", link [45]);
  } else if (songnumber2 == 45) {
    setText("artistTopsong", artist [44]);
    setText("streamsLabel", numberStreams [44]);
    setText("urlTable", link [44]);
  } else if (songnumber2 == 44) {
    setText("artistTopsong", artist [43]);
    setText("streamsLabel", numberStreams [43]);
    setText("urlTable", link [43]);
  } else if (songnumber2 == 43) {
    setText("artistTopsong", artist [42]);
    setText("streamsLabel", numberStreams [42]);
    setText("urlTable", link [42]);
  } else if (songnumber2 == 42) {
    setText("artistTopsong", artist [41]);
    setText("streamsLabel", numberStreams [41]);
    setText("urlTable", link [41]);
  } else if (songnumber2 == 41) {
    setText("artistTopsong", artist [40]);
    setText("streamsLabel", numberStreams [40]);
    setText("urlTable", link [40]);
  } else if (songnumber2 == 40) {
    setText("artistTopsong", artist [39]);
    setText("streamsLabel", numberStreams [39]);
    setText("urlTable", link [39]);
  } else if (songnumber2 == 39) {
    setText("artistTopsong", artist [38]);
    setText("streamsLabel", numberStreams [38]);
    setText("urlTable", link [38]);
  } else if (songnumber2 == 38) {
    setText("artistTopsong", artist [37]);
    setText("streamsLabel", numberStreams [37]);
    setText("urlTable", link [37]);
  } else if (songnumber2 == 37) {
    setText("artistTopsong", artist [36]);
    setText("streamsLabel", numberStreams [36]);
    setText("urlTable", link [36]);
  } else if (songnumber2 == 36) {
    setText("artistTopsong", artist [35]);
    setText("streamsLabel", numberStreams [35]);
    setText("urlTable", link [35]);
  } else if (songnumber2 == 35) {
    setText("artistTopsong", artist [34]);
    setText("streamsLabel", numberStreams [34]);
    setText("urlTable", link [34]);
  } else if (songnumber2 == 34) {
    setText("artistTopsong", artist [33]);
    setText("streamsLabel", numberStreams [33]);
    setText("urlTable", link [33]);
  } else if (songnumber2 == 33) {
    setText("artistTopsong", artist [32]);
setText("streamsLabel", numberStreams [32]);
setText("urlTable", link [32]);
  } else if (songnumber2 == 32) {
    setText("artistTopsong", artist [31]);
    setText("streamsLabel", numberStreams [31]);
    setText("urlTable", link [31]);
  } else if (songnumber2 == 31) {
    setText("artistTopsong", artist [30]);
    setText("streamsLabel", numberStreams [30]);
    setText("urlTable", link [30]);
  } else if (songnumber2 == 30) {
    setText("artistTopsong", artist [29]);
    setText("streamsLabel", numberStreams [29]);
    setText("urlTable", link [29]);
  } else if (songnumber2 == 29) {
    setText("artistTopsong", artist [28]);
    setText("streamsLabel", numberStreams [28]);
    setText("urlTable", link [28]);
  } else if (songnumber2 == 28) {
    setText("artistTopsong", artist [27]);
    setText("streamsLabel", numberStreams [27]);
    setText("urlTable", link [27]);
  } else if (songnumber2 == 27) {
    setText("artistTopsong", artist [26]);
setText("streamsLabel", numberStreams [26]);
setText("urlTable", link [26]);
  } else if (songnumber2 == 26) {
    setText("artistTopsong", artist [25]);
setText("streamsLabel", numberStreams [25]);
setText("urlTable", link [25]);
  } else if (songnumber2 == 25) {
    setText("artistTopsong", artist [24]);
    setText("streamsLabel", numberStreams [24]);
    setText("urlTable", link [24]);
  } else if (songnumber2 == 24) {
    setText("artistTopsong", artist [23]);
    setText("streamsLabel", numberStreams [23]);
    setText("urlTable", link [23]);
  } else if (songnumber2 == 23) {
    setText("artistTopsong", artist [22]);
    setText("streamsLabel", numberStreams [22]);
    setText("urlTable", link [22]);
  } else if (songnumber2 == 22) {
    setText("artistTopsong", artist [21]);
    setText("streamsLabel", numberStreams [21]);
    setText("urlTable", link [21]);
  } else if (songnumber2 == 21) {
    setText("artistTopsong", artist [20]);
    setText("streamsLabel", numberStreams [20]);
    setText("urlTable", link [20]);
  } else if (songnumber2 == 20) {
    setText("artistTopsong", artist [19]);
    setText("streamsLabel", numberStreams [19]);
    setText("urlTable", link [19]);
  } else if (songnumber2 == 19) {
    setText("artistTopsong", artist [18]);
    setText("streamsLabel", numberStreams [18]);
    setText("urlTable", link [18]);
  } else if ((songnumber2 == 18)) {
    setText("artistTopsong", artist [17]);
    setText("streamsLabel", numberStreams [17]);
    setText("urlTable", link [17]);
  } else if (songnumber2 == 17) {
    setText("artistTopsong", artist [16]);
    setText("streamsLabel", numberStreams [16]);
    setText("urlTable", link [16]);
  } else if (songnumber2 == 16) {
    setText("artistTopsong", artist [15]);
    setText("streamsLabel", numberStreams [15]);
    setText("urlTable", link [15]);
  } else if (songnumber2 == 15) {
    setText("artistTopsong", artist [14]);
    setText("streamsLabel", numberStreams [14]);
    setText("urlTable", link [14]);
  } else if (songnumber2 == 14) {
    setText("artistTopsong", artist [13]);
    setText("streamsLabel", numberStreams [13]);
    setText("urlTable", link [13]);
  } else if (songnumber2 == 13) {
    setText("artistTopsong", artist [12]);
    setText("streamsLabel", numberStreams [12]);
    setText("urlTable", link [12]);
  } else if (songnumber2 == 12) {
    setText("artistTopsong", artist [11]);
    setText("streamsLabel", numberStreams [11]);
    setText("urlTable", link [11]);
  } else if (songnumber2 == 11) {
    setText("artistTopsong", artist [10]);
    setText("streamsLabel", numberStreams [10]);
    setText("urlTable", link [10]);
  } else if (songnumber2 == 10) {
    setText("artistTopsong", artist [9]);
    setText("streamsLabel", numberStreams [9]);
    setText("urlTable", link [9]);
  } else if (songnumber2 == 9) {
    setText("artistTopsong", artist [8]);
    setText("streamsLabel", numberStreams [8]);
    setText("urlTable", link [8]);
  } else if (songnumber2 == 8) {
    setText("artistTopsong", artist [7]);
    setText("streamsLabel", numberStreams [7]);
    setText("urlTable", link [7]);
  } else if (songnumber2 == 7) {
    setText("artistTopsong", artist [6]);
    setText("streamsLabel", numberStreams [6]);
    setText("urlTable", link [6]);
  } else if (songnumber2 == 6) {
    setText("artistTopsong", artist [5]);
    setText("streamsLabel", numberStreams [5]);
    setText("urlTable", link [5]);
  } else if (songnumber2 == 5) {
    setText("artistTopsong", artist [4]);
    setText("streamsLabel", numberStreams [4]);
    setText("urlTable", link [4]);
  } else if (songnumber2 == 4) {
    setText("artistTopsong", artist [3]);
    setText("streamsLabel", numberStreams [3]);
    setText("urlTable", link [3]);
  } else if (songnumber2 == 3) {
    setText("artistTopsong", artist [2]);
    setText("streamsLabel", numberStreams [2]);
    setText("urlTable", link [2]);
  } else if (songnumber2 == 2) {
    setText("artistTopsong", artist [1]);
    setText("streamsLabel", numberStreams [1]);
    setText("urlTable", link [1]);
  } else if (songnumber2 == 1) {
    setText("artistTopsong", artist [0]);
    setText("streamsLabel", numberStreams [0]);
    setText("urlTable", link [0]);
  } else if (songnumber2 == 0) {
    setText("artistTopsong", "ha");
    setText("streamsLabel", "ha");
    setText("urlTable", "ha, undefined");
  }
}
