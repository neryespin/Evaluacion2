print("# Evaluación Unidad II Programación Web-Nery Espinoza\n")
# Función para agregar compra a la lista
def agregar_compra(compras, total_gastado):
    # Solicito al usuario ingresar el monto de la compra como un número entero.
    monto = int(input("Ingresa el monto de la compra: "))
    # Agrego el monto a la lista de compras y actualizo el total gastado.
    compras.append(monto)
    total_gastado += monto
    # Imprimo un mensaje indicando que la compra se ha agregado correctamente.
    print(f"¡Compra agregada correctamente!")
    return total_gastado

# Función para mostrar las compras
def mostrar_compras(compras):
    # Verifico si no hay compras registradas y muestro un mensaje informativo.
    if not compras:
        print("No hay compras registradas hasta el momento.")
    else:
        # Muestro todas las compras realizadas numeradas.
        print("Compras realizadas:")
        for idx, monto in enumerate(compras, start=1):
            print(f"Compra {idx}: ${monto}")

# Función para mostrar el total gastado
def mostrar_total(total_gastado):
    # Muestro el total gastado hasta el momento.
    print(f"Total gastado: ${total_gastado}")

# Función principal del programa
def main():
    # Inicializo las listas y variables necesarias.
    compras = []
    total_gastado = 0

    while True:
        # Muestro el menú al usuario.
        print("\nMenú:")
        print("1. Agregar compra")
        print("2. Mostrar compras")
        print("3. Mostrar total gastado")
        print("4. Salir")
        opcion = input("Seleccione una opción: ")

        if opcion == "1":
            # Llamo a la función agregar_compra para manejar la opción de agregar compra.
            total_gastado = agregar_compra(compras, total_gastado)
        elif opcion == "2":
            # Llamo a la función mostrar_compras para manejar la opción de mostrar compras.
            mostrar_compras(compras)
        elif opcion == "3":
            # Llamo a la función mostrar_total para manejar la opción de mostrar total gastado.
            mostrar_total(total_gastado)
        elif opcion == "4":
            # Imprimo un mensaje de despedida y salgo del bucle si el usuario elige salir.
            print("¡Hasta luego!")
            break
        else:
            # Imprimo un mensaje indicando que la opción ingresada no es válida.
            print("Opción ingresada no válida, intenta nuevamente.")

# Llamo a la función main() para mostrar el menú.
main()