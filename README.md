  
Este repositorio contiene páginas Markdown (MD) que incluyen diagramas UML utilizando la sintaxis de Mermaid. Aquí encontrarás ejemplos de diferentes tipos de diagramas útiles para el diseño y documentación de software.

## Ejemplos de Diagramas

### Diagrama de Casos de Uso

```mermaid
usecase
  :Usuario: --> (Iniciar sesión)
  :Usuario: --> (Consultar información)
  (Iniciar sesión) ..> (Recuperar contraseña) : <<include>>
```

### Diagrama de Secuencia

```mermaid
sequenceDiagram
  participant Usuario
  participant Sistema
  Usuario->>Sistema: Solicita acceso
  Sistema-->>Usuario: Solicita credenciales
  Usuario->>Sistema: Envía credenciales
  Sistema-->>Usuario: Acceso concedido
```

### Diagrama Entidad-Relación

```mermaid
erDiagram
  USUARIO ||--o{ PEDIDO : realiza
  PEDIDO }|..|{ PRODUCTO : contiene
  USUARIO {
    string nombre
    string email
  }
  PEDIDO {
    int id
    date fecha
  }
  PRODUCTO {
    int id
    string nombre
    float precio
  }
```

### Diagrama de Requerimientos

```mermaid
requirementDiagram

requirement req1 {
  id: 1
  text: El sistema debe permitir el registro de usuarios.
}

requirement req2 {
  id: 2
  text: El sistema debe enviar notificaciones por correo.
}

req1 - SATISFIES -> req2

```

Repositorio para realizar diseño por medio de mermaid de software.
