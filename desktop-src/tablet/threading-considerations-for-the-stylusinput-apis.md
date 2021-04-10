---
description: Übersicht über Überlegungen zum Threading bei Verwendung der StylusInput-API (Application Programming Interface).
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Threading Überlegungen für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530ac95fdf0e74e30c83a437b6ed573d03bb2c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865288"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Threading Überlegungen für die StylusInput-API

Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt dient zum Bereitstellen von Echtzeitzugriff auf den Datenstrom vom Tablettstift. Plug-ins, Objekte, die die [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -oder [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) -Schnittstelle implementieren, können einem **RealTimeStylus** -Objekt hinzugefügt werden. Synchrone Plug-ins werden im allgemeinen direkt durch das **RealTimeStylus** -Objekt in einem Thread mit hoher Priorität aufgerufen, während asynchrone Plug-ins im Allgemeinen für den Benutzeroberflächen Thread der Anwendung aufgerufen werden. Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom benötigen und Rechen mäßig nicht anspruchsvoll sind (z. b. Paketfilterung). Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom benötigen, z. b. eine frei Hand Auflistung.

Da die Plug-in-Daten für die asynchrone Plug-in-Auflistung des [**RealTimeStylus**](realtimestylus-class.md) -Objekts in die Warteschlange eingereiht werden, empfangen asynchrone Plug-ins möglicherweise Daten, bevor Sie einen Aufrufe **an die** zugehörige [realtimestylusdeaktivierte](/previous-versions/ms824774(v=msdn.10)) Methode erhalten. Beachten Sie, dass einige der Methoden und Eigenschaften des **RealTimeStylus** -Objekts eine Ausnahme auslösen, wenn das **RealTimeStylus** -Objekt deaktiviert ist.

Die folgenden [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) -Schnittstellen Methoden können für einen anderen Thread als den Tablet Pen-Datenthread aufgerufen werden.

-   Die Methoden [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) und [realtimestylusdeaktiviert](/previous-versions/ms824757(v=msdn.10)) werden für den Thread aufgerufen, der die [aktivierte](/previous-versions/ms585380(v=vs.100)) Eigenschaft des [**RealTimeStylus**](realtimestylus-class.md) -Objekts aktualisiert oder das Plug-in hinzufügt, während das **RealTimeStylus** -Objekt aktiviert ist.
-   Die [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) -Methode wird für den Thread aufgerufen, der die [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode des [**RealTimeStylus**](realtimestylus-class.md) -Objekts aufruft.
-   Die [Error](/previous-versions/ms824754(v=msdn.10)) -Methode wird für den Thread aufgerufen, auf dem das synchrone Plug-in ausgeführt wird, wenn eine Ausnahme ausgelöst wird.

Verwenden Sie zum interagieren mit der Anwendung über ein synchrones Plug-in die [AddCustomStylusDataToQueue](/previous-versions/ms825761(v=msdn.10)) -Methode des [**RealTimeStylus**](realtimestylus-class.md) -Objekts, und behandeln Sie die benutzerdefinierten Tablettstiftdaten in einem ihrer asynchronen Plug-ins. Wenn Sie von einem synchronen Plug-in einen synchronen Rückruf an einen anderen Thread durchführen, können Sie das **RealTimeStylus** -Objekt blockieren und somit die frei Hand Auflistung blockieren.

Bestimmte Aufgaben sind möglicherweise Rechen anspruchvoll, erfordern aber trotzdem Echtzeitzugriff auf den Datenstrom des Tablet-Stifts, wie z. b. für die Erkennung von Zeitgeber-Gesten. Die StylusInput-APIs bieten ein kaskadierenden [**RealTimeStylus**](realtimestylus-class.md) -Modell, mit dem Sie zwei **RealTimeStylus** -Objekte verwenden können, von denen jedes die synchronen Plug-ins aus unterschiedlichen Threads aufruft. Weitere Informationen zum kaskadierenden **RealTimeStylus** -Modell finden Sie [im kaskadierenden RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

> [!Note]  
> Das [**RealTimeStylus**](realtimestylus-class.md) -Objekt kann nicht an ein Fenster oder ein Steuerelement in einem anderen Prozess angefügt werden.

 

Weitere Informationen zu Threading Überlegungen für den Tablet PC im Allgemeinen finden Sie unter [Überlegungen zum Tablet PC-Threading](tablet-pc-threading-considerations.md) .

 

 
