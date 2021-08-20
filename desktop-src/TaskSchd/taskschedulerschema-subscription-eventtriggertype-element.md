---
title: Subscription (eventTriggerType)-Element
description: Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den Trigger auslöst.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Subscription-Element Taskplaner
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ec45a9c240a9dd5d30d2089f98216fc165af13fe418424f5b85feed5e022b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131555"
---
# <a name="subscription-eventtriggertype-element"></a>Subscription (eventTriggerType)-Element

Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den Trigger auslöst.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

Das **Subscription-Element** wird vom komplexen [**eventTriggerType-Typ**](taskschedulerschema-eventtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | Beschreibung                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) | Gibt einen Trigger an, der eine Aufgabe startet, wenn ein Systemereignis auftritt.<br/> |



## <a name="remarks"></a>Hinweise

Für die Skriptentwicklung wird das Ereignisabonnement durch die [**EventTrigger.Subscription-Eigenschaft**](eventtrigger-subscription.md) angegeben.

Für die C++-Entwicklung wird das Ereignisabonnement durch die [**IEventTrigger::Subscription-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Schemaelemente](task-scheduler-schema-elements.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





