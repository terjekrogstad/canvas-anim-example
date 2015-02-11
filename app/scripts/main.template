(function(){
    'use strict';

    //Get canvas element
    var canvas = document.getElementById( 'myCanvas' );

    //Get 2D context API
    var ctx = canvas.getContext( '2d' );

    


    var objects = [];

    var gravity = 0.05;
    var airforce = 0.01;



    var render = function(){

        canvas.height = canvas.height;

        var o = {
            x : canvas.width/2,
            y : canvas.height/2,
            height : 10,
            width : 10,
            velocityY : (Math.random() * 8 - 4),
            velocityX : (Math.random() * 8 - 4),
            color : {
                r : Math.round( Math.random() * 255 ),
                g : Math.round( Math.random() * 255 ),
                b : Math.round( Math.random() * 255 )
            }
        };

        objects[objects.length] = o;

        for( var i=0; i<objects.length; i++ ){
            var ot = objects[i];

            ot.velocityY -= gravity;
            ot.velocityX -= airforce;
            
            ot.x += ot.velocityX;
            ot.y -= ot.velocityY;

            ctx.fillStyle = 'rgb(' + ot.color.r + ',' + ot.color.g + ',' + ot.color.b + ')';
            
            ctx.fillRect( ot.x, ot.y, ot.width, ot.height );

        }

        

    };

    setInterval( render, 1000/24 );
})();