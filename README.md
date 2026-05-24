# Fase5
# Matriz con los recursos y horas trabajadas de lunes a viernes
# Formato: [Nombre, Lunes, Martes, Miércoles, Jueves, Viernes]

recursos = [
    ["Carlos", 8, 9, 8, 10, 9],
    ["Ana", 7, 8, 8, 7, 8],
    ["Luis", 9, 10, 9, 8, 10],
    ["María", 6, 7, 8, 7, 6]
]

# Función para calcular total de horas y clasificación
def calcular_horas(horas):
    total = sum(horas)

    if total > 40:
        clasificacion = "Sobretiempo"
    else:
        clasificacion = "Horario Estándar"

    return total, clasificacion


# Recorrer la matriz e imprimir resultados
for recurso in recursos:
    nombre = recurso[0]
    horas = recurso[1:]

    total, clasificacion = calcular_horas(horas)

    print("Recurso:", nombre)
    print("Total de horas semanales:", total)
    print("Clasificación:", clasificacion)
    print("-" * 40)
