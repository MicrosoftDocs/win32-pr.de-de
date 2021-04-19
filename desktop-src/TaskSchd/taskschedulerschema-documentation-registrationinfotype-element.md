---
title: Documentation-Element (registrationinfotype)
description: Gibt jede zusätzliche Dokumentation für den Task an.
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
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346540"
---
# <a name="documentation-registrationinfotype-element"></a>Documentation-Element (registrationinfotype)

Gibt jede zusätzliche Dokumentation für den Task an.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

Das **Documentation** -Element wird durch den komplexen Typ [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                           | Abgeleitet von                                                                         | BESCHREIBUNG                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationinfotype**](taskschedulerschema-registrationinfotype-complextype.md) | Gibt administrative Informationen zum Task an, z. b. den Autor der Aufgabe und das Datum, an dem die Aufgabe registriert ist.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei Skript Anwendungen wird mithilfe der-Eigenschaft [**RegistrationInfo.Doc**](registrationinfo-documentation.md) -Eigenschaft die zusätzliche Aufgaben Dokumentation angegeben.

Für C++-Anwendungen wird mithilfe der [**iregistrationinfo::D ocumentation**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) -Eigenschaft eine zusätzliche Aufgaben Dokumentation angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





