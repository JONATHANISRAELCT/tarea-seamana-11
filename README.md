# tarea-seamana-11
def bubble_sort(fila):
    n = len(fila)
    for i in range(n):
        for j in range(0, n - i - 1):
            if fila[j] > fila[j + 1]:
                fila[j], fila[j + 1] = fila[j + 1], fila[j]

def ordenar_fila(matriz, fila_indice):
    # Copiar la fila para evitar modificar la matriz original directamente
    fila_a_ordenar = matriz[fila_indice][:]

    # Ordenar la fila utilizando Bubble Sort
    bubble_sort(fila_a_ordenar)

    # Mostrar la matriz original
    print("Matriz original:")
    for fila in matriz:
        print(fila)

    # Mostrar la matriz con la fila ordenada
    print("Matriz con la fila ordenada:")
    matriz[fila_indice] = fila_a_ordenar
    for (fila) in matriz:
        print(fila)


# Ejemplo de matriz 3x3
matriz = [
    [30, 10, 20],
    [60, 50, 40],
    [90, 70, 80]
]

# Especifica el índice de la fila que deseas ordenar
fila_indice = 1

ordenar_fila(matriz, fila_indice)
