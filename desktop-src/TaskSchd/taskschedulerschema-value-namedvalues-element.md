---
title: Value (namedValues)-Element
description: Enthält den Wert, der einem Namen in einem Name-Wert-Paar zugeordnet ist.
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- Value-Element Taskplaner
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2583d7fcaa9a9832e54c405200397e40948204546cb81e89a90ceb6949e218e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610415"
---
# <a name="value-namedvalues-element"></a>Value (namedValues)-Element

Enthält den Wert, der einem Namen in einem Name-Wert-Paar zugeordnet ist.

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

Das **Value-Element** wird durch den komplexen [**NamedValues-Typ**](taskschedulerschema-namedvalues-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                              | Abgeleitet von                                                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ValueQueries (eventTriggerType)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Gibt eine Auflistung benannter XPath-Abfragen an. Jede Abfrage in der Auflistung wird auf die letzte übereinstimmende Ereignis-XML angewendet, die von der Abonnementabfrage zurückgegeben wird, die im [**Subscription-Element**](taskschedulerschema-subscription-eventtriggertype-element.md) angegeben ist. Der Name der Abfrage kann als Variable in der Nachricht einer ShowMessage-Aktion verwendet werden.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**Value Property of ITaskNamedValuePair (Werteigenschaft von ITaskNamedValuePair).**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value)

Informationen zur Skriptentwicklung finden Sie unter [**TaskNamedValuePair.Value.**](tasknamedvaluepair-value.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 





