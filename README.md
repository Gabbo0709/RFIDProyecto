# RFIDProyecto

# Planeación (español).

Gestionar la entrada y dar apoyo al personal de seguridad con situaciones para alumnos en estado de ebriedad que intenten acceder al plantel.

Alcances:

- La gestión de la entrada será a través de usar como identificación tarjetas de radiofrecuencia (RFID Mifare Classic).
- El identificador de las tarjetas será leído a través del módulo RC522 al presentarse la tarjeta.
Datasheet: https://www.nxp.com/docs/en/data-sheet/MFRC522.pdf
- Se registrará la alcoholemia en aliento usando el módulo sensor de alcohol MQ-3.
Datasheet: https://www.sparkfun.com/datasheets/Sensors/MQ-3.pdf
- Cuando un alumno presente un nivel de alcoholemia mayor al máximo permitido en el reglamento de la unidad, se levantará un reporte al alumno en el que se mostrará la fecha y hora del incidente, boleta o matrícula del alumno, entrada (si aplica) desde la cual se envía el reporte y grado de alcoholemia en aliento registrado; este reporte será enviado a la dirección correspondiente especificada por la unidad.
- El reporte enviado estará impreso en un archivo PDF.
- El reporte será almacenado en la base de datos de la aplicación.
- El ID de la tarjeta estará relacionado con la boleta del alumno almacenada en la base de datos.
- La pruebas de alcoholemia se harán a criterio del personal de seguridad y estarán sujetas al reglamento de la unidad académica.

Límitaciones:

- El reporte solo servirá como registro de un intento de acceso a la unidad.
- Esto no aplica para alumnos de CELEX ni alumnnos de posgrado, solo para los inscritos en licenciatura en la unidad.
- El sistema solo podrá funcionar en configuraciones con Windows 10 y Windows 11 como sistema operativo.


Requerimentos funcionales:

- La base de datos estára en un modelo relacional.
- La aplicación funcionará a través del framework .NET 7.0.
- El equipo en el que se ejecute la aplicación deberá contar con acceso a la red local de la unidad académica.

Requerimentos no funcionales:

- Al presentarse la identificación en el lector se emitirá un sonido para indicar si se leyó correctamente la tarjeta.

Especificaciones técnicas:

- La aplicación será codificada en C# haciendo uso del framework .NET 7.0 de Microsoft. Esta apliación será ejecutada de manera local mostrando formularios de windows (WinForms). Usando el IDE Visual Studio Community 2022.
- La base de datos será codificada en Transact SQL cuyo gestor de base de datos será Microsoft SQL Server 2022. 
- El sistema electrónico será implementado con:
	- Modulo RC522.
	- Sensor MQ-3.
	- Placa de desarrollo Arduino UNO R3.

# Planification (English)

Manage entry and provide support to security personnel with situations involving intoxicated students.

Scope:

- Entry management will be carried out by using radio frequency identification cards (RFID Mifare Classic) as identification.
- The card identifier will be read through the RC522 module when the card is presented (see the sensor datasheet in Annex A).
- Breath alcohol concentration will be recorded using the MQ-3 alcohol sensor module (see the sensor datasheet in Annex A).
- When a student presents a breath alcohol concentration higher than the maximum allowed by the unit's regulations, a report will be generated for the student. The report will include the date and time of the incident, the student's ID or enrollment number, the entry point (if applicable) from which the report is sent, and the recorded breath alcohol concentration. This report will be sent to the corresponding address specified by the unit.
- The sent report will be printed in a PDF file.
- The report will be stored in the application's database.
- The ID of the card will be linked to the student's enrollment number stored in the database.
- Breathalyzer tests will be conducted at the discretion of security personnel and wil be subject to the academic unit's regulations.

Limitations:

- The report will only serve as a record of an access attempt to the unit.
- This system does not apply to CELEX students or postgraduate students, only to undergraduate students.
- The system will only function on configurations with Windows 10 and Windows 11 as the operating system.

Functional Requirements:

- The database will be in a relational model.
- The application will function through the .NET 7.0 framework.
- The computer running the application must have access to the academic unit's local network.

Non-Functional Requirements:

- When the identification is presented to the reader, a sound will be emitted to indicate if the card was read correctly.

Technical Specifications:

- The application will be coded in C# using Microsoft's .NET 7.0 framework. This application will be executed locally, displaying Windows forms (WinForms) and developed using the Visual Studio Community 2022 IDE.
- The database will be coded in Transact SQL, and the database management system will be Microsoft SQL Server 2022.
- The electronic system will be implemented with:
    - RC522 Module.
    - MQ-3 Sensor
    - Arduino UNO R3 Development Board.