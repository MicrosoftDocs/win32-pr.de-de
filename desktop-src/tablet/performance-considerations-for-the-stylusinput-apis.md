---
description: Beschreibung der Möglichkeiten zum Verbessern der Leistung bei Verwendung der StylusInput-Anwendungsprogrammierschnittstellen (APPLICATION Programming Interfaces, APIs).
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Überlegungen zur Leistung der StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef40ab389687cd42ef516a61f61ab86a7eb79d4efac9ae6e9dd698e93e54bff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856492"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Überlegungen zur Leistung der StylusInput-API

In der folgenden Liste werden einige Möglichkeiten zur Verbesserung der Leistung von Anwendungen beschrieben, die die StylusInput-APIs verwenden.

-   Verwenden Sie die [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest-](/previous-versions/ms824752(v=msdn.10)) oder [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) -Eigenschaft, um nur die Daten zu abonnieren, die für Ihr Plug-In relevant sind. Dies reduziert die Gesamtanzahl der Methodenaufrufe, die das [**RealTimeStylus-Objekt**](realtimestylus-class.md) vornimmt, und verringert auch die Komplexität Ihres Plug-Ins. Das **RealTimeStylus-Objekt** überprüft nur die DataInterest-Eigenschaft, wenn das Plug-In angefügt ist.
-   Minimieren Sie die Komplexität synchroner Plug-Ins. Synchrone Plug-Ins werden im Allgemeinen vom Thread des [**RealTimeStylus-Objekts**](realtimestylus-class.md) aufgerufen und können zu Verzögerungen bei der Ink-Sammlung beitragen.
-   Erwägen Sie, das Plug-In asynchron zu gestalten. Wenn Ihr Plug-In komplex ist und der Warteschlange des [**RealTimeStylus-Objekts**](realtimestylus-class.md) benutzerdefinierte Daten hinzufügen muss, sollten Sie ein kaskadiertes **RealTimeStylus-Modell** verwenden und das Plug-In der synchronen Plug-In-Sammlung des sekundären **RealTimeStylus-Objekts** hinzufügen. Weitere Informationen zum kaskadierten **RealTimeStylus-Modell** finden Sie unter [Das kaskadierte RealTimeStylus-Modell.](the-cascaded-realtimestylus-model.md)

 

 
