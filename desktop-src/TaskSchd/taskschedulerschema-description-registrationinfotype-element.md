---
title: Description (registrationInfoType)-Element
description: Gibt die Beschreibung des Tasks an.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Beschreibungselement Taskplaner
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a6fef3012913eacfb8b8aa111793bd77255512d551bea0ab123d45b9caed6501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991390"
---
# <a name="description-registrationinfotype-element"></a>Description (registrationInfoType)-Element

Gibt die Beschreibung des Tasks an.

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

Das **Description-Element** wird durch den komplexen [**registrationInfoType-Typ**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen über den Task an, z. B. den Ersteller der Aufgabe und das Datum, an dem der Task registriert ist.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird die Beschreibung einer Aufgabe mithilfe der [**RegistrationInfo.Description-Eigenschaft**](registrationinfo-description.md) angegeben.

Für die C++-Entwicklung wird die Beschreibung einer Aufgabe mithilfe der [**IRegistrationInfo::D escription-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





