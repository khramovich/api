## <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Abacus.png" alt="Abacus" width="25" height="25" /> Тестирование API и SOAP

Первое задание — проверка XML на ошибки.

Затем — создание коллекции, подготовка 5 тест-кейсов и проведение автотестов в Postman на базе документации в Swagger. После этого — тестирование SOAP-сервиса CountryInfoService.

### Вводные данные:

* Первое задание (проверка XML на ошибки):
```xml
<?xml version="1.0" encoding="UTF-8"?>
<note date="12/05/2022">
<to><name>Alena</to></name>
<lastname>Petrova</lastname>
<from>Alex</From>
<update=12/05/2022><update>
</note>
```
* [Документация в Swagger](https://qa.demoshopping.ru/api-docs/) для qa-версии интернет-магазина Demoshopping

* Данные сервиса [CountryInfoService](http://webservices.oorsprong.org/websamples.countryinfo/CountryInfoService.wso?WSDL)   
В коллекцию должны попасть следующие методы: ListOfContinentsByName, ListOfCurrenciesByName, ListOfCountryNamesByName, CountryName, CountryISOCode, FullCountryInfo, LanguageName

### Артефакты:

* Скорректированный XML:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<note date="12/05/2022">
<to>
<name>Alena</name>
<lastname>Petrova</lastname>
</to>
<from>Alex</from>
<update date="12/05/2022"></update>
</note>
```
* Postman. Коллекция DemoShopping, тестирование API онлайн-магазина: [ссылка на коллекцию](https://www.postman.com/khramovich/workspace/roman-s-workspace/collection/40928672-04229a83-efce-476d-89a6-dfe4c526d3bc?action=share&creator=40928672&active-environment=40928672-eb2f9b48-9fc7-4363-81ff-c7309c9e2608), [json-файл коллекции на GitHub](https://github.com/khramovich/api/blob/main/DemoShopping.postman_collection.json)
* Postman. Коллекция DemoShopping, результаты прогона автотестов: [json-файл на GitHub](https://github.com/khramovich/api/blob/main/Roman%20Khramovich.%20DemoShopping.postman_test_run.json)
* Postman. Коллекция CountryInfoService, тестирование SOAP: [ссылка на коллекцию](https://www.postman.com/khramovich/workspace/roman-s-workspace/collection/40928672-b09b7fb7-4768-4149-9b1f-a6fc51454a20?action=share&creator=40928672&active-environment=40928672-eb2f9b48-9fc7-4363-81ff-c7309c9e2608), [json-файл коллекции на GitHub](https://github.com/khramovich/api/blob/main/CountryInfoService.postman_collection.json)
* Postman. Коллекция DemoShopping, тест-кейсы: [PDF-файл на GitHub](https://github.com/khramovich/api/blob/main/TD.%20API%20Testing.pdf)
