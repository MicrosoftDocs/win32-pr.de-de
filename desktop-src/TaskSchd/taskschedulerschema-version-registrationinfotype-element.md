---
title: Version (registrationInfoType)-Element
description: Gibt die Versionsnummer des Tasks an.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Version-Element Taskplaner
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63d69b501b12890939f3bd0b146c959278eeaa0d5eb596851a488cef87f0770a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610425"
---
# <a name="version-registrationinfotype-element"></a>Version (registrationInfoType)-Element

Gibt die Versionsnummer des Tasks an.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

Das **Version-Element** wird durch den komplexen [**registrationInfoType-Typ**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | Beschreibung                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen über den Task an, z. B. den Ersteller der Aufgabe und das Datum, an dem der Task registriert ist.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird die Version eines Tasks mithilfe der [**RegistrationInfo.Version-Eigenschaft**](registrationinfo-version.md) angegeben.

Für die C++-Entwicklung wird die Version eines Tasks mithilfe der [**IRegistrationInfo::Version-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) angegeben.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert die Version eines Tasks.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



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

 

 





