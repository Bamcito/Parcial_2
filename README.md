Calculadora CI — Parcial 2  
Desarrollo de Software 2  

 
Jarryson Steven Medina Noscue 
Juan Camilo Dorado Belalcázar 


Docente: 
Jhon Robert Causimanse  


Descripción General 

Este proyecto implementa una calculadora en PHP con operaciones aritméticas básicas (suma, resta, multiplicación y división), desarrollada bajo la metodología TDD (Desarrollo Dirigido por Pruebas) y con un pipeline de Integración Continua (CI) usando GitHub Actions.
El objetivo del parcial es demostrar el uso práctico de:
•	Gestión de dependencias con Composer
•	Pruebas unitarias automáticas con PHPUnit
•	Automatización de pruebas en la nube con GitHub Actions
•	Buenas prácticas de control de versiones con Git 





Estructura del Proyecto  

calculadora-ci/ 

├──. github/ 

│   └── workflows/ 

│       └── php-ci.yml          # Pipeline de Integración Continua 

├── src/ 

│   └── Calculadora.php         # Clase principal con la lógica 

├── tests/ 

│   └── CalculadoraTest.php     # Pruebas unitarias con PHPUnit 

├── composer.json               # Gestión de dependencias 

└── README.md                   # Este archivo

Tecnologías utilizadas
Tecnología	Versión	Propósito
PHP	8.2	Lenguaje de programación principal
Composer	Latest	Gestión de dependencias
PHPUnit	^10.0	Framework de pruebas unitarias
GitHub Actions	—	Pipeline de Integración Continua (CI)

Instalación y ejecución local 
Prerrequisitos 
-	PHP 8.2 o superior instalado 
-	  Composer instalado (getcomposer.org)  

Pasos 
# 1. Clonar el repositorio
git clone https://github.com/Bamcito/Parcial_2.git
cd Parcial_2

# 2. Instalar dependencias
composer install

# 3. Ejecutar las pruebas
. /vendor/bin/phpunit tests 

Resultado esperado 
PHPUnit 10.x

.....                                                               
5 / 5 (100%)

OK (5 tests, 5 assertions) 





Pruebas Unitarias 
El proyecto cuenta con 5 pruebas unitarias que cubren todas las operaciones de la calculadora:  
Prueba	Operación	Entrada	Resultado Esperado	Estado 

testSuma	Suma	2 + 3		✅ 

testResta	Resta	4 - 3		✅ 

testMultiplicacion	Multiplicación	4 × 3		✅ 

testDivision	División	6 ÷ 3		✅ 

testDivisionPorCeroLanzaExcepcion	División por cero	5 ÷ 0	InvalidArgumentException	✅

Historial de desarrollo (TDD) 
El proyecto fue desarrollado siguiendo el ciclo Rojo → Verde del TDD: 

#	Commit	Acción	Estado del Pipeline 

1	archivos base de la calculadora	Se suben los archivos base	✅ Verde 

2	agregar pipeline de GitHub Actions	Se crea el workflow de CI	✅ Verde 

3	integracion de prueba para la division	Se agrega testDivision()	❌ Rojo  

4	mejora en la implementación de testDivision	Se implementa dividir()	✅ Verde 

5	Prueba division por cero lanza excepcion	Se agrega testDivisionPorCeroLanzaExcepcion()	❌ Rojo  

6	Validación de division por cero con excepcion	Se lanza InvalidArgumentException	✅ Verde 

7	docs: agregar README 	Documentación final	✅ Verde

Enlace al repositorio  
https://github.com/Bamcito/Parcial_2.git
