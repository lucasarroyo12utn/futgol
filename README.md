# FutGol - Sistema de Gestión de Campeonatos de Fútbol

Sistema completo para gestionar campeonatos, equipos, jugadores, partidos y estadísticas de fútbol.

## 📋 Características Implementadas

### ✅ Completamente Funcional

1. **Dashboard Principal**
   - Resumen de estadísticas (Torneos, Equipos, Jugadores, Partidos)
   - Próximos partidos
   - Actividad reciente
   - Tabla de posiciones en vivo
   - Top goleadores

2. **Gestión de Torneos**
   - Crear nuevos torneos
   - Visualizar estado (en curso, inscripción, programado)
   - Ver detalles por torneo
   - Filtros por categoría

3. **Gestión de Equipos**
   - Registrar equipos
   - Asignar delegados y contactos
   - Ver planteles
   - Estado de equipos (activo/suspendido)
   - Color identificador

4. **Gestión de Jugadores**
   - Registrar jugadores
   - Asignar a equipos
   - Posiciones (Arquero, Defensor, Mediocampista, Delantero)
   - Estadísticas (Partidos, Goles, Tarjetas)
   - Control de estado (habilitado/suspendido)

5. **Tabla de Posiciones**
   - Actualización dinámica
   - Cálculo de puntos
   - Diferencia de goles
   - Clasificación

6. **Persistencia de Datos**
   - Datos guardados en localStorage
   - Sincronización entre desktop y móvil
   - JSON simulado (archivo data.json)

7. **Interfaz Móvil**
   - Versión completamente responsive
   - Navegación inferior con 5 tabs
   - Diseño optimizado para teléfono
   - Velocidad de carga rápida

## 🚀 Cómo Usar

### Abrir la Aplicación

**Desktop:**
```bash
Abre futgol_dashboard.html en tu navegador
```

**Móvil:**
```bash
Abre futgol_mobile.html en tu navegador o simula en Chrome DevTools (F12)
```

### Crear un Nuevo Torneo

1. Haz clic en el botón **"+ Nuevo Torneo"** (desktop) o en el botón FAB (+)
2. Completa los campos:
   - Nombre del torneo
   - Categoría
   - Formato
   - Fechas de inicio y fin
   - Cantidad máxima de equipos
3. Haz clic en **"Guardar"**

### Registrar un Equipo

1. Haz clic en **"+ Nuevo Equipo"**
2. Completa:
   - Nombre del equipo
   - Color identificador
   - Categoría
   - Nombre y teléfono del delegado
3. Guarda el registro

### Agregar un Jugador

1. Ve a la sección de **"Jugadores"**
2. Haz clic en **"+ Nuevo Jugador"**
3. Completa:
   - Nombre y apellido
   - Equipo
   - Posición
   - Edad
4. Guarda

## 💾 Estructura de Datos (localStorage)

Los datos se guardan en formato JSON en localStorage con la siguiente estructura:

```json
{
  "torneos": [
    {
      "id": "torneo_001",
      "nombre": "Liga Apertura 2026",
      "emoji": "🏆",
      "estado": "en-curso",
      "categoria": "Primera",
      "formato": "Liga",
      "equiposCupo": 8
    }
  ],
  "equipos": [
    {
      "id": "eq_001",
      "nombre": "Atlético San Martín",
      "color": "#1565c0",
      "categoria": "Primera",
      "delegado": "Carlos Méndez",
      "estado": "activo"
    }
  ],
  "jugadores": [
    {
      "id": "jug_001",
      "nombre": "Matías Rodríguez",
      "equipo": "eq_001",
      "posicion": "Delantero",
      "edad": 27,
      "goles": 9,
      "amarillas": 2,
      "rojas": 0,
      "estado": "habilitado"
    }
  ],
  "partidos": [],
  "posiciones": []
}
```

## 🔧 Funcionalidades Técnicas

### JavaScript Core
- **loadData()** - Carga datos desde localStorage
- **saveData()** - Guarda datos en localStorage
- **initializeDefaultData()** - Inicializa datos por defecto
- **openModal(type)** - Abre modales según tipo
- **guardarRegistro()** - Guarda nuevos registros

### Navegación
- Desktop: Sidebar con menú principal
- Móvil: Bottom navigation con 5 tabs

### Modales
- Formularios dinámicos para CRUD
- Validación básica de campos
- Guardado automático

### Sincronización
- Ambas versiones comparten el mismo localStorage
- Datos se actualizan en tiempo real
- Persistencia entre sesiones

## 📱 Características Móvil

- **Inicio**: Resumen con acciones rápidas
- **Torneos**: Lista de torneos con progreso
- **Partidos**: Fixture y resultados
- **Posiciones**: Tabla de clasificación y goleadores
- **Más**: Configuración y opciones

## 🎨 Diseño

- **Colores**: Sistema de diseño consistente
- **Tipografía**: Segoe UI / System UI
- **Iconos**: Emojis modernos
- **Animaciones**: Transiciones suaves
- **Responsive**: Adapta a cualquier pantalla

## 📊 Datos de Ejemplo

La aplicación viene con 8 equipos preconfigurados:

1. Atlético San Martín (#1565c0)
2. Deportivo Norte (#2e7d32)
3. Club Social Belgrano (#6a1b9a)
4. Racing Tucumán (#c62828)
5. San Lorenzo FC (#00838f)
6. Independiente Sur (#ef6c00)
7. Boca Juniors FC (#0d47a1)
8. River Plate FC (#b71c1c)

Con 3 torneos activos:
- Liga Apertura 2026 (En curso)
- Copa Ciudad 2026 (Inscripción abierta)
- Torneo Relámpago Junio (Programado)

## 🔐 Seguridad

- Los datos se guardan localmente en el navegador
- No se envía información a servidores externos
- Cada navegador tiene sus propios datos
- Se puede exportar/importar fácilmente

## 🚀 Próximas Mejoras

Funcionalidades planificadas:
- Exportar a PDF/Excel
- Gráficos estadísticos avanzados
- Sistema de pagos integrado
- Notificaciones en tiempo real
- Backup a la nube
- API REST
- Multi-usuario con autenticación

## ⚙️ Configuración Técnica

### Navegadores Soportados
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers actualizados

### Requerimientos
- JavaScript habilitado
- localStorage disponible
- Conexión a internet (opcional)

## 📞 Soporte

Para reportar bugs o sugerir mejoras, contacta a:
- Email: soporte@futgol.local
- Version: 1.0
- Última actualización: Junio 2026

---

**Enjoy managing your tournaments! ⚽🏆**
