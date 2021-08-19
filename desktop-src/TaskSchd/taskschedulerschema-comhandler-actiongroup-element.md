---
title: ComHandler -Element (actionGroup)
description: Gibt eine Aktion an, die einen Handler ausgibt.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- ComHandler-Element Taskplaner
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aba73244c3dc5217bcfe7350462200cd3226f0607c6d68ce5c6bcb8f5574b7df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943237"
---
# <a name="comhandler-actiongroup-element"></a>ComHandler -Element (actionGroup)

Gibt eine Aktion an, die einen Handler ausgibt.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

Das **ComHandler-Element** wird durch die [**actionGroup definiert.**](taskschedulerschema-actiongroup-group.md)

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                         | Abgeleitet von                                                       | Beschreibung                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Enthält die aktionen, die von der Aufgabe ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | Typ                                                         | Beschreibung                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Classid**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Gibt den Bezeichner der Handlerklasse an.<br/>         |
| [**Daten**](taskschedulerschema-data-comhandlertype-element.md)       | [**Datatype**](taskschedulerschema-datatype-complextype.md) | Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.<br/> |



## <a name="remarks"></a>Hinweise

Anwendungen definieren eine COM-Handleraktion mithilfe der [**IComHandlerAction-Schnittstelle.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

### <a name="attributes"></a>Attribute

Das folgende Attribut wird durch den komplexen [**ActionBaseType-Typ**](taskschedulerschema-actionbasetype-complextype.md) definiert.

-   ID: Bezeichner der Aktion, die vom Task ausgeführt wird.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine COM-Handleraktion.


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





