01
Registrar dos cuentas desde /registro/ en producción
Ej. usuario_a y usuario_b, cada una con un correo y contraseña distintos.

Resultado: Hecho, ambos usuarios estan registrados con sus contraseñas

02
Cargar servicios distintos con cada cuenta
Con sesión iniciada como usuario_a, crea 2 servicios. Cierra sesión, inicia como usuario_b y crea otros 2 servicios diferentes.

Resultado: Hecho, ambos usurios cuentan con sus respectivos servicios

03
Confirmar que el listado no se mezcla
Con sesión en usuario_b, en /servicios/ solo deben aparecer sus 2 servicios, nunca los de usuario_a.

Resultado: Los servicios no se mesclan, nunca se cruzan y nunca interfieren entre si

04
Intentar "saltarse" el aislamiento a propósito
Primero, con sesión en usuario_a, da clic en «Editar» de uno de sus servicios y anota el número que aparece en la barra de direcciones (ej. en /servicios/7/editar/ el id es 7). Cierra sesión, entra como usuario_b y escribe a mano en la barra de direcciones /servicios/<ese id>/editar/. Debe responder con un error 404, no con el formulario de edición.

Resultado: La pagina sale de servicios y marca un "Not Found" dejando claro la caida de esta.