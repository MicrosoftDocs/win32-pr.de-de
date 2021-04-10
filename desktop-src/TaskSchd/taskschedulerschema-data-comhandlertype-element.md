---
title: Data (comhandlertype)-Element
description: Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Datenelement Taskplaner
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956922"
---
# <a name="data-comhandlertype-element"></a>Data (comhandlertype)-Element

Gibt zusätzliche Daten an, die dem Handler zugeordnet sind.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

Das **Data** -Element wird durch den komplexen [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                  | Abgeleitet von                                                             | BESCHREIBUNG                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comhandlertype**](taskschedulerschema-comhandlertype-complextype.md) | Gibt eine Aktion an, die einen Handler auslöst.<br/> |



## <a name="remarks"></a>Bemerkungen

Anwendungen definieren die Handlerdaten mithilfe der [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) -Eigenschaft der [**icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) -Schnittstelle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schema Elemente Taskplaner](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





