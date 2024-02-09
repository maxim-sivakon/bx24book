# Событие OnAfterCrmDealAdd



{% tabs %}
{% tab title="Описание" %}
Событие вызываемое перед созданием элемента методом `CCrmDeal::Add`.



|  Параметр  | Значение                   |
| :--------: | -------------------------- |
| &$arFields | Поля создаваемого элемента |
{% endtab %}

{% tab title="Пример использования" %}
```php
$eventManager = \Bitrix\Main\EventManager::getInstance();

$eventManager->addEventHandlerCompatible(
    'crm',
    'OnBeforeCrmDealAdd',
    function( &$arFields )
    {
        // $arFields может изменяться
        // (добавлять поля, изменять или удалять некоторые параметры)
        return true;
    }
);
```
{% endtab %}
{% endtabs %}
