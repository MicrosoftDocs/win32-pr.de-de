---
description: Beschreibung der Möglichkeiten zum Verbessern der Leistung bei Verwendung der StylusInput-APIs (Application Programming Interfaces).
ms.assetid: 2a541715-2d9e-4eb2-ab60-ec95368fca5a
title: Überlegungen zur Leistung der StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721474f1e1097729246e5d497d20dcab868190a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759805"
---
# <a name="performance-considerations-for-the-stylusinput-api"></a>Überlegungen zur Leistung der StylusInput-API

In der folgenden Liste werden einige Möglichkeiten beschrieben, wie Sie die Leistung von Anwendungen verbessern können, die die StylusInput-APIs verwenden.

-   Verwenden Sie die Eigenschaft [Microsoft. StylusInput. IStylusSyncPlugin. DataInterest](/previous-versions/ms824752(v=msdn.10)) oder [Microsoft. StylusInput. IStylusAsyncPlugin. DataInterest](/previous-versions/ms824769(v=msdn.10)) , um nur die für Ihr Plug-in relevanten Daten zu abonnieren. Dadurch wird die Gesamtzahl der Methodenaufrufe verringert, die das [**RealTimeStylus**](realtimestylus-class.md) -Objekt vornimmt, und die Komplexität des Plug-ins wird reduziert. Das **RealTimeStylus** -Objekt überprüft nur die DataInterest-Eigenschaft, wenn das Plug-in angefügt wird.
-   Minimieren Sie die Komplexität synchrone Plug-ins. Synchrone Plug-ins, die in der Regel vom Thread des [**RealTimeStylus**](realtimestylus-class.md) -Objekts aufgerufen werden und zu Verzögerungen bei der frei Hand Eingabe beitragen können.
-   Ziehen Sie in Erwägung, das Plug-in asynchron zu gestalten. Wenn das Plug-in Komplex ist und der Warteschlange des [**RealTimeStylus**](realtimestylus-class.md) -Objekts benutzerdefinierte Daten hinzugefügt werden müssen, empfiehlt es sich, ein kaskadierenden- **RealTimeStylus** -Modell zu verwenden und das Plug-in zur synchronen Plug-in-Auflistung des sekundären **RealTimeStylus** -Objekts hinzuzufügen. Weitere Informationen zum kaskadierenden **RealTimeStylus** -Modell finden Sie [im kaskadierenden RealTimeStylus-Modell](the-cascaded-realtimestylus-model.md).

 

 
