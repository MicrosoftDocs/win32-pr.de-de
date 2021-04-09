---
title: Date (registrationinfotype)-Element
description: Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.
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
ms.openlocfilehash: 1e7d61b9cc637fcc39c8bfd114999a84ede4153d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104636"
---
# <a name="date-registrationinfotype-element"></a>Date (registrationinfotype)-Element

Gibt das Datum und die Uhrzeit der Registrierung der Aufgabe an.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

Das **Date** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skripterstellung wird das Registrierungsdatum einer Aufgabe mithilfe der [**RegistrationInfo. Date**](registrationinfo-date.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird das Registrierungsdatum einer Aufgabe mithilfe der [**iregistrationinfo::D Ate**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date) -Eigenschaft angegeben.

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

 

 





