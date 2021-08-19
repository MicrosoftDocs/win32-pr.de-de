---
description: Benachrichtigung zum Entfernen von Geräten
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Benachrichtigung zum Entfernen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3cc73aba6ad02eb1dfba095b6f45b9fa6c067c51dbe165f4ded86141dae1c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052020"
---
# <a name="device-removal-notification"></a>Benachrichtigung zum Entfernen von Geräten

If the user removes a Plug and Play device that the graph was using, the filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event. Wenn das Gerät wieder verfügbar ist, sendet der Filtergraph-Manager ein weiteres **EC \_ DEVICE \_ LOST-Ereignis.** Der vorherige Zustand des Erfassungsfilters ist jedoch nicht mehr gültig. Die Anwendung muss das Diagramm neu erstellen, um das Gerät zu verwenden.

DirectShow sendet kein Ereignis, wenn ein neues Gerät angeschlossen ist. Um zu erfahren, wann ein neues Gerät verfügbar ist, kann die Anwendung WM \_ DEVICECHANGE-Fenstermeldungen überwachen. Weitere Informationen finden Sie unter "Geräteverwaltung" in der Dokumentation zum Plattform-SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



