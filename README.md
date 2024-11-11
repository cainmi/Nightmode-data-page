# Nightmode-data-page
repository for Nightmode a data page project that can be opened offline






current (copy paste)



<!--



data:text/html;charset=utf-8,
<!DOCTYPE html>
<html>

<head>
    <title>Notepad (Nightmode)</title>
    <style>
        canvas {
            border: 1px solid white;
        }

        .scrollable-place {
            height: 10px;
        }
    </style>
</head>

<body style=" font-family: DejaVu;font-weight:bold;background:1E1E1E;color:FFFFFF;font-size:1rem;line-height:1.4;max-width:80rem;margin:0 auto;padding:2rem;" spellcheck="true" javascript="true">
    <script src="https://code.jquery.com/jquery-3.1.0.js">jquery-3-1-0</script>
    <script src="https://releases.jquery.com/git/jquery-git.js">jquery-git</script>        

    
    <div id="exploits"> 
        <h1>Exploits</h1>

        <a href="(function(){ promt: " https://webcache.googleusercontent.com/search?q=cache: then your link"})()">builder</a>
        
        <br>
        
        <a href="javascript:(function()var popup = document.createElement(%27div%27);  popup.style.cssText = position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(0,0,0,0.8); z-index: 9999;;  var iframe = document.createElement(%27iframe%27);  iframe.style.cssText = %27position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); width: 90%; height: 90%;%27;  iframe.src = %27https://fffkfd.interstellar.furkanpowered.com/%27;  iframe.setAttribute(%27frameborder%27,0);  iframe.setAttribute(%27scrolling%27,%27yes%27);  iframe.id = %272beat-iframe%27;  popup.appendChild(iframe);  document.body.appendChild(popup);  var close = document.createElement(%27div%27);  close.style.cssText = %27position:absolute;top:5px;right:5px;color:white;cursor:pointer;%27;  close.innerHTML = %27X%27;  popup.appendChild(close);  close.addEventListener(%27click%27, function() {        document.body.removeChild(popup);    });  var back = document.createElement(%27div%27);  back.style.cssText = %27position:absolute;top:5px;left:5px;color:white;cursor:pointer;%27;  back.innerHTML = %27<%27;  popup.appendChild(back);  back.addEventListener(%27click%27, function() {    iframe.contentWindow.history.back();});  var forward = document.createElement(%27div%27);  forward.style.cssText = %27position:absolute;top:5px;left:25px;color:white;cursor:pointer;%27;  forward.innerHTML = %27>%27;  popup.appendChild(forward);  forward.addEventListener(%27click%27, function() {    iframe.contentWindow.history.forward();});})();">popout dodge</a>
        
        <br>
        
        <a href="javascript:(function(){  var popup = document.createElement(%27div%27);  popup.style.cssText = %27position: fixed; top: 0; left: 0; right: 0; bottom: 0; background: rgba(0,0,0,0.8); z-index: 9999;%27;  var iframe = document.createElement(%27iframe%27);  iframe.style.cssText = %27position: absolute; top: 50%; left: 50%; transform: translate(-50%,-50%); width: 90%; height: 90%;%27;  iframe.src = %27https://picture-day.photo-frame.com/%27;  iframe.setAttribute(%27frameborder%27,0);  iframe.setAttribute(%27scrolling%27,%27yes%27);  iframe.id = %272beat-iframe%27;  popup.appendChild(iframe);  document.body.appendChild(popup);  var close = document.createElement(%27div%27);  close.style.cssText = %27position:absolute;top:5px;right:5px;color:white;cursor:pointer;%27;  close.innerHTML = %27X%27;  popup.appendChild(close);  close.addEventListener(%27click%27, function() {        document.body.removeChild(popup);    });  var back = document.createElement(%27div%27);  back.style.cssText = %27position:absolute;top:5px;left:5px;color:white;cursor:pointer;%27;  back.innerHTML = %27<%27;  popup.appendChild(back);  back.addEventListener(%27click%27, function() {    iframe.contentWindow.history.back();});  var forward = document.createElement(%27div%27);  forward.style.cssText = %27position:absolute;top:5px;left:25px;color:white;cursor:pointer;%27;  forward.innerHTML = %27>%27;  popup.appendChild(forward);  forward.addEventListener(%27click%27, function() {    iframe.contentWindow.history.forward();});})();">popout</a>
        
        <br>
    </div>

    <div id="utility">
        <h1>utility</h1>
        <br>
        <a href="javascript:document.body.contentEditable='true'; document.designMode='on'; void 0">design Mode on </a>
        <br>
        <a href="javascript:document.body.contentEditable='false'; document.designMode='off'; void 0">design Mode off</a>
        <br>
    </div>

    <h1>Snake game</h1>
    <p>lock the scrolling to play</p>

    <p class="scrollable-place">
        <button onclick="disableScroll()">
            Disable Scrolling</button>
        <button onclick="enableScroll()">
            Enable Scrolling</button>
    </p>

    <script>
        function disableScroll() {
            scrollTop =
                window.pageYOffset ||
                document.documentElement.scrollTop;
            scrollLeft =
                window.pageXOffset ||
                document.documentElement.scrollLeft,

                window.onscroll = function () {
                    window.scrollTo(scrollLeft, scrollTop);
                };
        }

        function enableScroll() {
            window.onscroll = function () { };
        }
    </script>

    <div id="game_space">
        <canvas width="400px" height="400px" id="game" </canvas>

            <script>
                var
                    canvas = document.getElementById('game');
                var context = canvas.getContext('2d');
                var grid = 16; var count = 0;
                var snake = {
                    x: 160, y: 160,
                    dx: grid, dy: 0,
                    cells: [],
                    maxCells: 4
                };
                var apple = { x: 320, y: 320 };
                function getRandomInt(min, max) { return Math.floor(Math.random() * (max - min)) + min }
                function loop() {
                    requestAnimationFrame(loop);
                    if (++count < 4) { return; } count = 0; context.clearRect(0, 0, canvas.width, canvas.height);
                    snake.x += snake.dx; snake.y += snake.dy;
                    if (snake.x < 0) { snake.x = canvas.width - grid; }
                    else if (snake.x >= canvas.width) { snake.x = 0; }
                    if (snake.y < 0) { snake.y = canvas.height - grid; }
                    else if (snake.y >= canvas.height) { snake.y = 0; }
                    snake.cells.unshift({ x: snake.x, y: snake.y });
                    if (snake.cells.length > snake.maxCells) { snake.cells.pop(); }
                    context.fillStyle = 'red'; context.fillRect(apple.x, apple.y, grid - 1, grid - 1);
                    context.fillStyle = 'green';
                    snake.cells.forEach(function (cell, index) {
                        context.fillRect(cell.x, cell.y, grid - 1, grid - 1);
                        if (cell.x === apple.x && cell.y === apple.y) {
                            snake.maxCells++;
                            apple.x = getRandomInt(0, 25) * grid;
                            apple.y = getRandomInt(0, 25) * grid;
                        }
                        for (var i = index + 1; i < snake.cells.length; i++) {
                            if (cell.x === snake.cells[i].x && cell.y === snake.cells[i].y) {
                                snake.x = 160;
                                snake.y = 160;
                                snake.cells = [];
                                snake.maxCells = 4;
                                snake.dx = grid;
                                snake.dy = 0;
                                apple.x = getRandomInt(0, 25) * grid;
                                apple.y = getRandomInt(0, 25) * grid;
                            }
                        }
                    });
                }
                document.addEventListener('keydown', function (e) {
                    if (e.which === 37 && snake.dx === 0) {
                        snake.dx = -grid; snake.dy = 0;
                    }
                    else if (e.which === 38 && snake.dy === 0) {
                        snake.dy = -grid;
                        snake.dx = 0;
                    }
                    else if (e.which === 39 && snake.dx === 0) {
                        snake.dx = grid;
                        snake.dy = 0;
                    }
                    else if (e.which === 40 && snake.dy === 0) {
                        snake.dy = grid;
                        snake.dx = 0;
                    }
                });
                requestAnimationFrame(loop);
            </script>
    </div>

    <div id="gamezone">
    
        <h1> old javascript bookmarklet games</h1>
        
        <br>
        
        <a href='javascript:(function(){var js=document.body.appendChild(document.createElement("script"));js.onerror=function(){alert("Sorry, the script could not be loaded.")};js.src="https://rawgit.com/Krazete/bookmarklets/master/lupire.js"})();'>pinball</a>
        
        <br>
        
        <a href="javascript:var s=document.createElement('script');s.type='text/javascript';s.onerror=function(e){alert('Failed to load the script. The site\'s Content Security Policy might be blocking it. Feel free to try again.');};document.body.appendChild(s);s.src='https://blog.roysolberg.com/js/dom2.min.js';void(0);">DOMII.js </a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
    
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>
                
        <a href=""></a>    
        
        <br>

    </div>

</body>

</html>

-->
