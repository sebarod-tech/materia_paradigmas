import tkinter as tk

def calcular(operacion):
    try:
        num1 = float(entrada1.get())
        num2 = float(entrada2.get())

        if operacion == "sumar":
            resultado = num1 + num2

        elif operacion == "restar":
            resultado = num1 - num2

        elif operacion == "multiplicar":
            resultado = num1 * num2

        elif operacion == "dividir":
            if num2 == 0:
                etiqueta_resultado.config(text="Error: división por cero")
                return
            resultado = num1 / num2

        if resultado.is_integer():
            resultado = int(resultado)

        etiqueta_resultado.config(text="Resultado: " + str(resultado))

    except:
        etiqueta_resultado.config(text="Error: ingresar números válidos")

def limpiar():
    entrada1.delete(0, tk.END)
    entrada2.delete(0, tk.END)
    etiqueta_resultado.config(text="Resultado: ")

ventana = tk.Tk()
ventana.title("Mini Calculadora")

tk.Label(ventana, text="Calculadora", font=("Arial", 16)).pack()

tk.Label(ventana, text="Número 1:").pack()
entrada1 = tk.Entry(ventana)
entrada1.pack()

tk.Label(ventana, text="Número 2:").pack()
entrada2 = tk.Entry(ventana)
entrada2.pack()

tk.Button(ventana, text="Sumar", command=lambda: calcular("sumar")).pack()
tk.Button(ventana, text="Restar", command=lambda: calcular("restar")).pack()
tk.Button(ventana, text="Multiplicar", command=lambda: calcular("multiplicar")).pack()
tk.Button(ventana, text="Dividir", command=lambda: calcular("dividir")).pack()

tk.Button(ventana, text="Limpiar", command=limpiar).pack()

etiqueta_resultado = tk.Label(ventana, text="Resultado: ", font=("Arial", 16))
etiqueta_resultado.pack()

ventana.mainloop()
