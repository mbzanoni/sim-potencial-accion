Descripción
Página HTML autocontenida (sin dependencias externas) que permite explorar la dinámica del potencial de acción mediante dos parámetros ajustables y consignas guiadas.
La respuesta subumbral se modela como una membrana pasiva RC (decaimiento exponencial al potencial de reposo). Ante un estímulo que supera el umbral, se despliega una traza canónica fija que representa el potencial de acción completo, garantizando el principio todo-o-nada independientemente de la amplitud del estímulo.
Parámetros

Amplitud del estímulo (µA/cm²): intensidad de la corriente excitatoria entrante
Umbral de disparo (mV): potencial a partir del cual se genera el potencial de acción

No está usando las ecuaciones de HH; si bien están en el código, se reemplazaron por una membrana pasiva RC simple para evitar los bugs que tenías (disparos subumbrales espurios, no retorno al reposo). Lo que corre ahora es:

Subumbral: dV/dt = -(V - Vrest)/τ + Rm·I — puramente pasivo, sin canales
Supraumbral: traza canónica fija (curva analítica, no HH)

Consignas incluidas

¿Qué pasa si el estímulo es muy débil?
Encontrá el umbral empíricamente
Comprobá el principio todo-o-nada
¿Qué pasa si modificás el umbral de disparo?

Uso
Abrir potencial_accion.html directamente en el navegador. No requiere servidor ni instalación.
