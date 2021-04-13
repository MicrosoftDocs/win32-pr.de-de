---
title: Komplexer tasklisttype-Typ
description: Definiert eine Liste von Aufgaben, die zum Identifizieren der Komponenten einer Anwendung verwendet werden.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Tasklisttype Complex-Typ EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad427743242ada8901e904fc4e03620ccc72f405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391486"
---
# <a name="tasklisttype-complex-type"></a>Komplexer tasklisttype-Typ

Definiert eine Liste von Aufgaben, die zum Identifizieren der Komponenten einer Anwendung verwendet werden.

``` syntax
<xs:complexType name="TaskListType">
    <xs:sequence>
        <xs:element name="task"
            type="TaskType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                       | type                                                         | BESCHREIBUNG                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Task**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | Definiert eine Komponente oder eine Unterkomponente einer Anwendung.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





