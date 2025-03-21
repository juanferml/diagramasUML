# diagramasUML

'''mermaid
	classDiagram
	
	    class Habitacion {
	        -int numero
	        -string tipo
	        -bool ocupada
	        +Habitacion(int, string)
	        +~Habitacion()
	        +int getNumero()
	        +string getTipo()
	        +bool estaOcupada()
	        +void ocupar()
	        +void desocupar()
	    }
	
	    class Cliente {
	        -int id
	        -string nombre
	        +Cliente(int, string)
	        +~Cliente()
	        +int getId()
	        +string getNombre()
	    }
	
	    class Hotel {
	        -string nombre
	        -vector~Habitacion~ habitaciones
	        -vector~Cliente~ clientes
	        +Hotel(string)
	        +~Hotel()
	        +void agregarHabitacion(int, string)
	        +void registrarCliente(Cliente* cliente)
	        +void mostrarInfo()
	    }
	
	    Hotel *-- Habitacion
	    Hotel *-- Cliente
'''	
'''mermaid
	classDiagram
	
		class Auto {
			-string placa
			-string modelo
			-bool disponible
			+Auto(string, string)
			+~Auto()
			+string getPlaca()
			+string getModelo()
			+bool estaDisponible()
			+void rentar()
			+void devolver()
		}
		
		class Cliente {
			-int id
			-string nombre
			+Cliente(int, string)
			+~Cliente()
			+int getId()
		}
	
		class Contrato{
			-Cliente* cliente
			-Auto* autoRentado
			-int dias
			+Contrato(Cliente*, Auto*, int)
			+~Contrato()
		}
		
		class AgenciaRenta{
			-string nombre
			-vector~Auto*~
			-vector~Cliente*~
			+AgenciaRenta(string)
			+~AgenciaRenta()
			+void agregarAuto()
			+void agregarCliente()
			+void mostrarInfo()
		}
		
		Auto --> Contrato 
	    Cliente --> Contrato 
		Auto o-- AgenciaRenta 
	    Cliente o-- AgenciaRenta 
'''
