# AdvancedAI
IA capaz de : ✅ Resolver ecuaciones matemáticas ✅ Analizar datos y generar gráficos ✅ Crear documentos PDF
import sympy as sp
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from fpdf import FPDF

class AdvancedAI:
    def __init__(self):
        print("IA avanzada iniciada")
    
    def solve_math(self, equation):
        """Resuelve ecuaciones matemáticas simbólicas"""
        try:
            expr = sp.sympify(equation)
            solution = sp.solve(expr)
            return solution
        except Exception as e:
            return f"Error resolviendo la ecuación: {e}"
    
    def analyze_data(self, data):
        """Analiza y grafica datos de entrada en un DataFrame"""
        df = pd.DataFrame(data)
        df.describe().to_string()
        df.plot()
        plt.show()
    
    def generate_pdf(self, text, filename="output.pdf"):
        """Genera un PDF con el texto dado"""
        pdf = FPDF()
        pdf.add_page()
        pdf.set_font("Arial", size=12)
        pdf.multi_cell(190, 10, text)
        pdf.output(filename)
        return f"PDF generado: {filename}"
    
    def generate_image(self, prompt):
        """Generará imágenes con IA (requiere integración con API como DALL·E o Stable Diffusion)"""
        return "Funcionalidad de generación de imágenes en desarrollo"
    
    def generate_video(self, script):
        """Generará videos (requiere herramientas avanzadas como RunwayML o MoviePy)"""
        return "Funcionalidad de generación de videos en desarrollo"

# Ejemplo de uso
aio = AdvancedAI()
print(io.solve_math("x**2 - 4"))  # Resolver x^2 - 4 = 0
print(io.generate_pdf("Este es un documento de prueba"))
