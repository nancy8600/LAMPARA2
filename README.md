LAMPARA2
========

PRENDER LED SIN POTENCIOMETRO
#define maxleds 8 //creamos la variable maxleds de 8 elementos
 int led[maxleds] = {2,3,4,5,6,7,8,9}; //creamos un vector de enteros para los pines a utilizar
void setup () //Esta función se ejecutará una única vez después de que se conecte la placa Arduino a la fuente de alimentación, o cuando se pulse el botón de reinicio de la placa.
 {
 for (int i=0;i<maxleds;i++)
 pinMode(led[i],OUTPUT); //configura los pines de los LEDS como salida.
 }
// se ejecuta consecutivamente, permitiéndole al programa variar y responder.
 void loop()
 {
 for (int i=0;i<=maxleds;i++) // ciclo for para cambiar de salida derecha
 {
 prender(led[i],100); //llama a la funcion prender, pasando como parametro el arreglo y el tiempo intensidad y velocidad del encendido y apagado de los LED al ir.
 apagar(led[i],100); //llama a la funcion apagar, pasando como parametro el arreglo y el tiempo.
 }
for (int i=maxleds;i>=0;i--) // ciclo for para cambiar de salida izquierda
 { 
prender(led[i],100);  //llama a la funcion prender ingresando los parametros intencidad y velocidad del encendido y apagado de los LED al regresar
apagar(led[i],100);   //llama a la funcion apagar ingresando los parametros}
 }
}
void prender(int i, int t) //Declaramos la funcion para enceder el led
 {
 digitalWrite(i, HIGH);//led esta encendido
 delay(t); //tiempo de encendido
 }
void apagar(int i, int t) //Declaramos LA funcion para apagar el led
 {
 digitalWrite(i, LOW); //led esta apagado
 
 delay(t); //tiempo de apagado
 }
