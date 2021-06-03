fprintf('\n Método de Newton Rapson Modificado\n\n');
   funcion=input('Ingrese la funcion f(x) : ','s');
   d1=input('Ingrese la derivada de funcion f(x) : ','s');
     d2=input('Ingrese la segunda derivada de funcion f(x) : ','s');
        xi=input('Ingrese el valor inicial de x : ');
     e=input('Ingrese el porciento del error : ');
   E_a=1000;
  c=1;
 x=xi;
while E_a>e 
 g=eval(funcion);
  h=eval(d1);
   k=eval(d2);
     j=x-(g*h)/(h^(2)-(g*k));
   E_a=abs((j-x)/j*100);
  x=j;
 c=c+1;
end
 fprintf('\nLa raiz exacta es: %d',j)
  fprintf('\nNumero de iteraciones: %d',c);
