---
title: Data (TaskType)-Element
description: Definiert Additions Daten, die dem Task zugeordnet sind, aber anderweitig vom Taskplaner Dienst nicht verwendet werden.
ms.assetid: 296cd33d-5f82-4de7-84a7-e791619ad0b5
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
ms.openlocfilehash: 3afff1cbd81ede49568afdc9e516d87a57ff9e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740825"
---
# <a name="data-tasktype-element"></a>Data (TaskType)-Element

Definiert Additions Daten, die dem Task zugeordnet sind, aber anderweitig vom Taskplaner Dienst nicht verwendet werden.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

Das **Data** -Element wird durch den komplexen [**TaskType**](taskschedulerschema-tasktype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                          | Abgeleitet von                                                 | BESCHREIBUNG                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Aufgabe**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definiert den Task, der vom Taskplaner-Dienst ausgeführt wird.<br/> |



## <a name="remarks"></a>Bemerkungen

Als Beispiel für diese Art von Daten verwendet der Leistungsprotokolle und-Warnungen-Dienst diese Eigenschaft als Speicher Container für die einem Task zugeordnete Leistungs-Leistungs Zählers-Abfrage.

Bei der C++-Entwicklung werden die Daten einer Aufgabe mithilfe der [**Data-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_data)angegeben.

Bei der Skripterstellung werden die Daten einer Aufgabe mithilfe der [**Taskdefinition. Data**](taskdefinition-data.md) -Eigenschaft angegeben.

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

 

 





