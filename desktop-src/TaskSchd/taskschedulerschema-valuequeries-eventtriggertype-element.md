---
title: ValueQueries (eventTriggerType) -Element
description: Enthält eine Sequenz von Elementen, die jeweils einen Namen und einen XPath-Abfragewert enthalten.
ms.assetid: 4b57568c-81b6-43fd-9194-9817c4817197
keywords:
- ValueQueries-Taskplaner
topic_type:
- apiref
api_name:
- ValueQueries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fecf58696618f1f0f359754bc29aa10680dd1717fe55ffe9fc3e87d0b361b76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118355343"
---
# <a name="valuequeries-eventtriggertype-element"></a>ValueQueries (eventTriggerType) -Element

Enthält eine Sequenz von Elementen, die jeweils einen Namen und einen XPath-Abfragewert enthalten. Die Abfragen werden auf ein Ereignis angewendet, das von dem ereignisabonnement zurückgegeben wird, das im [**Subscription-Element angegeben**](taskschedulerschema-subscription-eventtriggertype-element.md) ist. Der Name für den XPath-Abfragewert kann als Variable im Aktionsabschnitt einer Aufgabe verwendet werden.

``` syntax
<xs:element name="ValueQueries"
    type="namedValues"
    minOccurs="0"
 />
```

Das **ValueQueries-Element** wird durch den komplexen [**EventTriggerType-Typ**](taskschedulerschema-eventtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                                      | Abgeleitet von                                                                 | BESCHREIBUNG                                                                   |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger (triggerGroup)**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.<br/> |



## <a name="remarks"></a>Hinweise

Informationen zur C++-Entwicklung finden Sie unter [**ValueQueries-Eigenschaft von IEventTrigger.**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries)

Informationen zur Skriptentwicklung finden Sie unter [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).

## <a name="examples"></a>Beispiele

Ein vollständiges Xml-Beispiel für eine Aufgabe, die einen Ereignistrigger mit diesem Element angibt, finden Sie unter [Ereignistriggerbeispiel (XML).](/previous-versions//aa446889(v=vs.85))

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

