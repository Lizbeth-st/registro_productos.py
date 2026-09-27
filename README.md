# Programa: Registro de productos de una tienda

productos = []

print("====================================")
print("     REGISTRO DE PRODUCTOS")
print("====================================")

cantidad = int(input("¿Cuántos productos desea registrar? "))

# Agregar productos a la lista
for i in range(cantidad):
    print("\nProducto", i + 1)

    nombre = input("Ingrese el nombre del producto: ")
    precio = float(input("Ingrese el precio: "))

    producto = {
        "nombre": nombre,
        "precio": precio
    }

    productos.append(producto)

# Mostrar productos registrados
print("\n====================================")
print("       PRODUCTOS REGISTRADOS")
print("====================================")

for producto in productos:
    print("Producto:", producto["nombre"])
    print("Precio: $", producto["precio"])
    print("------------------------------------")

# Buscar un producto
buscar = input("\nIngrese el nombre de un producto para buscarlo: ")

encontrado = False

for producto in productos:
    if producto["nombre"].lower() == buscar.lower():
        print("\nProducto encontrado:")
        print("Nombre:", producto["nombre"])
        print("Precio: $", producto["precio"])
        encontrado = True

if not encontrado:
    print("\nEl producto no se encuentra registrado.")

# Mostrar cantidad total
print("\nTotal de productos registrados:", len(productos))
