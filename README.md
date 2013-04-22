# Kiwix, a Javascript HTML5 Audio library

Kiwix is a small but powerful Javascript library that allows you to easily take advantage of the new HTML5 audio element. It tries to degrade properly on non-modern browsers.

    var mySound = new Kiwix.sound( "/sounds/myfile", {
        formats: [ "ogg", "mp3", "acc" ]
    });
  
    mySound.play()
        .fadeIn()
        .loop()
        .bind( "timeupdate", function() {
            var timer = Kiwix.toTimer( this.getTime() );
            document.getElementById( "timer" ).innerHTML = timer;
        });



