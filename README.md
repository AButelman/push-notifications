# Push-notifications

El botón en la activity genera un log en Android Studio con el token de identificación único del dispositivo.

Se debe buscar en la consola de Firebase la key de autorización de la aplicación en la plataforma.

## Json a enviar para generar la notifación:

URL: https://fcm.googleapis.com/fcm/send
METHOD: POST

HEADERS:

    Content/type: application/json
    Authorization: key=token_de_identificacion_de_la_aplicacion_en_firebase

BODY:

    {
	"notification" : {
            "click_action" : ".ActivityAAbrirAlPresionarNotificacion", 
            "body" : "Cuerpo del mensaje", 
            "title" : "Titulo del mensaje", 
            "icon" : "Imagen del icono, debe estar precargada en la aplicacion en la carpeta Drawable",
            "sound" : "Sonido de notificacion, debe estar precargada en la aplicacion en la carpeta Raw"},
      "registration_ids": [ "token_identificacion_dispositivo" ]
    }

