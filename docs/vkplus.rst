#######################
Описание объекта VkPlus
#######################


.. py:class:: VkPlus

    .. py:function:: method(method: str, \*\*values, send_from=None, nowait=False)

       (Сопрограмма)
       Выполняет метод ``method`` API ВКонтакте (например, "messages.get") с параметрами ``values`` (например, {"count": 2}), в ``send_from`` можно передать SenderGroup или SenderUser, чтобы уточнить, кто должен выполнять команду, если ``nowait=True``, то method не вернёт результат запроса к вк, а продолжит программу без ожидания ответа.

    .. py:function:: upload_doc(multipart_data, filename="image.png")

       (Сопрограмма)
       Загружает ``multipart_data`` с именем ``filename`` и возвращает Attachment.

    .. py:function:: upload_photo(multipart_data)

       (Сопрограмма)
       Загружает фото ``multipart_data`` и возвращает Attachment.

    .. py:function:: mark_as_read(ids: str)

       (Сопрограмма)
       Помечает сообщения с ``ids`` как прочитанные.

    .. py:function:: resolve_name(screen_name: str)

       (Сопрограмма)
       Перевод короткого имени `screen_name` в числовой ID.

    .. py:function:: get_default_sender(key)

       Возвращает подходящего (на сколько это возможно) отправителя для метода `key`.

.. py:class:: Attachment(token_id):

    .. py:attribute:: type

    Тип вложения (photo, video, audio, doc, link, market, market_album, wall, wall_reply, sticker или gift).

    .. py:attribute:: owner_id

    ID владельца вложения.

    .. py:attribute:: id

    ID вложения.

    .. py:attribute:: access_key

    access_key вложения, если присутствует.

    .. py:attribute:: url

    Сслыка на вложение, если присутствует.


.. py:class:: SenderGroup(token_id):

    Какой токен должен выполнять запрос, ``token_id`` - это порядковый номер в текущем списке групповых личностей бота.


.. py:class:: SenderUser(token_id):

    Какой пользователь должен выполнять запрос, ``user_id`` - это порядковый номер в текущем списке пользовательских личностей бота.