# Swift

*El lenguaje de programacion para iOS , OS X y watchOS*

##Imprimiendo con Swift

    print("Hola, Mundo!")

*Esta linea de codigo es un total programa , no es necesario importar librerias, no es necesario escribir punto y coma al final de la setencia*

#Simples Valores

    let = para hacer constantes

    var = para hacer variables

*Ejemplo  Una variable o constante  debe tener el mismo tipo de dato*

    var myVariable = 42

    myVariable = 50

    let myConstant = 42 

##Especificando explicitamente  tipo de dato de una variable o una constante -obligatorio-

    let implicitInteger = 70

    let implicitDouble = 70.0

    let explicitDouble: Double = 70

    let explicitFloat: Float = 70

*Los valores implícitamente no se convierten  a otro tipo, Si necesita para convertir un valor a un tipo diferente, hacer explícita una instancia al tipo deseado.*

    let label = "The width is "

    let width = 94

    let widthLabel = label + String(width)

*Convirtiendo la constante width a un String y se almacena en la constante widthLabel*

*Hay una manera aún más sencilla para incluir valores en Strings: Escriba el valor entre paréntesis, y escribir una barra invertida (\) antes del paréntesis. Por ejemplo:"*

    let apples = 3
    
    let oranges= 5
    
    let applesSummary = "I have \(apples) apples."
    
    let fruitSummary = "I have \(apples + oranges) pieces of fruit."
    
#Arrays y Diccionarios 

*Crear matrices "Arrays" y diccionarios utilizando corchetes ([]), y acceder a sus elementos escribiendo el índice o clave entre corchetes. Se permite una coma después del último elemento ".*

*Array*

    var shoppingList = ["catfish", "water", "tulips", "blue paint"]
    
    shoppingList[1] = "bottle of water"
    
*Diccionarios*

    var occupations = ["Malcolm": "Captain", "Kaylee": "Mechanic",]
    
    occupations["Jayne"] = "Public Relations"
    
*"Para crear una matriz "Array"  o diccionario vacía, utilice la sintaxis inicializador."*

    let emptyArray = [String]()
    
    let emptyDictionary = [String: Float]()
    
*"Si la información de tipo se puede inferir, puede escribir una matriz vacía como [] y un diccionario vacío como [:] -. Por ejemplo, cuando se establece un nuevo valor para una variable o pasar un argumento a una función"*

*Array Vacia*

    shoppingList = []
  
*Diccionario Vacio*
    
    occupations = [:]
    
#Flujos de Control

*"Usar if y switch para hacer los condicionales" y for-in, for, while y repeat-while para hace bucles.Parentesis alrededor de la condicional o bucle variables son opcionales. LLaves alrededor del cuerpo son requeridos*

    let individualScores = [75, 43, 103, 87, 12]
    
    var teamScore = 0
    
    for score in individualScores {
    
        if score > 50{
        
            teamscore += 3
        }else{
        
            teamscore += 1
        }
        
    }
    
    print(teamScore)

    

    





