# MEDICAL SYSTEM

Para utilizarlo completamente con las dependecias se encuentra en este link, donde se encontrara el .Jar
https://github.com/ItsRedm4n/MedicalSystem/tree/master/dist

Al iniciar te pedira login el cual es el siguiente
usuario: hms
contraseña: admin

Librerias que se utilizan en el proyecto
mysql-connector-j-8.0.33.jar
rs2xml.jar
jdk 17

#PSEUDOCODIGO
// Definir la clase MedicalSystem
clase MedicalSystem:
    // Método principal para iniciar la aplicación
    método principal():
        // Crear una instancia del sistema médico
        sistemaMedico = MedicalSystem()
        // Autenticar al usuario
        sistemaMedico.autenticarUsuario()
        // Mostrar menú principal
        sistemaMedico.mostrarMenuPrincipal()

    // Método para autenticar al usuario
    método autenticarUsuario():
        // Mostrar formulario de inicio de sesión
        mostrarFormularioInicioSesion()
        // Validar credenciales del usuario
        si credenciales son válidas:
            // Permitir acceso al sistema
        sino:
            // Mostrar mensaje de error y volver a solicitar credenciales

    // Método para mostrar el menú principal
    método mostrarMenuPrincipal():
        // Mostrar opciones del menú principal (añadir paciente, añadir doctor, etc.)
        mostrarOpcionesMenuPrincipal()
        // Esperar selección del usuario
        opcionSeleccionada = obtenerOpcionMenuPrincipalSeleccionada()
        // Ejecutar la función correspondiente a la opción seleccionada
        ejecutarFuncionMenuPrincipal(opcionSeleccionada)

    // Método para añadir un paciente
    método añadirPaciente():
        // Mostrar formulario para agregar un nuevo paciente
        mostrarFormularioAgregarPaciente()
        // Obtener datos del paciente ingresados por el usuario
        datosPaciente = obtenerDatosPacienteIngresados()
        // Validar datos del paciente
        si datosPaciente son válidos:
            // Agregar paciente a la base de datos
            agregarPacienteABaseDeDatos(datosPaciente)
            // Mostrar mensaje de éxito
        sino:
            // Mostrar mensaje de error

    // Método para añadir un doctor
    método añadirDoctor():
        // Mostrar formulario para agregar un nuevo doctor
        mostrarFormularioAgregarDoctor()
        // Obtener datos del doctor ingresados por el usuario
        datosDoctor = obtenerDatosDoctorIngresados()
        // Validar datos del doctor
        si datosDoctor son válidos:
            // Agregar doctor a la base de datos
            agregarDoctorABaseDeDatos(datosDoctor)
            // Mostrar mensaje de éxito
        sino:
            // Mostrar mensaje de error

    // Métodos similares para añadir diagnóstico, historial médico completo, actualizar historial, programar cita, etc.

    // Método para cerrar sesión
    método cerrarSesion():
        // Limpiar datos de sesión
        // Volver al formulario de inicio de sesión

// Función principal para iniciar el sistema médico
función principal():
    // Crear una instancia del sistema médico
    sistemaMedico = MedicalSystem()
    // Iniciar el sistema médico
    sistemaMedico.principal()


# DIAGRAMA DE FLUJO
![Diagrama de flujo](https://github.com/ItsRedm4n/MedicalSystem/assets/104162679/1010151f-637b-4d10-b979-f53ed0208fe8)



#CREACION DE MYSQL USANDO COMMAND LINE CLIENT
create database project;
use project;
create table patient(patientID varchar(10)primary key, name varchar(100),contactNumber varchar(10),age varchar(3),gender varchar(10), bloodGroup varchar(100),anyMajorDisease varchar(500), address varchar (100));
CREATE TABLE patientreport (patientID VARCHAR(50), symptom VARCHAR(255), diagnosis VARCHAR(255), medicines VARCHAR(255), wardReq VARCHAR(50), typeWard VARCHAR(50));
CREATE TABLE doctor (doctorID varchar(10) PRIMARY KEY, name varchar(100), age varchar(3), gender varchar(10), phone varchar(10), address varchar(100), staffType varchar(50));
CREATE TABLE medical_appointment (appointmentID INT AUTO_INCREMENT PRIMARY KEY, patientID VARCHAR(10), doctorID VARCHAR(10), date DATE, time TIME, appointmentType VARCHAR(100), hasMedicalInsurance BOOLEAN, additionalComments VARCHAR(500), FOREIGN KEY (patientID) REFERENCES patient(patientID), FOREIGN KEY (doctorID) REFERENCES doctor(doctorID));


#IMPORTS MAS UTILIZADOS EN TODAS LAS CLASES
import Project.ConnectionProvider;
import java.sql.*;
import javax.swing.JOptionPane;


IMAGENES DEL PROGRAMA
LOGIN
![image](https://github.com/ItsRedm4n/MedicalSystem/assets/104162679/3f5cc964-44ab-4606-9e8d-eda8f1e78e67)
MENU
![image](https://github.com/ItsRedm4n/MedicalSystem/assets/104162679/1d5b581b-78f3-4cb7-bc45-6726e847fcba)
ADD PATIENT AND DOCTOR
![image](https://github.com/ItsRedm4n/MedicalSystem/assets/104162679/82798570-41f4-4529-9495-af407fd674fa)


CREDITOS
Hospital Management System. (2020, 22 marzo). [Vídeo]. Youtube. Recuperado 4 de mayo de 2024, de https://www.youtube.com/watch?v=nUqi3egzq28&t=1s

