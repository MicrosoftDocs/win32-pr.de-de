---
title: Documentation (registrationInfoType)-Element
description: Gibt eine beliebige zusätzliche Dokumentation für die Aufgabe an.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Documentation-Element Taskplaner
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6cb8c2a78450fffa467ea659b55015f064310783ae21b067093de9473612fcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356868"
---
# <a name="documentation-registrationinfotype-element"></a>Documentation (registrationInfoType)-Element

Gibt eine beliebige zusätzliche Dokumentation für die Aufgabe an.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

Das **Documentation-Element** wird durch den komplexen [**registrationInfoType-Typ**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen über den Task an, z. B. den Ersteller der Aufgabe und das Datum, an dem der Task registriert ist.<br/> |



## <a name="remarks"></a>Hinweise

Für Skriptanwendungen wird zusätzliche Aufgabendokumentation mithilfe der [**RegistrationInfo.DocUmentation-Eigenschaft**](registrationinfo-documentation.md) angegeben.

Für C++-Anwendungen wird mithilfe der [**IRegistrationInfo::D ocumentation-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) eine zusätzliche Aufgabendokumentation angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





