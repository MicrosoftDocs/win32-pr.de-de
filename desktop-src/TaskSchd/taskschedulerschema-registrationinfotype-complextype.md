---
title: komplexer registrationinfotype-Typ
description: Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das RegistrationInfo-Element.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- komplexer registrationinfotype-Typ Taskplaner
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956761"
---
# <a name="registrationinfotype-complex-type"></a>komplexer registrationinfotype-Typ

Definiert die untergeordneten Elemente und Sequenzierungs Informationen für das [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) -Element.

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



| Element                                                                                           | type     | BESCHREIBUNG                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Autor**](taskschedulerschema-author-registrationinfotype-element.md)                         | Zeichenfolge   | Gibt den Autor der Aufgabe an.<br/>                                                                       |
| [**Datum**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.<br/>                                                |
| [**Beschreibung**](taskschedulerschema-description-registrationinfotype-element.md)               | Zeichenfolge   | Gibt die Beschreibung des Tasks an.<br/>                                                                  |
| [**Dokumentation**](taskschedulerschema-documentation-registrationinfotype-element.md)           | Zeichenfolge   | Gibt jede zusätzliche Dokumentation für den Task an.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | Zeichenfolge   | Gibt die Sicherheits Beschreibung der Aufgabe an.<br/>                                                          |
| [**Ausgangs**](taskschedulerschema-source-registrationinfotype-element.md)                         | Zeichenfolge   | Gibt an, woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.<br/> |
| [**RT**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Gibt den URI der Aufgabe an.<br/>                                                                          |
| [**Version**](taskschedulerschema-version-registrationinfotype-element.md)                       | Zeichenfolge   | Gibt die Versionsnummer der Aufgabe an.<br/>                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komplexe Typen von Taskplaner Schemas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





