---
description: Wird vom Microsoft Internet Explorer System Event Notification Service (SENS) für den Zugriff auf den Ereignisdatenspeicher verwendet. Diese Schnittstelle erweitert die IEventSystem-Schnittstelle.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: IEventSystem2-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6ecee3137750da9f86b61696799a3a7c6e7177beb2b92fb386712a6c90f69d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070600"
---
# <a name="ieventsystem2-interface"></a>IEventSystem2-Schnittstelle

Wird vom Microsoft Internet Explorer System Event Notification Service (SENS) für den Zugriff auf den Ereignisdatenspeicher verwendet. Diese Schnittstelle erweitert die [**IEventSystem-Schnittstelle.**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie müssen die **IEventSystem2-Schnittstelle nicht** implementieren. Ein vom System bereitgestelltes Ereignissystemobjekt (CLSID \_ CEventSystem) implementiert **IEventSystem2.**

## <a name="when-to-use"></a>Verwendung

Wenn Sie SENS verwenden, können Sie die Methoden von **IEventSystem2** aufrufen, um Dem Ereignisspeicher Objekte hinzuzufügen und daraus zu entfernen und Objekte aus dem Ereignisspeicher zu erhalten.

Da [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) und das Publisher-Objekt nicht mehr unterstützt werden, [**wird IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) für die [**ChangedPublisher-Methode nicht aufgerufen.**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher)

## <a name="members"></a>Member

Die **IEventSystem2-Schnittstelle** erbt von **IEventSystem**. **IEventSystem2** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEventSystem2-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**Getversion**](ieventsystem2-getversion.md)                                 | Ruft die Versionsnummer des Ereignissystems ab.<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | Überprüft das Vorhandensein aller vorübergehenden Abonnenten im Datenspeicher.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

