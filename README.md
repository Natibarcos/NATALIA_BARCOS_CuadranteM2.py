##Encontrar el cudrante (Sistema Cartesiano)

##En este bloque determinamos el tipo de cuadrante


def determinar_cuadrante(x,y):
    
    if x > 0 and y >0:
        return "Cuadrante I" ##Ingresa en esta opcion cuando ambos valores son positivos (+ , +)
        
    elif x < 0 and y > 0:        
        return "Cuadrante II" ##Ingresa en esta opcion cuando el valor es negativo y el otro positivo (- , +)
        
    elif x < 0 and y < 0:    
        return "Cuadrante III" ##Ingresa en esta opcion cuando ambos valores son negativos (- , -)
        
    elif x > 0 and y < 0:
        return "Cuadrante IV" ##Ingresa en esta opcion cuando el valor es positivo y el otro negativo (+ , -)
        
    else:
        return "El punto esta en el origen (Coordenadas 0,0)." 

    
##Solicitu de coordenadas (Valor numerico que ingresa el usuario)

try:
    x = float(input("Ingrese el vañor de x :"))
    y = float(input("Ingrese el vañor de y :"))
    
    #Verifica que ninguna coordenada sea 0
    if x==0 or y==0:
        print("Ninguna coordenada debe ser igual a 0.") #Saldra esta leyenda si ingresas uno de los valores en 0
        
    else:
        cuadrante = determinar_cuadrante(x, y)
        print(f"El punto se encuentra en {cuadrante}.")

##Esta linea lanza una excepcion cuando el usuario agrega un valor no valido (Ejemplo una letra o un signo en x o y)

except ValueError:
    print("Por favor, ingrese un valor numerico valido para las coordenadas")
