---
description: Übersicht über Threadingüberlegungen bei der Verwendung der StylusInput-Api (Application Programming Interface).
ms.assetid: 5d98768a-c60b-4bb0-8640-9bf38254d41f
title: Threadingüberlegungen für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f9a26da86295a322d926278eda87388c0105132eafd2dfa3d7a9f6c6655e48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819640"
---
# <a name="threading-considerations-for-the-stylusinput-api"></a>Threadingüberlegungen für die StylusInput-API

Das [**RealTimeStylus-Objekt**](realtimestylus-class.md) ist für den Echtzeitzugriff auf den Datenstrom vom Tablettstift aus konzipiert. Plug-Ins, Objekte, die die [**IStylusSyncPlugin-**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) oder [**IStylusAsyncPlugin-Schnittstelle**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) implementieren, können einem **RealTimeStylus-Objekt** hinzugefügt werden. Synchrone Plug-Ins werden im Allgemeinen direkt vom **RealTimeStylus-Objekt** in einem Thread mit hoher Priorität aufgerufen, während asynchrone Plug-Ins im Allgemeinen für den Benutzeroberflächenthread der Anwendung aufgerufen werden. Erstellen oder verwenden Sie synchrone Plug-Ins für Aufgaben, die Echtzeitzugriff auf den Datenstrom erfordern und rechenintensiv sind, z. B. Paketfilterung. Erstellen oder verwenden Sie asynchrone Plug-Ins für Aufgaben, die keinen Echtzeitzugriff auf den Datenstrom erfordern, z. B. die Ink-Sammlung.

Da die Plug-In-Daten für die asynchrone Plug-In-Sammlung des [**RealTimeStylus-Objekts**](realtimestylus-class.md) in die Warteschlange eingereiht werden, empfangen asynchrone Plug-Ins möglicherweise Daten, bevor sie einen Aufruf der [RealTimeStylusDisabled-Methode](/previous-versions/ms824774(v=msdn.10)) empfangen, aber nachdem das **RealTimeStylus-Objekt** deaktiviert wurde. Beachten Sie, dass einige der Methoden und Eigenschaften des **RealTimeStylus-Objekts** eine Ausnahme auslösen, wenn das **RealTimeStylus-Objekt** deaktiviert ist.

Die folgenden [**IStylusSyncPlugin-Schnittstellenmethoden**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) können für einen anderen Thread als den Tablettstift-Datenthread aufrufen.

-   Die Methoden [RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) und [RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) werden für den Thread aufgerufen, der die [Enabled-Eigenschaft](/previous-versions/ms585380(v=vs.100)) des [**RealTimeStylus-Objekts**](realtimestylus-class.md) aktualisiert oder das Plug-In hinzufügt oder entfernt, während das **RealTimeStylus-Objekt** aktiviert ist.
-   Die [CustomStylusDataAdded-Methode](/previous-versions/ms824753(v=msdn.10)) wird für den Thread aufgerufen, der die [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) des [**RealTimeStylus-Objekts**](realtimestylus-class.md) aufruft.
-   Die [Error-Methode](/previous-versions/ms824754(v=msdn.10)) wird für den Thread aufgerufen, in dem das synchrone Plug-In ausgeführt wird, wenn es eine Ausnahme auslöst.

Verwenden Sie zum Interagieren mit Ihrer Anwendung über ein synchrones Plug-In die [AddCustomStylusDataToQueue-Methode](/previous-versions/ms825761(v=msdn.10)) des [**RealTimeStylus-Objekts,**](realtimestylus-class.md) und verarbeiten Sie die benutzerdefinierten Stiftdaten in einem Ihrer asynchronen Plug-Ins. Wenn Sie einen synchronen Aufruf eines anderen Threads über ein synchrones Plug-In vornehmen, können Sie das **RealTimeStylus-Objekt** und somit die Ink-Sammlung blockieren.

Bestimmte Aufgaben sind möglicherweise rechenintensiv, erfordern aber dennoch Echtzeitzugriff auf den Datenstrom des Tablettstifts, z. B. für die Erkennung von Gesten mit mehreren Tastatureingaben. Die StylusInput-APIs stellen ein kaskadiertes [**RealTimeStylus-Modell**](realtimestylus-class.md) bereit, mit dem Sie zwei **RealTimeStylus-Objekte** verwenden können, von denen jedes seine synchronen Plug-Ins aus verschiedenen Threads aufruft. Weitere Informationen zum kaskadierten **RealTimeStylus-Modell** finden Sie unter [Das kaskadierte RealTimeStylus-Modell.](the-cascaded-realtimestylus-model.md)

> [!Note]  
> Sie können das [**RealTimeStylus-Objekt**](realtimestylus-class.md) nicht an ein Fenster oder Steuerelement in einem anderen Prozess anfügen.

 

Weitere Informationen zu Threadingüberlegungen für den Tablet-PC im Allgemeinen finden Sie unter Überlegungen zum [Threading von Tablet-PCs.](tablet-pc-threading-considerations.md)

 

 
