---
title: Date (registrationInfoType)-Element
description: Gibt das Datum und die Uhrzeit der Registrierung des Tasks an.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Date-Element Taskplaner
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f191d6181e450deff8ffdb7bda0bf97cd0b27901fe454c25599d17b8edb30628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866640"
---
# <a name="date-registrationinfotype-element"></a>Date (registrationInfoType)-Element

Gibt das Datum und die Uhrzeit der Registrierung des Tasks an.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

Das **Date-Element** wird durch den komplexen [**registrationInfoType-Typ**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen über den Task an, z. B. den Ersteller der Aufgabe und das Datum, an dem der Task registriert ist.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird das Registrierungsdatum eines Tasks mithilfe der [**RegistrationInfo.Date-Eigenschaft**](registrationinfo-date.md) angegeben.

Für die C++-Entwicklung wird das Registrierungsdatum einer Aufgabe mithilfe der [**IRegistrationInfo::D ate-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





