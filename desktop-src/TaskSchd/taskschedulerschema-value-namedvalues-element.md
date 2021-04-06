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
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743320"
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

Das **value** -Element wird durch den komplexen [**namedValues**](taskschedulerschema-namedvalues-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                              | Abgeleitet von                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Valuequeries (eventtriggertype)**](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [**namedValues**](taskschedulerschema-namedvalues-complextype.md) | Gibt eine Auflistung von benannten XPath-Abfragen an. Jede Abfrage in der Auflistung wird auf das letzte übereinstimmende Ereignis-XML angewendet, das von der Abonnement Abfrage zurückgegeben wird, die im [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) -Element angegeben ist. Der Name der Abfrage kann als Variable in der Nachricht einer ShowMessage-Aktion verwendet werden.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**Value-Eigenschaft von itasknamedvaluepair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).

Informationen zur Skript Entwicklung finden Sie unter [**tasknamedvaluepair. Value**](tasknamedvaluepair-value.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 





