friends.appInvite

$description
Отправляет друзьям приглашение в приложение

$params#uids
Список идентификаторов друзей, разделённых запятой, которым требуется разослать приглашения

$params#text
Текст приглашения

$params#devices
Список устройств, на которых нужно отобразить приглашение. На данный момент поддерживаются: IOS, ANDROID

$additional
Пользователь должен подтвердить список получателей. Пользователю должно быть очевидно, что это действие приведет к рассылке пакета приглашений другим пользователям. В случае нарушения этого правила приложение будет заблокировано администрацией. При возникновении любых вопросов или сомнений обращайтесь в нашу службу поддержки API.
<br>
Используйте метод {% replace_method friends.getByDevices %} чтобы узнать устройства, которыми пользуется пользователь.
<br>
Для использования метода, запросите для вашего приложения право APP_INVITE.
<br>
Для отправки приглашения от пользователя A пользователю Б должны быть соблюдены требования:

* A должен быть пользователем приложения;
* Б не должен быть пользователем приложения;
* A и Б должны быть друзьями;
* A авторизовал приложение и выдал право APP_INVITE;
* Б до этого заходил на портал с устройства, на которое отправляется приглашение;
* Б не запретил в своих настройках приватности приглашения в приложения от друзей;
* Приложению должно быть разрешено отсылать приглашения на указанные типы устройств (IOS-приложение не может слать приглашения на устройства Android)