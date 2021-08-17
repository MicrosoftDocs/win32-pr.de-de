---
title: Komplexer TaskListType-Typ
description: Definiert eine Liste von Aufgaben, die zum Identifizieren der Komponenten einer Anwendung verwendet werden.
ms.assetid: 41a46967-7c5b-4555-9f65-bd9582c0c492
keywords:
- Komplexer TaskListType-Typ EventLog
topic_type:
- apiref
api_name:
- TaskListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d59457aaeeefeec4b490b4c399a2faafb4f62c22e67a600f741ccc16b3abcaad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750906"
---
# <a name="tasklisttype-complex-type"></a>Komplexer TaskListType-Typ

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



| Element                                                       | type                                                         | Beschreibung                                                       |
|---------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Aufgabe**](eventmanifestschema-task-tasklisttype-element.md) | [**TaskType**](eventmanifestschema-tasktype-complextype.md) | Definiert eine Komponente oder Unterkomponente einer Anwendung.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





