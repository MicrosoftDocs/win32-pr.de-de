---
description: Benachrichtigung zum Entfernen von Geräten
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Benachrichtigung zum Entfernen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c84fa280e0adbc1d0eec9043fbb2f1446487f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958115"
---
# <a name="device-removal-notification"></a>Benachrichtigung zum Entfernen von Geräten

Wenn der Benutzer ein Plug & Play Gerät entfernt, das im Diagramm verwendet wurde, stellt der Filter Graph-Manager ein Ereignis für ein Ereignis mit dem Ereignis " [**EC- \_ Gerät \_**](ec-device-lost.md) " Wenn das Gerät wieder verfügbar wird, sendet der Filter Graph-Manager ein anderes Ereignis für das Ereignis " **EC- \_ Gerät \_** ". Der vorherige Status des Erfassungs Filters ist jedoch nicht mehr gültig. Die Anwendung muss das Diagramm neu erstellen, damit das Gerät verwendet werden soll.

DirectShow sendet kein Ereignis, wenn ein neues Gerät angeschlossen ist. Um zu erfahren, wann ein neues Gerät verfügbar ist, kann die Anwendung die Nachrichten des WM- \_ devicechange-Fensters überwachen. Weitere Informationen finden Sie unter "Geräteverwaltung" in der Platform SDK-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



