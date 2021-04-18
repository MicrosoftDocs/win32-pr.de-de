---
description: Speichert Informationen zu Ereignis Abonnements und ruft Sie ab. Diese Schnittstelle erweitert die ieventabonnement-Schnittstelle.
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
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344374"
---
# <a name="ieventsubscription2-interface"></a>IEventSubscription2-Schnittstelle

Speichert Informationen zu Ereignis Abonnements und ruft Sie ab. Diese Schnittstelle erweitert die [**ieventabonnement**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) -Schnittstelle.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie müssen die **IEventSubscription2** -Schnittstelle nicht implementieren. Eine vom System bereitgestellte Ereignis Objektklasse (CLSID \_ ceventabonnement) implementiert **IEventSubscription2**.

## <a name="when-to-use"></a>Verwendung

Das [com+-Ereignis](com--events.md) System verwendet diese Schnittstelle zum Abrufen von Informationen zu einzelnen Abonnements.

## <a name="members"></a>Member

Die **IEventSubscription2** -Schnittstelle erbt von **ieventabonnement**. **IEventSubscription2** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IEventSubscription2** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                      | Zugriffstyp           | BESCHREIBUNG                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**FilterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Lesen/Schreiben<br/> | Die Filterkriterien für das Abonnement.<br/> |
| [**Abonniert**](ieventsubscription2-subscribermoniker.md)<br/> | Lesen/Schreiben<br/> | Der Moniker des Abonnenten.<br/>                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ieventabonnement**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




