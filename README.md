# Proyecto-1
Proyecto I programación II

# Documentación del Proyecto `NotasPrimaria`

## Introducción

El proyecto `NotasPrimaria` es una aplicación en Java diseñada para gestionar los datos de alumnos de sexto grado de primaria. Permite registrar, buscar y calcular las notas de los alumnos en cuatro bimestres, así como guardar y cargar estos datos desde un archivo de texto.

## Estructura del Proyecto

El proyecto está compuesto por las siguientes clases principales:

1. **`NotasPrimaria`**: Clase principal que proporciona la interfaz de consola para manejar los datos de los alumnos.
2. **`NotasPrimariaGUI`**: Clase que proporciona la interfaz gráfica de usuario (GUI) para gestionar los datos de los alumnos.
3. **`Alumno`**: Clase que representa al alumno con sus notas y proporciona métodos para manejar la información del alumno.
4. **`Notas`**: Clase que gestiona las notas de un alumno en los bimestres.
5. **`GestorNotas`**: Clase que permite la gestión de los datos de los alumnos, incluyendo la carga y el guardado en archivos de texto.

---

## Clase `NotasPrimariaGUI`

### Descripción
La clase NotasPrimariaGUI proporciona la interfaz gráfica de usuario (GUI) para gestionar los datos de los alumnos. Permite realizar las mismas operaciones que la interfaz de consola, pero a través de una interfaz gráfica.

### Componentes

1. Ventanas y Paneles: Utiliza JFrame, JPanel, y otros componentes Swing para crear la interfaz gráfica.
2. Botones: Incluye botones para ingresar alumnos, buscar alumnos, y calcular promedios.
3. Campos de Texto y Etiquetas: Utiliza campos de texto para la entrada de datos y etiquetas para mostrar información.

### Métodos

1. `public NotasPrimariaGUI()`: Constructor que inicializa la interfaz gráfica y configura los componentes.
2. `private void initComponents()`: Configura y organiza los componentes gráficos.
3. `private void agregarAlumnoActionPerformed(ActionEvent evt)`: Maneja el evento de agregar un alumno.
4. `private void buscarAlumnoActionPerformed(ActionEvent evt)`: Maneja el evento de buscar un alumno por código.
5. `private void calcularPromedioActionPerformed(ActionEvent evt)`: Maneja el evento de calcular el promedio del alumno.

### Ejemplo de Uso

public static void main(String[] args) {
    SwingUtilities.invokeLater(() -> {
        NotasPrimariaGUI gui = new NotasPrimariaGUI();
        gui.setVisible(true);
    });
}

## Clase `Alumno`

### Descripción
La clase Alumno representa al alumno y sus notas, y proporciona métodos para manejar la información del alumno.

### Métodos
1. `public String getNombre()`: Devuelve el nombre del alumno.
2. `public String getCodigo()`: Devuelve el código del alumno.
3. `public void setNota(int bimestre, double nota)`: Establece la nota para un bimestre específico.
4. `public double[] getNotas()`: Devuelve el array de notas del alumno.
5. `public double calcularPromedio()`: Calcula el promedio de las notas del alumno.
6. `public void mostrarDatos()`: Muestra los datos del alumno, incluidas las notas y el promedio.
7. `@Override public String toString()`: Devuelve una representación en cadena del alumno.
8. `public static Alumno fromString(String linea)`: Crea un objeto Alumno a partir de una línea de texto.

### Ejemplo de Uso
Notas notas = new Notas();
notas.setNota(1, 75);
notas.setNota(2, 85);
System.out.println(notas);


## Clase `Notas`

### Descripción
La clase Notas gestiona las notas de un alumno en los 4 bimestres y proporciona métodos para manejar la información de las notas.

### Métodos
1. `public void setNota(int bimestre, double nota)`: Establece la nota para un bimestre específico.
2. `public double getNota(int bimestre)`: Devuelve la nota para un bimestre específico.
3. `public double calcularPromedio()`: Calcula el promedio de las notas.
4. `@Override public String toString()`: Devuelve una representación en cadena de las notas y el promedio.

### Ejemplo de Uso
Notas notas = new Notas();
notas.setNota(1, 75);
notas.setNota(2, 85);
System.out.println(notas);

## Clase `GestorNotas`

### Descripción
La clase GestorNotas gestiona los datos de los alumnos, permite agregar, buscar, guardar y cargar datos desde un archivo de texto.

### Métodos
1. `public void agregarAlumno(Alumno alumno)`: Agrega un alumno a la lista.
2. `public Alumno getAlumnoPorCodigo(String codigo)`: Busca un alumno por su código.
3. `public void guardarDatos(String nombreArchivo)`: Guarda los datos de los alumnos en un archivo de texto.
4. `public void cargarDatos(String nombreArchivo)`: Carga los datos de los alumnos desde un archivo de texto.

### Ejemplo de Uso
GestorNotas gestor = new GestorNotas();
Alumno alumno = new Alumno("Juan Pérez", "123");
alumno.setNota(1, 75);
gestor.agregarAlumno(alumno);
gestor.guardarDatos("notas_alumnos.txt");
GestorNotas nuevoGestor = new GestorNotas();

















