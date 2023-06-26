print('***Miscelanea de ejercicios python***')
print('Ejercicio de listas y tuplas 3. Actividad')
#Suma de elementos: Escribe una función que tome una lista de números como entrada y devuelva la suma de todos los elementos de la lista.

def suma_de_elementos():
    print("SUMA DE ELEMENTOS")
    numero = int(input("¿Cuántos valores va a introducir? "))

    if numero <= 0:
        print("¡Imposible!")
    else:
        suma = 0
        for i in range(1, numero + 1):
            valor = float(input(f"Escriba el número {i}: "))
            suma = suma + valor
        print(f"La suma de los números que ha escrito es {suma}")

#Escribe una función que tome una lista de números como entrada y calcule el promedio de todos los elementos de la lista.

def Promedio_de_valores():
    print('Promedio de valores')
    print('Escribe 4 numeros y el programa saca el promedio de ellos')
    lista=[ ]
    suma=0
    for i in range(4):
      numero=int(input('Ingrese el primer valor: '))
      lista.insert (i,numero)
      suma=suma+lista[i]
    print(f'lista los numeros ingresados es: {lista} y el promedio es', (suma/4))
  
#Escribe una función que tome una lista como entrada y elimine todos los elementos duplicados, dejando solo una aparición de cada elemento en la lista final.

def eliminacion_duplicados():
  numeros=[3,6,7,8,2,3,4,5,67,8,2,3,5,6,7]
  print('Los numeros registrados son: \n',numeros)
  unicos=[]
  copias=list(numeros)
  for n in copias:
    if n not in unicos:
      unicos.append(n)
    else:
      numeros.remove(n)  
  print('Los numeros  unicos son: \n',unicos)
#Escribe una función que tome una lista de números como entrada y la ordene de menor a mayor. No utilices la función de ordenación incorporada en Python.
def ordenar_lista():
  lista=[]  
  ingresos=int(input('Cuantos desean ingresar: '))
  n=0
  while n<ingresos:
    print('Ingrese numero',n+1)
    nom=input()
    lista.append(nom)
    n+=1
  lista.sort()
  print(lista)

#Escribe una función que tome una lista de palabras como entrada y devuelva la palabra más larga de la lista. Si hay varias palabras con la misma longitud máxima, devuelve la primera que aparezca en la lista.
def palabra_mas_larga():
  frase=input('Escribe una oración: ')
  palabra=frase.split()
  larga=palabra[0]
  for i in range(1, len(palabra)):
    if len(larga) < len(palabra[i]):
        larga = palabra[i]
  print('La palagra mas grande de la oracion es : ',larga)

#Escribe una función que tome una tupla de números como entrada y devuelva el producto de todos los elementos de la tupla.
def producto_de_elemento():
  tupla=([1,'Perros'],[2, 'Gatos'],[3, 'Vacas'],[4,'Chivas'])
  
  Saber_dato=input('Que dato tiene la tupla del programa, oprime la letra  T: ')
  if Saber_dato=='T':
    print(tupla)
  else:
    print('No seleccionó la letra correcta')

#Escribe una función que tome una tupla de números como entrada y devuelva el valor máximo y mínimo de la tupla.
def Mayor_y_menor_elemento():
  tupla=(1,2,3,5,6,7,8,5,9,5,3)
  print(tupla)
  maximo=tupla[0]
  minimo=tupla[0]
  for i in tupla:
    if(i>maximo):
      maximo=i
    elif(i<minimo):
      minimo=i
  print('El maximo numero es: {}'.format(maximo))
  print('El minimo numero es: {}'.format(minimo))

#Escribe una función que tome una tupla como entrada y cuente cuántas veces aparece cada elemento en la tupla, devolviendo un diccionario con los elementos como claves y las ocurrencias como valores.

def Contar_ocurrencias():
  tupla=('Manzanas', 'Peras', 'Fresas','Fresas','Peras')
  print(tupla)

  frecuencia={}
  for i in tupla:
    if i in frecuencia:
      frecuencia[i] +=1
    else:
      frecuencia[i]=1
  print('El contenido que se replite con frecuencia es :', frecuencia)

#Escribe una función que tome una tupla y un elemento como entrada, y devuelva una lista con todos los índices en los que aparece el elemento en la tupla.

def Buscar_índices():
  tupla=(12,13,14,15,16,17,18,19,20)
  print(tupla) 
  lista=input('Escribe nueva serie de numeros: ')
  print(lista)
  nueva_lista=list(zip(tupla,lista))
  print(nueva_lista)
  
def Separar_elementos():
  lista=input('Ingrese una cadena de palabras a la tupla: ') 
  lista=[lista]
  tupla = tuple(lista)
  print(tupla)
  lista=tupla
  
  for palabra in lista:
    if lista[0].lower()=='a':
      print(palabra)
    elif lista[0].lower()!='a':
      print(palabra)

def contar_palabras():
  frase=input('Escribe una frase: ')
  #Para quitar los caracteres que no se van a utilizar para la realizacion del conteo.
  quitar = ",;:\n'"
  for caracter in quitar:
    frase=frase.replace(caracter," ")
  #lo primero es convertir la frase por si tiene palabras en mayuscula con el comando 'texto.lower'
  frase=frase.lower()  
  #Con la siguiente funcion limpiamo las palabras para poder generar el conteo
  palabras=frase.split(" ")
  #ahora contadoremos la cantidad de palabras que se encuentren durante la frase por medio de un dicionario.
  diccionario_frecuencia={}
  for palabra in palabras:
    if palabra in diccionario_frecuencia:
     diccionario_frecuencia[palabra]+=1
    else:
      diccionario_frecuencia[palabra] = 1
  for palabra in diccionario_frecuencia:
    frecuencia=diccionario_frecuencia[palabra]
    print(f'La palabra: "{palabra}" tiene una frecuencia de: {frecuencia}')

  
  
  
  
  
seleccion=(input('Ejercicios de la actividad 4\n 01. Suma de elementos\n 02. Promedio de valores\n 03. Eliminacion de duplicados\n 04. Ordenar lista\n 05. Palabra mas larga\n 06. Producto de elementos\n 07. Mayor y menor elemento\n 08. Contar ocurrencias\n 09. Buscar indices\n 10.Escribe una función que tome una tupla de cadenas como entrada y devuelva dos tuplas separadas: una con todas las cadenas que empiezan con una vocal y otra con las que no.\n 11. Escribe una función que tome una lista de palabras como entrada y devuelva un diccionario que cuente cuántas veces aparece cada palabra en la lista.\n 99. Para salir ___________\n Ejercicio a desarrollar: '))

while seleccion!= '99':
  if seleccion == '01':
    suma_de_elementos()
  elif seleccion =='02':
    Promedio_de_valores()
  elif seleccion =='03':
    eliminacion_duplicados()
  elif seleccion =='04':
    ordenar_lista()
  elif seleccion =='05':
    palabra_mas_larga()
  elif seleccion =='06':
    producto_de_elemento()
  elif seleccion =='07':
    Mayor_y_menor_elemento()
  elif seleccion =='08':
    Contar_ocurrencias()
  elif seleccion =='09':
    Buscar_índices()
  elif seleccion =='10':
    Separar_elementos()
  elif seleccion =='11':
    contar_palabras()
  else:
    print('Seleccion incorrecta')     
  selccion=(input('Ejercicios de la actividad 4\n 01. Suma de elementos\n 02. Promedio de valores\n 03. Eliminacion de duplicados\n 04. Ordenar lista\n 05. Palabra mas larga\n 06. Producto de elementos\n 07. Mayor y menor elemento\n 08. Contar ocurrencias\n 09. Buscar indices\n 99. 10.Escribe una función que tome una tupla de cadenas como entrada y devuelva dos tuplas separadas: una con todas las cadenas que empiezan con una vocal y otra con las que no.\n 11. Escribe una función que tome una lista de palabras como entrada y devuelva un diccionario que cuente cuántas veces aparece cada palabra en la lista. \n Para salir___________\n Ejercicio a desarrollar: '))
  print('Finalizado el programa')
