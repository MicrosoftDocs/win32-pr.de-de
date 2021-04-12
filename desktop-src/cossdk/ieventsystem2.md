---
description: Wird vom Microsoft Internet Explorer-System Ereignis Benachrichtigungsdienst (Sens) verwendet, um auf den Ereignisdaten Speicher zuzugreifen. Diese Schnittstelle erweitert die ieventsystem-Schnittstelle.
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
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483598"
---
# <a name="ieventsystem2-interface"></a>IEventSystem2-Schnittstelle

Wird vom Microsoft Internet Explorer-System Ereignis Benachrichtigungsdienst (Sens) verwendet, um auf den Ereignisdaten Speicher zuzugreifen. Diese Schnittstelle erweitert die [**ieventsystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) -Schnittstelle.

## <a name="when-to-implement"></a>Gründe für die Implementierung

Sie müssen die **IEventSystem2** -Schnittstelle nicht implementieren. Ein vom System bereitgestelltes Ereignis Systemobjekt (CLSID \_ ceventsystem) implementiert **IEventSystem2**.

## <a name="when-to-use"></a>Verwendung

Wenn Sie "Sens" verwenden, können Sie die **IEventSystem2** -Methoden zum Hinzufügen und Entfernen von Objekten aus dem Ereignisspeicher und zum Abrufen von Objekten aus dem Ereignisspeicher verwenden.

Da [**ieventpublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) und das Verleger Objekt nicht mehr unterstützt werden, wird [**ieventobjectchange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) nicht in der [**changedpublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) -Methode aufgerufen.

## <a name="members"></a>Member

Die **IEventSystem2** -Schnittstelle erbt von **ieventsystem**. **IEventSystem2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IEventSystem2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                         | BESCHREIBUNG                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | Ruft die Versionsnummer des Ereignis Systems ab.<br/>                      |
| [**Verifytransientabonnenten**](ieventsystem2-verifytransientsubscribers.md) | Überprüft, ob alle vorübergehenden Abonnenten im Datenspeicher vorhanden sind.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ieventsystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

