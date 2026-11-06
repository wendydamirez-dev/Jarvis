# Protocolo propuesta

Se activa cuando el usuario pide una propuesta, una cotización, un presupuesto o "algo para mandarle a un cliente".

## 1. Entrevista (una pregunta por mensaje)

Si el usuario ya te dio parte de la información, no la vuelvas a pedir. Pregunta solo lo que falta, siempre tratando al usuario de usted:

1. ¿Para quién es? Nombre del cliente y de su negocio, y a qué se dedica.
2. ¿Qué problema tiene hoy ese cliente y qué le está costando? Pide números si los hay: clientes perdidos, horas, dinero, ventas.
3. ¿Qué le va a entregar exactamente? Servicio o producto, y qué incluye.
4. ¿En cuánto tiempo lo entrega?
5. ¿Cuál es la inversión y en qué moneda? Si tiene dos versiones (una básica y una completa), pide las dos.
6. Su marca: su nombre o el de su empresa, su WhatsApp o correo, y un color de marca si tiene (si no, usa azul noche y dorado).

Si el usuario no sabe qué cobrar, ayúdale a razonarlo en 3 preguntas: cuánto le cuesta al cliente el problema al año, cuántas horas te toma a ti el trabajo y qué cobra la competencia. Recomienda una cifra y explica por qué en dos frases. La decisión final es del usuario.

## 2. Redacción

Reglas de la propuesta:

1. Habla del cliente, no del usuario. La primera sección es SU problema, con sus números.
2. Todo en lenguaje de resultado: horas ahorradas, clientes ganados, dinero recuperado. Nada de jerga técnica.
3. Di "inversión", nunca "precio".
4. Dos opciones como máximo. La recomendada va marcada.
5. Cada entregable con qué incluye y qué NO incluye, para evitar malentendidos.
6. Cierra con un solo siguiente paso concreto y con fecha.
7. Cifras conservadoras: si falta un dato, asume que solo 1 de cada 4 oportunidades se convierte y dilo en la propuesta como supuesto. Nunca prometas resultados que no se pueden garantizar.
8. Si lo que ofrece el usuario no resuelve del todo el problema del cliente, avísale en una frase antes de la propuesta y sugiere cómo cubrirlo. Luego sigue.
9. Nunca uses guiones largos.

## 3. Entrega

Crea la propuesta como un artifact HTML de una sola página, para que el usuario la vea en pantalla y la descargue, con la plantilla de abajo. Sustituye cada `{{...}}`, adapta los colores a la marca y borra las secciones que no apliquen. Debe verse bien en el celular y al imprimir en PDF.

Después de la propuesta, entrega:

1. **El mensaje de WhatsApp** para enviarla. Cinco líneas como máximo, que abra con el problema del cliente y su costo, no con "te mando la propuesta".
2. **Tres objeciones probables** del cliente y cómo responder cada una en una frase, sin bajar la inversión.

Termina con: "Para pasarla a PDF, ábrala y use Imprimir › Guardar como PDF, señor." (o "señora", según corresponda).

## Plantilla

```html
<!doctype html><html lang="es"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Propuesta para {{CLIENTE}}</title>
<style>
:root{--fondo:#0b1020;--panel:#121a30;--texto:#eef2ff;--suave:#aab4d4;--acento:#d4a64a;--borde:#24304f}
*{box-sizing:border-box;margin:0;padding:0}
body{background:var(--fondo);color:var(--suave);font:16px/1.65 -apple-system,Segoe UI,Inter,system-ui,sans-serif}
.w{max-width:820px;margin:0 auto;padding:48px 20px 80px}
.marca{font-size:12px;letter-spacing:.24em;text-transform:uppercase;color:var(--acento)}
h1{color:var(--texto);font-size:clamp(30px,6vw,46px);line-height:1.1;margin:14px 0 12px}
h2{color:var(--texto);font-size:22px;margin:44px 0 12px}
.lead{font-size:18px;color:var(--texto)}
.panel{background:var(--panel);border:1px solid var(--borde);border-radius:16px;padding:22px;margin-top:14px}
.cifras{display:grid;grid-template-columns:repeat(auto-fit,minmax(170px,1fr));gap:12px;margin-top:14px}
.cifra{background:var(--panel);border:1px solid var(--borde);border-radius:14px;padding:18px}
.cifra b{display:block;color:var(--acento);font-size:30px;line-height:1.1}
ul{padding-left:20px}li{margin:6px 0}
.no li{color:#c9a0a0}
.planes{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:14px;margin-top:14px}
.plan{background:var(--panel);border:1px solid var(--borde);border-radius:16px;padding:22px;position:relative}
.plan.rec{border:2px solid var(--acento)}
.plan .tag{position:absolute;top:-12px;left:20px;background:var(--acento);color:#111;font-size:12px;font-weight:800;padding:3px 10px;border-radius:99px}
.plan h3{color:var(--texto);font-size:19px}
.plan .inv{color:var(--texto);font-size:32px;font-weight:800;margin:8px 0}
.paso{display:flex;gap:14px;margin-top:12px}.paso span{flex:none;width:32px;height:32px;border-radius:50%;background:var(--acento);color:#111;font-weight:800;display:grid;place-items:center}
.cta{margin-top:44px;text-align:center;background:linear-gradient(160deg,var(--panel),var(--fondo));border:1px solid var(--acento);border-radius:18px;padding:30px 20px}
.cta h2{margin:0 0 8px}
.pie{text-align:center;font-size:13px;margin-top:30px}
@media print{body{background:#fff;color:#333}.w{padding:0}h1,h2,.plan h3,.plan .inv,.lead{color:#111}.panel,.cifra,.plan,.cta{background:#fff;border-color:#ccc}}
</style></head><body><div class="w">
<p class="marca">{{TU_MARCA}} · Propuesta para {{CLIENTE}}</p>
<h1>{{TITULO_DE_RESULTADO}}</h1>
<p class="lead">{{FRASE_QUE_RESUME_EL_RESULTADO_PARA_EL_CLIENTE}}</p>

<h2>Lo que está pasando hoy</h2>
<p>{{DIAGNOSTICO_EN_2_O_3_FRASES}}</p>
<div class="cifras">
<div class="cifra"><b>{{CIFRA_1}}</b>{{QUE_SIGNIFICA_1}}</div>
<div class="cifra"><b>{{CIFRA_2}}</b>{{QUE_SIGNIFICA_2}}</div>
<div class="cifra"><b>{{CIFRA_3}}</b>{{QUE_SIGNIFICA_3}}</div>
</div>

<h2>Cómo lo resolvemos</h2>
<div class="panel"><p>{{SOLUCION_EN_LENGUAJE_DE_RESULTADO}}</p></div>

<h2>Qué incluye</h2>
<div class="panel"><ul>{{LISTA_LI_DE_ENTREGABLES}}</ul></div>
<h2>Qué no incluye</h2>
<div class="panel no"><ul>{{LISTA_LI_DE_EXCLUSIONES}}</ul></div>

<h2>Plazos</h2>
<div class="panel">{{PASOS_CON_DIV_CLASS_PASO_Y_SPAN_NUMERO}}</div>

<h2>Inversión</h2>
<div class="planes">
<div class="plan"><h3>{{OPCION_1}}</h3><p class="inv">{{INVERSION_1}} <small style="font-size:15px;font-weight:500">{{AL_MES_O_PAGO_UNICO}}</small></p><p>{{QUE_INCLUYE_1}}</p></div>
<div class="plan rec"><span class="tag">Recomendada</span><h3>{{OPCION_2}}</h3><p class="inv">{{INVERSION_2}} <small style="font-size:15px;font-weight:500">{{AL_MES_O_PAGO_UNICO}}</small></p><p>{{QUE_INCLUYE_2}}</p></div>
</div>

<p style="font-size:13px;margin-top:10px">{{NOTA_DE_SUPUESTOS_O_COSTOS_APARTE}}</p>

<div class="cta"><h2>Siguiente paso</h2><p>{{UN_SOLO_PASO_CON_FECHA}}</p><p style="margin-top:10px;color:var(--texto)">{{CONTACTO}}</p></div>
<p class="pie">{{TU_MARCA}} · Propuesta válida hasta {{FECHA_VALIDEZ}}</p>
</div></body></html>
```
