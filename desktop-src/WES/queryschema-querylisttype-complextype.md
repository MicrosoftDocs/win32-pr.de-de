---
title: Komplexer querylisttype-Typ
description: Definiert eine Liste von Abfragen, die eine Reihe von Selektoren und Unterdrückern enthalten können, mit denen Ereignisse in das Resultset eingeschlossen oder daraus ausgeschlossen werden.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Querylisttype komplexer Typ EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338538"
---
# <a name="querylisttype-complex-type"></a>Komplexer querylisttype-Typ

Definiert eine Liste von Abfragen, die eine Reihe von Selektoren und Unterdrückern enthalten können, mit denen Ereignisse in das Resultset eingeschlossen oder daraus ausgeschlossen werden.

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                  | type                                                   | BESCHREIBUNG                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Query**](queryschema-query-querylisttype-element.md) | [**QueryType**](queryschema-querytype-complextype.md) | Definiert einen Satz von Selektoren und Unterdrückern, die verwendet werden, um Ereignisse in das Resultset einzuschließen oder Ereignisse aus dem Resultset auszuschließen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





