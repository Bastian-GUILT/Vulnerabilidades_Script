# Vulnerabilidades_Script

class Vulnerabilidad: #Clase padre
    def __init__(self, nombre, severidad, descripcion):
        self.nombre = nombre
        self.severidad = severidad
        self.descripcion = descripcion
        
    def mostrar_info(self): #METODO PARA MOSTRAR LA INFORRMACION DE LOS PROGRAMAS
        print(f'''Nombre: {self.nombre}, Severidad: {self.severidad} , Descripcion: {self.descripcion}.''')

    def recomendar_acciones(self):

        
#Estructura logica if/elif/else => Segun el nivel de severidad del programa 
        if self.severidad == 'Critica':
            recomendacion = f'Aplicar parches de seguridad inmediatamente y revisar sistemas afectados.'
        elif self.severidad == 'Alta':
            recomendacion = f'Realizar una auditoría de seguridad y aplicar medidas correctivas lo antes posible.'
        elif self.severidad == 'Media':
            recomendacion = f'Monitorizar la actividad del sistema y planificar la aplicación de parches.'
        elif self.severidad == 'Baja':
            recomendacion = f'Mantener bajo observación y revisar en el próximo ciclo de actualización.'

            #Algo nuevo que aprendi haciendo este ejercicio es que se puede asignar una variable en la estructura if/else/elif,
            #en este caso recomendacion en funcion de self.severidad

        print(f'Acción recomendada: {recomendacion}')


        

        


    
#Tres objetos con la clase vulnerabilidad y sus parametros, 'Nombre', 'Severidad', 'Descripcion'
d1 = Vulnerabilidad('SQL Injection', 'Alta', 'Permite la ejecucion de consultas SQL NO autorizadas')
d2 = Vulnerabilidad('XSS', 'Media', 'Permite la ejecución de scripts en el navegador del usuario')
d3 = Vulnerabilidad('Desbordamiento de Buffer', 'Critica', 'Permite la ejecución arbitraria de código')

#Lista de los objetos guardadas en una variable
registro_vulnerabilidades = [d1, d2, d3]


#Una iteracion para la lista
for registro in registro_vulnerabilidades:
    registro.mostrar_info() #llamamos a los metodos mediante el objeto 'registro'
    registro.recomendar_acciones()



        
