---
title: ClassID-Element (comhandlertype)
description: Gibt den Bezeichner der Handlerklasse an.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- ClassID-Element Taskplaner
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479239"
---
# <a name="classid-comhandlertype-element"></a>ClassID-Element (comhandlertype)

Gibt den Bezeichner der Handlerklasse an.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

Das **ClassID-** Element wird durch den komplexen [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                             | BESCHREIBUNG                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md) | Gibt eine Aktion an, die einen Handler auslöst.<br/> |



## <a name="remarks"></a>Bemerkungen

Anwendungen definieren den Klassen Bezeichner mithilfe der [**ClassID-**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) Eigenschaft der [**icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) -Schnittstelle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





