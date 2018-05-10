# Ejercicios-
Deber de ejercios de metodo de metodos numericos

% Método de bisección
clear, clc
h=input('INGRESE LA FUNCION: ');
f=inline(h);
a=input('Ingrese limite inferior del intervalo: ');
b=input('Ingrese limite superior del intervalo: ');
tol=input('Ingrese la tolerancia deseada: ');
 
c=0; n=0; MEP=(b-a)/2;
fprintf('\t n \t\ta \t\t c\t\t b \t\t MEP\n');
 
while (MEP>tol)
    c=(a+b)/2;
    disp([n,a,c,b,MEP])
    if(f(a)*f(c)<0)
        b=c;
    else
        a=c;
    end
    MEP=(b-a)/2;
    n=n+1;
end
fprintf('Raiz encontrada con la tolerancia de %f:\n\t%f\n', tol, c)

