<html lang="in">
<head>
				<title>Judul halaman</title>
				
								<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>
								<script>
$(document).ready(function(){
  $("#ambil").click(function(){
    $("#bckgrnd").fadeOut(100);
    $("#hasil").fadeIn(1000);
    $("#ambil").fadeOut(100);
    
  });
});
</script>

<style type="text/css">
				
				.bckgrnd{
								background:url(https://raw.githubusercontent.com/webanakmilenial/Twibbom/main/tujuhbelasan.jpg);
								width:80%;
								background-size:100%;
								height:50%;
								margin:auto;
								display:block;
								
								
								}

.clip{

width:30%;

margin:auto;
display:block;


clip-path: circle(50% at 50% 50%);
border-style:solid;
border-color:red;

}

.head{
				position:fixed;
				top:0;
				left:0;
				right:0;
				background-color:#bb1f27; 		
}

.span{
				width:27px;
				height:22px;
				color:white;
				background-color:#bb1f27;
				margin-left:10px; 
				display:flex;
				justify-content:space-between;
				flex-direction:column;
				margin-top:-30px;
				border:none; 
 }

.span span{
				background-color:white;
				width:17px;
				height:3px;
				display:block;
				margin-top:0px;
				
				margin-left:5px;
}

.nama{
				text-align:center;
				font-family:cursive,"Brush Script MT";
	     color:white;
				margin-top:-21px;
}

  .bawah{
				position:fixed;
				bottom:0;
				left:0;
				right:0;
				background-color:#bb1f27;
				padding:5px;
}

.copy{
				text-align:center;
				font-size:12px;
				color:white;
}

.ambil{
				border:none;
				text-decoration:none;
				background:white;
				color:#bb1f27;
				width:30%;
				margin:auto;
				display:block;
				font-size:10px;
				padding:10px;
				border-radius:3px;
				border-style:solid;
				border-color:#bb1f27;
}


.hasil{
				background:url(https://raw.githubusercontent.com/webanakmilenial/Twibbom/main/tujuhbelasan.jpg);
								width:80%;
								background-size:100%;
								height:100%;
								margin:auto;
								display:block;
				       display:none;
				}

.canvas{
   width:30%;

margin:auto;
display:block;


clip-path: circle(50% at 50% 50%);
border-style:solid;
border-color:red;
}


</style>


				
</head>
<body>
				<div class="head">
								<button class="span" id="span">
								<span></span>
								<span></span>
								<span></span>
								</button>
								<h2 class="nama">Twibbon</h2>
				</div>
				<br><br><br><br>
				
				<div class="bckgrnd" id="bckgrnd">
								
<div>
				<br><br><br>
    <video autoplay="true" id="video-webcam" class="clip">
       
    </video>
    
     <br><br><br><br>
</div>
</div>
<br><br>
<button onclick="takeSnapshot()" class="ambil" id="ambil">Ambil Gambar</button>




<div class="hasil" id="hasil">
<br><br><br>
				<canvas id="canvas" class="canvas"></canvas>
<br><br><br><br>
</div>


<br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br><br>





<div class="bawah">
								<p class="copy">XII TITL 01 Web Deisgn Copyright © 2021</p>
				</div>



<script type="text/javascript">
    // elemen untuk menyeleksi video, dan variable #video-webcam harus sama seperti pada atribut id="video-webcam"
    var video = document.querySelector("#video-webcam");

    // Berfungsi untuk meminta izin terlebih dahulu kepada user
    navigator.getUserMedia = navigator.getUserMedia || navigator.webkitGetUserMedia || navigator.mozGetUserMedia || navigator.msGetUserMedia || navigator.oGetUserMedia;

    // jika user memberikan izin pada program webcam panduancode
    if (navigator.getUserMedia) {
        // run fungsi handleVideo, dan videoError jika user tidak memberikan izin
        navigator.getUserMedia({ video: true }, handleVideo, videoError);
    }

    // fungsi ini hanya akan di run jika user telah memberi izin kepada program webcam
    function handleVideo(stream) {
        video.srcObject = stream;
    }

    // jika user tidak memberikan izin maka fungsi ini akan di run
    function videoError(e) {
        // do something
        
    }








function takeSnapshot() {
    // Ini berfungsi untuk membuat gambar
    var img = document.createElement('img');
    var context;

    // ini berfungsi untuk mengambil ukuran video
    var width = video.offsetWidth
            , height = video.offsetHeight;

    // Ini berfungsi untuk membuat elemen canvas
    canvas = document.getElementById('canvas');
    canvas.width = width;
    canvas.height = height;

    // mengambil gambar dari video dan memasukannya kedalam canvas
    context = canvas.getContext('2d');
    context.drawImage(video, 0, 0, width, height);

    // gambar yang dimasukan kedalam canvas di render ke dalam format gambar png
    img.src = canvas.toDataURL('image/png');
    document.body.appendChild(img);
}


</script>

</body>
</html>
