# JEDIE ERP PRO — Demo para GitHub Pages

Aplicación estática de demostración en español para gestión de obras, trabajadores, jornadas, salarios acumulados, pagos, clientes, presupuestos, facturas, gastos, inventario e informes.

## Publicar en GitHub Pages
1. Crear un repositorio nuevo en GitHub, por ejemplo `jedie-erp-pro`.
2. Subir `index.html`, `styles.css` y `app.js` **a la raíz del repositorio**.
3. En **Settings → Pages → Build and deployment**, elegir **Deploy from a branch**, `main` y `/ (root)`, y guardar.
4. Abrir la URL de Pages que indique GitHub cuando termine el despliegue.

## Uso
- Crear primero clientes, trabajadores y obras.
- En **Jornadas**, asignar trabajador y tarifa. Si el trabajador tiene tarifa por día, una jornada con horas > 0 devenga una tarifa diaria; con tarifa por hora se multiplica por las horas.
- Registrar anticipos y pagos con el mes al que corresponden.
- Consultar **Salarios e IRPF** y **Bancos y remesas** (solo resumen, no remesa bancaria real).
- Exportar CSV o copia JSON desde **Configuración**.

## Límites críticos
- Los datos se almacenan en `localStorage` del navegador: no hay sincronización, cifrado, roles, auditoría, autenticación ni backend. **No introducir datos personales reales de trabajadores, datos bancarios ni documentación confidencial.** GitHub Pages publica los archivos de la web.
- No es una aplicación contable o de nóminas legalmente validada. IRPF solo aplica porcentaje manual y el saldo no es una nómina neta oficial. No calcula Seguridad Social ni coste laboral completo.
- Facturas y presupuestos son borradores de demostración, no facturas fiscales aptas para emisión. No incorpora Verifactu, Facturae, certificación ni integración con AEAT.
- No envía transferencias ni genera ficheros bancarios SEPA; no conecta con CaixaBank.
- El asistente muestra cálculos locales, no una integración de IA externa.
- Para uso empresarial real, migrar a Next.js + Supabase con autenticación, políticas RLS, validación de permisos, cifrado apropiado, copias, registros de auditoría, pruebas y revisión de cumplimiento normativo.

## Tecnología
HTML, CSS y JavaScript sin dependencias ni instalación. Funciona abriendo `index.html` o desde GitHub Pages.
