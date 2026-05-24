# trabajo 5 
# Diego Cotrino 
# Grupo 213022_371
equipo = [
    ["Marcela Supanteve",    9, 8, 10, 9, 8],
    ["Adrian Cotrino",  8, 8,  8, 8, 8],
    ["Katia Herrera", 10, 9, 10, 9, 9],
    ["Jaime Pulido", 7, 8,  6, 7, 8],
]

UMBRAL_HORAS = 40

def calcular_y_clasificar(recurso):
    """Calcula el total de horas semanales y clasifica la jornada."""
    nombre = recurso[0]
    horas_diarias = recurso[1:]
    total_horas = sum(horas_diarias)
    clasificacion = "Sobretiempo" if total_horas > UMBRAL_HORAS else "Horario Estándar"
    return nombre, total_horas, clasificacion

# Salida
print(f"{'Recurso':<20} {'Total Horas':>12} {'Clasificación':<20}")
print("-" * 55)

for persona in equipo:
    nombre, total, clasificacion = calcular_y_clasificar(persona)
    print(f"{nombre:<20} {total:>12} {clasificacion:<20}")
