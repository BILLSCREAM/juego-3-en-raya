juego-3-en-raya
===============
<!DOCTYPE html>
Tobar Briones Marvin Andres<br>
Acosta Alvarado Nexar Jesus<br>
Tercer nivel "A"<BR>
Programacion Orientada a la web<BR> 
<CENTER><h1> TRES EN RAYA</h1></CENTER>

<html>
<head>        
	<title>Tres En Raya</title>
 
	<style>
		.cuadrito{width:60px;height:60px;border:solid 4px;float:left;font-size:25px;text-align:center;}
		#div_contenedor{width:204px;border:solid 0px;margin:auto;}
		li{font-size:28px;width:850px;margin-bottom:20px;}
	</style>
 
	<script>	
		var turno = "X";	
		var turno2= "O";
		var bandera=1;
		var ban=false;
		var opciones = new Array(9);//arreglo para las pocisiones del juego tres en raya
		function marcar(id){		
			// Para los turnos
			var celda = document.getElementById(id);
			if(bandera%2!=0 && opciones[id]!=0){
				celda.value = turno;
				document.getElementById("div_turno").innerHTML="Turno del jugador : "+turno2;celda.style.background="lightblue";
				opciones[id]=1;
			}else if(bandera%2==0 && opciones[id]!=1){
				celda.value=turno2;
				document.getElementById("div_turno").innerHTML="Turno del jugador : "+turno;celda.style.background="lightgreen";
				opciones[id]=0;
			}
			bandera++;
			jugadorX();
			jugadorO();
		}	
 
		function jugadorX(){
				//para el jugador X
				if(opciones[1]==1 && opciones[2]==1 && opciones[3]==1){//primer linea horizontal
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[4]==1 && opciones[5]==1 && opciones[6]==1){//segunda linea horizontal
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[7]==1 && opciones[8]==1 && opciones[9]==1){//tercera linea horizontal
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[1]==1 && opciones[5]==1 &&opciones[9]==1){//primera linea diagonal
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[3]==1 && opciones[5]==1 &&opciones[7]==1){//segunda linea diagonal
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[1]==1 && opciones[4]==1 &&opciones[7]==1){//primer linea vertical izquierda
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[2]==1 && opciones[5]==1 &&opciones[8]==1){//linea de enmedio vertical
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}else if(opciones[3]==1 && opciones[6]==1 &&opciones[9]==1){//tercer linea vertical derecha
					alert("Felicidades Jugador " +turno+ " Ganaste");
				}
                }
                // para el jugador 2
               function jugadorO(){
				if(opciones[1]==0 && opciones[2]==0 && opciones[3]==0){//primer linea horizontal
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[4]==0 && opciones[5]==0 && opciones[6]==0){//segunda linea horizontal
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[7]==0 && opciones[8]==0 && opciones[9]==0){//tercera linea horizontal
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[1]==0 && opciones[5]==0 &&opciones[9]==0){//primera linea diagonal
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[3]==0 && opciones[5]==0 &&opciones[7]==0){//segunda linea diagonal
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[1]==0 && opciones[4]==0 &&opciones[7]==0){//primer linea vertical izquierda
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[2]==0 && opciones[5]==0 &&opciones[8]==0){//linea de enmedio vertical
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}else if(opciones[3]==0 && opciones[6]==0 &&opciones[9]==0){//tercer linea vertical derecha
					alert("Felicidades Jugador " +turno2+ " Ganaste");
				}
               }
                // funcion para reiniciar el juego
        
	 function reiniciar(){

               	location.reload(opciones);
               }
 
	</script
 
</head>    
<body bgcolor="red">


	<!-- Tablero -->
	<div id="div_contenedor"/>		
		<input type="text" class="cuadrito" value="" id="1" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="2" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="3" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="4" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="5" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="6" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="7" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="8" readonly onclick="marcar(this.id)">
		<input type="text" class="cuadrito" value="" id="9" readonly onclick="marcar(this.id)">
 
		<div id="div_turno">Turno del jugador: X</div>
		<button onclick="reiniciar()" >Reiniciar Juego</>
		

	</div>
 
	
 
</body>
</html>
