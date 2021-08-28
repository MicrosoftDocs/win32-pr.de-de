---
title: Komplexer QueryListType-Typ
description: Definiert eine Liste von Abfragen, die einen Satz von Selektoren und Unterdrückungen enthalten können, die verwendet werden, um Ereignisse in das Ergebnisset ein- oder auszuschließen.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Komplexer QueryListType-Typ EventLog
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1692427538dcd500cd4190839ffcc148c7358e0aee7f5a27b4906192a0810b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904160"
---
# <a name="querylisttype-complex-type"></a>Komplexer QueryListType-Typ

Definiert eine Liste von Abfragen, die einen Satz von Selektoren und Unterdrückungen enthalten können, die verwendet werden, um Ereignisse in das Ergebnisset ein- oder auszuschließen.

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
| [**Query**](queryschema-query-querylisttype-element.md) | [**QueryType**](queryschema-querytype-complextype.md) | Definiert einen Satz von Selektoren und Unterdrückungen, die verwendet werden, um Ereignisse in das Ergebnisset ein- oder auszuschließen.<br/> |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





