
#! encoding: UTF-8
import time
import timeit
import moduloPI
start=time.time()
l=[]  

def error (intervalo, veces , umbral):
    p = 0.0
    fallos = 0.0
    PI = moduloPI.PI
    for j in range (veces):
        pi = moduloPI.aproximacion(intervalo)
        error=abs(pi-PI)
        if (error > umbral):
           fallos= fallos + 1
    return (fallos/veces) * 100

if __name__=="__main__":
   import sys
   if (len(sys.argv)==4):
     e1=int(sys.argv[1])
     e2=int(sys.argv[2])
     e3=float(sys.argv[3])
   else:
     print"Debe escribir tres valores, como no lo ha hecho, ahora se ejecutará con los valores 6 ,6 , 0.2"
     e1=6
     e2=6
     e3=0.2
   pi=error(e1,e2,e3)
   print "El porcentaje de error es de: %.35f" %pi
   finish=time.time()-start
   print "El tiempo que tarda es: %14.13f" %finish
   l=l+[finish]
   print "Introduzca el nombre del fichero en el que va a almacenar los resultados dados:"
   nombre_fichero= raw_input();
   f=open(nombre_fichero, 'w')
   f.write('El tiempo que ha tardado en ejecutarse el programa es:')
   f.write(str(l[0]) + '\n')
   f.close()