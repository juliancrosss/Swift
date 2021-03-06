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
        
            teamScore += 3
            
        }else{
        
            teamScore += 1
        }
        
    }
    
    print(teamScore)
    
*En una if declaracion, la condifional debe ser un Boolean expression, esto significa que el codigo como "if score { ... } es un error , no una implicita comparacion a cero. "Se puede utilizar if y let  juntos para  trabajar con valores que pudieran faltar."Estos valores se representan como opcionales .Un valor opcional o bien que contiene un valor o contiene nil para indicar que falta un valor. Escriba un signo de interrogación (?) Después de que el tipo de un valor para marcar el valor como opcional "."*

    var optionalString: String? = "Hello"
    print(optionalString == nil)

    var optionalName: String? = "Julian Cruz"
    var greeting = "Hello!"
    if let name = optionalName{
        greeting = "Hello, \(name)"
    }
    
*"Si el valor opcional es nil, "El condicional es falso y el código entre llaves se omite"."De lo contrario, el valor es opcional sin envolver y asignado a la constante después de let, lo que hace que el valor sin envolver disponible dentro del bloque de código.""Switches soportan cualquier tipo de datos y una amplia variedad de operaciones de comparación, que no se limitan a los números enteros y las pruebas para la igualdad."*

    let vegetable = "red pepper"
    switch vegetable{
    case "celery":
        print("Add some raisins and make ants on a log.")
    case "cucumber", "watercress":
        print("That would make a good tea sandwich.")
    case let x where x.hasSuffix("pepper"):
        print("Is it a spicy \(x)?")
    default:
        print("Everything tastes good in soup.")
    }
    
*Observe cómo let puede ser utilizado en un modelo para asignar el valor que hacía juego con la parte de un patrón a una constante."*

*Después de ejecutar el código dentro de la caja del switch que hacía juego, el programa sale de la sentencia switch. Ejecución no continúa a la siguiente caso, lo que no hay necesidad de romper explícitamente del switch al final del código de cada caso.*

#for-in manejo de diccionarios

*Se utiliza for-in para iterar sobre los elementos de un diccionario, proporcionando un par de nombres a utilizar para cada par clave-valor. Los diccionarios son una colección desordenada, por lo que sus claves y valores se repiten a lo largo de un orden arbitrario ".*

    let interestingNumbers = [
    "Prime": [2, 3, 5, 7, 11, 13],
    "Fibonacci": [1, 1, 2, 3, 5, 8],
    "Square": [1, 4, 9, 16, 25]
    ]

    var largest = 0
    for(kind, numbers) in interestingNumbers{
        for number in numbers{
            if number > largest{
                largest = number
            }
        }
    }
    print(largest)
    
#While

*Use while para repetir un bloque de código hasta que una condición cambia. El estado de un bucle puede estar en el extremo en su lugar, asegurando que el bucle se ejecuta al menos una vez ".*

    var n = 2

    while n < 100{
        n = n * 2
    }
    print(n)



    var m = 2
    repeat{
        m = m * 2
    }while m < 100
    
*Usted puede mantener un índice en un bucle, ya sea mediante el uso de .. <para hacer una serie de índices o escribiendo una explícita inicialización, condición, y la subasta. Estos dos bucles hacen lo mismo "*

    var firstForLoop = 0
    for i in 0..<4{
        firstForLoop += i
    }
    print(firstForLoop)
    
*Ejemplo2*
    
    var secondForLoop = 0
    for var i = 0; i < 4; ++i{
        secondForLoop += i
    }
    print(secondForLoop)
    
*"Use .. < para hacer un rango que omite su valor superior, y use ... para hacer un rango que incluye ambos valores.*

#Funcciones y Cierres

*"Use func para declarar una función. Llame a una función siguiendo su nombre con una lista de argumentos entre paréntesis. Use -> para separar los nombres de los parámetros y tipos del tipo de retorno de la función*

    func greet(name: String, day: String)->String{
        return "Hello \(name), today is \(day)."
    }

    greet("Julian Cruz",day: "Wednesday")

#Tupla
    
*"Use una tupla para hacer un valor compuesto -por ejemplo"."Para retornar multiples valores de una función.Los elementos de una tupla se pueden referir por nombre o por número."*

    func calculateStatistics(scores: [Int]) -> (min: Int, max: Int, sum: Int){
        var min = scores[0]
        var max = scores[0]
        var sum = 0

        for score in scores{
            if score > max{
                max = score
            }else if score < min {
                min = score
            }
        sum += score
        }
    return (min, max, sum)
    }

    let statistics = calculateStatistics([5, 3, 100, 3, 9])

    print(statistics.sum)
    print(statistics.2)
    
*Las funciones también pueden tomar un número variable de argumentos, a su recogida en una matriz.*

    func sumOf(numbers: Int...) -> Int{
        var sum = 0 
        for number in numbers{
            sum += number
        }
    return sum
    }
    
    sumOf()
    sumOf(42, 597, 12)
    
*"Las funciones se pueden anidadas. Funciones anidadas tienen acceso a las variables que fueron declaradas en la función externa. Puede utilizar funciones anidadas para organizar el código en una función que es largo o complejo*

    func returnFifteen() -> Int {
        var y = 10 
        func add(){
            y += 5
        }
        add()
        return y 
    }
    returnFifteen()
    
*"Las funciones son un tipo de primera clase. Esto significa que una función puede devolver otra función como su valor"*

    func makeIncrementer() -> ((Int) -> Int){
        func addOne(number: Int) -> Int {
            return 1 + number
        }
        return addOne
    }
    var increment = makeIncrementer()
    increment(7)



    





