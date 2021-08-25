---
title: URI -Element (registrationInfoType)
description: Gibt den URI der Aufgabe an.
ms.assetid: 5b438e00-ed8a-4ec8-854f-e8eda48d1cfc
keywords:
- URI-element Taskplaner
topic_type:
- apiref
api_name:
- URI
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b9a2d9b8faf327f7b64be2cdd4273f2252405767004dc6e0d58b0c95b5f1910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355603"
---
# <a name="uri-registrationinfotype-element"></a>URI -Element (registrationInfoType)

Gibt den URI der Aufgabe an. Dieses Element wird verwendet, um anzugeben, wo der registrierte Task in der Taskordnerhierarchie platziert wird.

``` syntax
<xs:element name="URI"
    type="anyURI"
    minOccurs="0"
 />
```

Das **URI-Element** wird durch den komplexen [**RegistrationInfoType-Typ**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt Administratorinformationen zum Task an, z. B. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert wird.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird der URI der Aufgabe mithilfe der [**RegistrationInfo.URI-Eigenschaft**](registrationinfo-uri.md) angegeben.

Für die C++-Entwicklung wird der URI der Aufgabe mithilfe der [**IRegistrationInfo::URI-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_uri) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





