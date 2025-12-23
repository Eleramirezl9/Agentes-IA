# MiAgente - OpenCode AI Personalizado

Configuración personalizada de OpenCode AI con el agente **Gentleman** para desarrollo de software.

## 🎯 Características del Agente Gentleman

- **Senior Architect con 15+ años de experiencia**
- **Nunca es un yes-man**: Siempre verifica antes de estar de acuerdo
- **Colaborador proactivo**: Similar a Jarvis para Tony Stark
- **Propone alternativas**: Presenta opciones con compensaciones
- **Bilingüe**: Español rioplatense o inglés confrontacional
- **Verificador**: Investiga usando herramientas antes de responder

## 🚀 Instalación

### Prerrequisitos
- Node.js 18+ 
- OpenCode CLI instalado

### Instalar OpenCode
```bash
# Usando npm
npm install -g opencode-ai

# O usando curl
curl -fsSL https://opencode.ai/install | bash
```

### Configurar MiAgente
```bash
# Clonar este repositorio
git clone https://github.com/tu-usuario/MiAgente.git
cd MiAgente

# Copiar configuración al directorio de OpenCode
mkdir -p ~/.config/opencode
cp opencode.json ~/.config/opencode/

# O crear enlace simbólico para mantener actualizado
ln -sf $(pwd)/opencode.json ~/.config/opencode/opencode.json
```

## 📖 Uso

### Iniciar OpenCode con el agente Gentleman
```bash
opencode
```

### Cambiar al agente Gentleman
1. Inicia OpenCode
2. Escribe `/agent` y presiona Enter
3. Selecciona `gentleman` de la lista

### Uso directo
```bash
# Usar el agente gentleman directamente
opencode --agent gentleman
```

## ⚙️ Configuración

El archivo `opencode.json` contiene:

- **Modelo**: `anthropic/claude-sonnet-4-20250514`
- **Temperatura**: `0.3` (balance entre creatividad y precisión)
- **Herramientas**: Todas las herramientas de desarrollo habilitadas
- **Permisos**: 
  - Comandos bash: preguntar antes de ejecutar
  - Edición/escritura: permitido
  - Web fetch: permitido

### Personalización

Para modificar el agente:

1. Edita `~/.config/opencode/opencode.json`
2. O edita este archivo y copia nuevamente
3. Reinicia OpenCode

## 🛠️ Herramientas Disponibles

- **write**: Crear archivos
- **edit**: Editar archivos existentes
- **read**: Leer archivos
- **bash**: Ejecutar comandos del sistema
- **glob**: Búsqueda de archivos por patrones
- **grep**: Búsqueda de contenido
- **list**: Listar directorios
- **webfetch**: Obtener contenido web
- **websearch**: Buscar en internet
- **codesearch**: Buscar documentación de código
- **task**: Lanzar subagentes especializados
- **todowrite/todoread**: Gestión de tareas
- **skill**: Cargar habilidades especializadas

## 🎨 Tema

Incluye el tema **Gentleman** con colores inspirados en Kanagawa para una experiencia visual consistente.

## 📝 Ejemplos de Uso

### Planificación de características
```
Quiero agregar un sistema de autenticación a mi aplicación React. ¿Cuáles son las mejores opciones y qué ventajas/desventajas tiene cada una?
```

### Revisión de código
```
Revisa este componente y busca posibles problemas de seguridad o rendimiento:
@read src/components/UserForm.tsx
```

### Depuración
```
Tengo un error 500 en mi API. ¿Puedes ayudarme a investigar qué está pasando?
@bash npm run dev
```

### Documentación
```
Genera documentación para esta función:
@read src/utils/validation.ts
```

## 🤝 Contribuir

1. Fork este repositorio
2. Crea una rama (`git checkout -b feature/mejora-agente`)
3. Commit tus cambios (`git commit -am 'Mejorar configuración del agente'`)
4. Push a la rama (`git push origin feature/mejora-agente`)
5. Abre un Pull Request

## 📄 Licencia

MIT License - ver archivo [LICENSE](LICENSE) para detalles.

## 🔗 Enlaces Útiles

- [OpenCode Documentation](https://opencode.ai/docs/)
- [OpenCode GitHub](https://github.com/sst/opencode)
- [Agentes Documentation](https://opencode.ai/docs/agents/)

---

**Hecho con ❤️ usando OpenCode AI y el agente Gentleman**