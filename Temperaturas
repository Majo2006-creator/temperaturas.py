# ------------------------------
# Función para calcular temperaturas promedio
# ------------------------------

def calcular_promedios(temperaturas):
    """
    Calcula el promedio de temperaturas por ciudad.
    
    Parámetros:
        temperaturas (dict): Diccionario con el nombre de la ciudad como clave
                             y una lista de listas (semanas) con temperaturas como valor.
                             
                             Ejemplo:
                             {
                                "Quito": [[20, 22, 21], [19, 20, 21], [22, 21, 20], [19, 20, 18]],
                                "Guayaquil": [[28, 30, 29], [27, 28, 30], [29, 30, 31], [28, 27, 29]],
                                "Cuenca": [[18, 19, 20], [17, 18, 19], [19, 18, 20], [18, 17, 19]]
                             }
    
    Retorna:
        dict: Diccionario con el promedio de temperaturas por ciudad.
    """
    
    promedios = {}
    
    for ciudad, semanas in temperaturas.items():
        suma = 0
        contador = 0
        
        for semana in semanas:
            suma += sum(semana)     # sumamos las temperaturas de la semana
            contador += len(semana) # contamos los días registrados
        
        promedio = suma / contador if contador > 0 else 0
        promedios[ciudad] = promedio
    
    return promedios


# ------------------------------
# Pruebas de la función
# ------------------------------

# Datos de ejemplo: 3 ciudades, 4 semanas, con 3 días cada semana
datos_temperaturas = {
    "Quito": [[20, 22, 21], [19, 20, 21], [22, 21, 20], [19, 20, 18]],
    "Guayaquil": [[28, 30, 29], [27, 28, 30], [29, 30, 31], [28, 27, 29]],
    "Cuenca": [[18, 19, 20], [17, 18, 19], [19, 18, 20], [18, 17, 19]]
}

# Calcular promedios
resultado = calcular_promedios(datos_temperaturas)

# Mostrar resultados
print("Promedio de temperaturas por ciudad:")
for ciudad, promedio in resultado.items():
    print(f"{ciudad}: {promedio:.2f} °C")
