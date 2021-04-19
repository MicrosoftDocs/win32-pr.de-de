---
description: Speichert Informationen zu Ereignis Abonnements und ruft Sie ab. Diese Schnittstelle erweitert die IEventSubscription2-Schnittstelle.
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
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346456"
---
# <a name="ieventsubscription3-interface"></a>IEventSubscription3-Schnittstelle

Speichert Informationen zu Ereignis Abonnements und ruft Sie ab. Diese Schnittstelle erweitert die [**IEventSubscription2**](ieventsubscription2.md) -Schnittstelle.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie müssen die **IEventSubscription3** -Schnittstelle nicht implementieren. Eine vom System bereitgestellte Ereignis Objektklasse (CLSID \_ ceventabonnement) implementiert **IEventSubscription3**.

## <a name="when-to-use"></a>Verwendung

Das [com+-Ereignis](com--events.md) System verwendet diese Schnittstelle zum Abrufen von Informationen zu einzelnen Abonnements.

## <a name="members"></a>Member

Die **IEventSubscription3** -Schnittstelle erbt von **IEventSubscription2**. **IEventSubscription3** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IEventSubscription3** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp           | BESCHREIBUNG                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**Eventclassapplicationid**](ieventsubscription3-eventclassapplicationid.md)<br/> | Lesen/Schreiben<br/> | Die Anwendungs-GUID des Ereignis Klassen Objekts.<br/> |
| [**Eventclasspartitionid**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Lesen/Schreiben<br/> | Die Partitions-GUID des Ereignis Klassen Objekts.<br/>   |
| [**Abonnement-ID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Lesen/Schreiben<br/> | Die Anwendungs-GUID des Abonnenten.<br/>         |
| [**Abonnement-ID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Lesen/Schreiben<br/> | Die Partitions-GUID des Abonnenten.<br/>           |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




