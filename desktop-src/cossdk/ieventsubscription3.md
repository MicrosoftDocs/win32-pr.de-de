---
description: Speichert Informationen zu Ereignisabonnements und ruft sie ab. Diese Schnittstelle erweitert die IEventSubscription2-Schnittstelle.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: IEventSubscription3-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: cbb6c5b19ed6116c59642e8dc5c0aa8eabf4800b066904f2132c7d182f2b7bbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070630"
---
# <a name="ieventsubscription3-interface"></a>IEventSubscription3-Schnittstelle

Speichert Informationen zu Ereignisabonnements und ruft sie ab. Diese Schnittstelle erweitert die [**IEventSubscription2-Schnittstelle.**](ieventsubscription2.md)

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie müssen die **IEventSubscription3-Schnittstelle** nicht implementieren. Eine vom System bereitgestellte Ereignisobjektklasse (CLSID \_ CEventSubscription) implementiert **IEventSubscription3.**

## <a name="when-to-use"></a>Verwendung

Das [COM+-Ereignissystem](com--events.md) verwendet diese Schnittstelle, um Informationen zu einzelnen Abonnements abzurufen.

## <a name="members"></a>Member

Die **IEventSubscription3-Schnittstelle** erbt von **IEventSubscription2.** **IEventSubscription3** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IEventSubscription3-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp           | BESCHREIBUNG                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Lesen/Schreiben<br/> | Die Anwendungs-GUID des Ereignisklassenobjekts.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Lesen/Schreiben<br/> | Die Partitions-GUID des Ereignisklassenobjekts.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Lesen/Schreiben<br/> | Die Anwendungs-GUID des Abonnenten.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Lesen/Schreiben<br/> | Die Partitions-GUID des Abonnenten.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




