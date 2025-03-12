@startuml

class Paciente {
    - ci: String
    - nombre: String
    - apellidos: String
    - fechaNacimiento: Date
    - sexo: String
    - peso: Double
    - estatura: Double
    - direccion: String
    + buscarDatos()
    + obtenerEstaturaMaxima(): List<String>
    + contarPacientesDengueFemeninos(): int
    + obtenerDatosOrdenadosPorNombre(): List<Paciente>
    + obtenerDatosOrdenadosPorPeso(): List<Paciente>
    + agregarPaciente()
    + eliminarPaciente()
    + modificarPaciente()
}

class Imagen {
    - nombreArchivo: String
    - fechaTomada: Date
    - tipoImagen: String
    - comentariosDoctor: String
    + agregarImagen()
    + eliminarImagen()
    + modificarImagen()
}

class Enfermedad {
    - nombreEnfermedad: String
    - fecha: Date
    - tratamiento: String
    + agregarEnfermedad()
    + eliminarEnfermedad()
    + modificarEnfermedad()
}

Paciente "1" -- "0..*" Imagen : tiene >
Paciente "1" -- "0..*" Enfermedad : padece >

@enduml
