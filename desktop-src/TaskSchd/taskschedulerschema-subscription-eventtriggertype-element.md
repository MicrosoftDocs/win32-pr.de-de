---
title: Abonnement (eventtriggertype)-Element
description: Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.
ms.assetid: ea351a55-c6f9-4e39-b15e-c2a1027a1360
keywords:
- Abonnement Element Taskplaner
topic_type:
- apiref
api_name:
- Subscription
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efe38f2e825e2de566391a7b1707ce1f8cfbbc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743768"
---
# <a name="subscription-eventtriggertype-element"></a>Abonnement (eventtriggertype)-Element

Gibt die XPath-Abfrage an, die das Ereignis identifiziert, das den-Triggern auslöst.

``` syntax
<xs:element name="Subscription"
    type="nonEmptyString"
 />
```

Das **Abonnement** Element wird durch den komplexen Typ [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) definiert.

## <a name="parent-element"></a>Übergeordnetes Element



| Element                                                                       | Abgeleitet von                                                                 | BESCHREIBUNG                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) | [**eventtriggertype**](taskschedulerschema-eventtriggertype-complextype.md) | Gibt einen-Fehler an, der einen Task startet, wenn ein System Ereignis auftritt.<br/> |



## <a name="remarks"></a>Bemerkungen

Bei der Skript Entwicklung wird das Ereignis Abonnement durch die [**EventTrigger. Abonnement**](eventtrigger-subscription.md) -Eigenschaft angegeben.

Bei der C++-Entwicklung wird das Ereignis Abonnement durch die [**ieventvent:: Abonnement**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_subscription) -Eigenschaft angegeben.

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

 

 





