---
title: SecurityDescriptor (registrationinfotype)-Element
description: Gibt die Sicherheits Beschreibung der Aufgabe an.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- SecurityDescriptor-Element Taskplaner
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 20f352e20f1017029558a0de0a99186a978edbf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040280"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>SecurityDescriptor (registrationinfotype)-Element

Gibt die Sicherheits Beschreibung der Aufgabe an.

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

Das **securityDescriptor** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird die Sicherheits Beschreibung einer Aufgabe mithilfe der [**RegistrationInfo. securityDescriptor**](registrationinfo-securitydescriptor.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird die Sicherheits Beschreibung einer Aufgabe mithilfe der [**iregistrationinfo:: securityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) -Eigenschaft angegeben.

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

 

 





