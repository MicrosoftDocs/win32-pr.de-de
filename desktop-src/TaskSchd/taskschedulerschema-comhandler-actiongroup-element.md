---
title: Comhandler-Element (Aktionsgruppe)
description: Gibt eine Aktion an, die einen Handler auslöst.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Comhandler-Element Taskplaner
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956923"
---
# <a name="comhandler-actiongroup-element"></a>Comhandler-Element (Aktionsgruppe)

Gibt eine Aktion an, die einen Handler auslöst.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

Das **comhandler** -Element wird von der [**Aktionsgruppe**](taskschedulerschema-actiongroup-group.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                         | Abgeleitet von                                                       | BESCHREIBUNG                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md) | [**Aktions sType**](taskschedulerschema-actionstype-complextype.md) | Enthält die Aktionen, die vom Task ausgeführt werden.<br/> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                               | type                                                         | BESCHREIBUNG                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**ClassID**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidtype**](taskschedulerschema-guidtype-simpletype.md)  | Gibt den Bezeichner der Handlerklasse an.<br/>         |
| [**Daten**](taskschedulerschema-data-comhandlertype-element.md)       | [**Datentyp**](taskschedulerschema-datatype-complextype.md) | Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.<br/> |



## <a name="remarks"></a>Bemerkungen

Anwendungen definieren eine com- [**handleraktion mithilfe der icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) -Schnittstelle.

### <a name="attributes"></a>Attribute

Das folgende Attribut wird vom komplexen Typ " [**aktionbasetype**](taskschedulerschema-actionbasetype-complextype.md) " definiert.

-   ID: Bezeichner der von der Aufgabe ausgeführten Aktion.

## <a name="examples"></a>Beispiele

Der folgende XML-Code definiert eine com-handleraktion.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





