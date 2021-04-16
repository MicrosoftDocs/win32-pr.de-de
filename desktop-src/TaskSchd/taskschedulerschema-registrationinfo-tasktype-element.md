---
title: RegistrationInfo (TaskType)-Element
description: Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- Registrierungsinformationen Taskplaner, XML-Element
- RegistrationInfo-Element Taskplaner
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477784"
---
# <a name="registrationinfo-tasktype-element"></a>RegistrationInfo (TaskType)-Element

Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

Das **RegistrationInfo** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | BESCHREIBUNG                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                                                  | type     | BESCHREIBUNG                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autor (registrationinfotype)**](taskschedulerschema-author-registrationinfotype-element.md)                         | Zeichenfolge   | Gibt den Autor der Aufgabe an.<br/>                                                                              |
| [**Date (registrationinfotype)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.<br/>                                                       |
| [**Description (registrationinfotype)**](taskschedulerschema-description-registrationinfotype-element.md)               | Zeichenfolge   | Gibt die Beschreibung des Tasks an.<br/>                                                                         |
| [**Dokumentation (registrationinfotype)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | Zeichenfolge   | Gibt jede zusätzliche Dokumentation für den Task an.<br/>                                                           |
| [**SecurityDescriptor (registrationinfotype)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | Zeichenfolge   | Gibt die Sicherheits Beschreibung der Aufgabe an.<br/>                                                                 |
| [**Quelle (registrationinfotype)**](taskschedulerschema-source-registrationinfotype-element.md)                         | Zeichenfolge   | Gibt an, woher die Aufgabe stammt. Beispielsweise aus einer Komponente, einem Dienst, einer Anwendung oder einem Benutzer.<br/> |
| [**URI (registrationinfotype)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Gibt den URI der Aufgabe an.<br/>                                                                                 |
| [**Version (registrationinfotype)**](taskschedulerschema-version-registrationinfotype-element.md)                       | Zeichenfolge   | Gibt die Versionsnummer der Aufgabe an.<br/>                                                                      |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**Taskdefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung werden die Registrierungsinformationen einer Aufgabe mithilfe der [**RegistrationInfo-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo)angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





