import streamlit as st
import random

# Función para generar un ejercicio de cinemática
def generar_ejercicio():
    v0 = random.randint(5, 20)  # Velocidad inicial (m/s)
    t = random.randint(1, 10)   # Tiempo (s)
    a = random.randint(1, 5)    # Aceleración (m/s²)
    
    # Fórmula: d = v0 * t + (1/2) * a * t²
    d_correcta = v0 * t + 0.5 * a * t**2
    
    return v0, t, a, d_correcta

# Generar un ejercicio
v0, t, a, d_correcta = generar_ejercicio()

# Interfaz de Streamlit
st.title("Ejercicios de Cinemática")
st.write(f"Un objeto parte de una velocidad inicial de **{v0} m/s** y tiene una aceleración de **{a} m/s²** durante **{t} segundos**.")
st.write("¿Cuál es la distancia recorrida (d) en metros?")

# Input del usuario
respuesta_usuario = st.number_input("Introduce tu respuesta (d):", min_value=0.0)

# Botón para verificar respuesta
if st.button("Verificar respuesta"):
    if respuesta_usuario == d_correcta:
        st.success("¡Correcto! La distancia es efectivamente {:.2f} metros.".format(d_correcta))
    else:
        st.error("Incorrecto. La distancia correcta es {:.2f} metros.".format(d_correcta))

# Botón para generar un nuevo ejercicio
if st.button("Generar nuevo ejercicio"):
    v0, t, a, d_correcta = generar_ejercicio()
    st.experimental_rerun()
