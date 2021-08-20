---
title: RegistrationInfoType Complex Type
description: Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das RegistrationInfo-Element.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Komplexer registrationInfoType-Taskplaner
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 704fcb3205f032654ef6a666dd119dec34f88992018f16b1715ba4982847149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131660"
---
# <a name="registrationinfotype-complex-type"></a>RegistrationInfoType Complex Type

Definiert die untergeordneten Elemente und Sequenzierungsinformationen für das [**RegistrationInfo-Element.**](taskschedulerschema-registrationinfo-tasktype-element.md)

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                           | Typ     | Beschreibung                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Autor**](taskschedulerschema-author-registrationinfotype-element.md)                         | Zeichenfolge   | Gibt den Autor der Aufgabe an.<br/>                                                                       |
| [**Datum**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Gibt das Datum und die Uhrzeit der Registrierung des Task an.<br/>                                                |
| [**Beschreibung**](taskschedulerschema-description-registrationinfotype-element.md)               | Zeichenfolge   | Gibt die Beschreibung des Tasks an.<br/>                                                                  |
| [**Dokumentation**](taskschedulerschema-documentation-registrationinfotype-element.md)           | Zeichenfolge   | Gibt eine zusätzliche Dokumentation für die Aufgabe an.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | Zeichenfolge   | Gibt die Sicherheitsbeschreibung der Aufgabe an.<br/>                                                          |
| [**Quelle**](taskschedulerschema-source-registrationinfotype-element.md)                         | Zeichenfolge   | Gibt an, woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Gibt den URI der Aufgabe an.<br/>                                                                          |
| [**Version**](taskschedulerschema-version-registrationinfotype-element.md)                       | Zeichenfolge   | Gibt die Versionsnummer der Aufgabe an.<br/>                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Komplexe Schematypen](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





