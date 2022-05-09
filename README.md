# get-geolocation-js
Menginginkan dirimu untuk mengambil kordinat lokasimu

<!DOCTYPE html>
<html>
<body onload="getLocation()">
 
<input type="text" class="form-control" name="lokasi" id="lokasi">
 
<script>
var x = document.getElementById("lokasi");
 
function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(showPosition);
  } else { 
    x.innerHTML = "Geolokasi tidak didukung oleh browser ini.";
  }
}
 
function showPosition(position) {
  x.value = position.coords.latitude + "," + position.coords.longitude;
}
</script>

</body>
</html>
