---
title: SecurityDescriptor -Element (registrationInfoType)
description: Gibt die Sicherheitsbeschreibung der Aufgabe an.
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
ms.openlocfilehash: 83742ebbbc6b8fb653610bf8e20c00094a3c8a3984123765adf6e953935c9011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099860"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>SecurityDescriptor -Element (registrationInfoType)

Gibt die Sicherheitsbeschreibung der Aufgabe an.

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

Das **SecurityDescriptor-Element** wird durch den komplexen [**RegistrationInfoType-Typ**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt Administratorinformationen zum Task an, z. B. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird der Sicherheitsdeskriptor einer Aufgabe mithilfe der [**RegistrationInfo.SecurityDescriptor-Eigenschaft**](registrationinfo-securitydescriptor.md) angegeben.

Für die C++-Entwicklung wird der Sicherheitsdeskriptor einer Aufgabe mithilfe der [**IRegistrationInfo::SecurityDescriptor-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





