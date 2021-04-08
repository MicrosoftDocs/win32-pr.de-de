---
title: Valuequeries (eventtriggertype)-Element
description: Enthält eine Sequenz von-Elementen, die jeweils einen Namen und einen XPath-Abfrage Wert enthalten.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- Valuequeries-Element Taskplaner
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4448693c1c1ab19b2ea13050cc9ab817bdc25e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949570"
---
# <a name="valuequeries-eventtriggertype-element"></a>Valuequeries (eventtriggertype)-Element

Enthält eine Sequenz von-Elementen, die jeweils einen Namen und einen XPath-Abfrage Wert enthalten. Die Abfragen werden auf ein Ereignis angewendet, das von dem im [**Abonnement**](taskschedulerschema-subscription-eventtriggertype-element.md) Element angegebenen Ereignis Abonnement zurückgegeben wurde. Der Name des XPath-Abfrage Werts kann als Variable im Aktions Abschnitt einer Aufgabe verwendet werden.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

Das **valuequeries** -Element wird durch den komplexen [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) -Typ definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                      | Abgeleitet von                                                                 | BESCHREIBUNG                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggergroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) | Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.<br/> |



## <a name="remarks"></a>Bemerkungen

Informationen zur C++-Entwicklung finden Sie unter [**valuequeries-Eigenschaft von ieventvent**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries).

Informationen zur Skript Entwicklung finden Sie unter [**EventTrigger. valuequeries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Beispiele

Ein umfassendes Beispiel für den XML-Code für eine Aufgabe, die einen Ereignis Auslösers mit diesem Element angibt, finden Sie unter [Event-auslöserbeispiel (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

