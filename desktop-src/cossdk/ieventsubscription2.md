---
description: Speichert und ruft Informationen zu Ereignisabonnements ab. Diese Schnittstelle erweitert die IEventSubscription-Schnittstelle.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: IEventSubscription2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 332f123756d1340352524852aa5bcb38fce09612f52554facaf6e5c8c2398e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047481"
---
# <a name="ieventsubscription2-interface"></a>IEventSubscription2-Schnittstelle

Speichert und ruft Informationen zu Ereignisabonnements ab. Diese Schnittstelle erweitert die [**IEventSubscription-Schnittstelle.**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie müssen die **IEventSubscription2-Schnittstelle nicht** implementieren. Eine vom System bereitgestellte Ereignisobjektklasse (CLSID \_ CEventSubscription) implementiert **IEventSubscription2.**

## <a name="when-to-use"></a>Verwendung

Das [COM+-Ereignissystem](com--events.md) verwendet diese Schnittstelle, um Informationen zu einzelnen Abonnements zu erhalten.

## <a name="members"></a>Member

Die **IEventSubscription2-Schnittstelle** erbt von **IEventSubscription**. **IEventSubscription2** verfügt auch über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IEventSubscription2-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                      | Zugriffstyp           | Beschreibung                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**FilterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Lesen/Schreiben<br/> | Die Filterkriterien für das Abonnement.<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | Lesen/Schreiben<br/> | Der Moniker des Abonnenten.<br/>                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




