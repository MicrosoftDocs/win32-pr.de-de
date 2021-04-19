---
description: In diesem Abschnitt wird ein Teil einer Beispielanwendung untersucht, die sehr langsam über das Netzwerk ausgeführt wird. In diesem Abschnitt werden Änderungen am ursprünglichen Code vorgenommen, um die Leistung zu verbessern.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Verbessern einer langsamen Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360036"
---
# <a name="improving-a-slow-application"></a>Verbessern einer langsamen Anwendung

In diesem Abschnitt wird ein Teil einer Beispielanwendung untersucht, die sehr langsam über das Netzwerk ausgeführt wird. In diesem Abschnitt werden Änderungen am ursprünglichen Code vorgenommen, um die Leistung zu verbessern.

Das Mock-Beispiel ist der aktualisierte Teil für ein Spiel namens "Life". Die Anwendung wird so geschrieben, dass der Client die Berechnungen für die Updates ausführt und Sie an den Server sendet. Der Server zeigt dann das resultierende Lebensfeld an. Bei der Ausgabe des Clients handelt es sich um einen Bytestream, der in dreies (dreiplets) gruppiert ist, wobei jedes einzelne Paar ein einzelnes Zellen Update darstellt. Die Bytes im Dreieck stellen die Zeile, Spalte und den Wert für die Zelle dar.

Dieses Beispiel beginnt als absichtlich schlechte Anwendung, die die Baseline bietet, von der Leistungsverbesserungen veranschaulicht werden können. Von dort wird der Code dreimal verbessert, um verschiedene Probleme zu beheben, die sich auf die Leistung auswirken. Diese Beispiele sollten in der richtigen Reihenfolge gelesen werden, da sich jede Iterations Zeit auf der vorherigen Version verbessert.

Der grundlegende Code und die Revisionen, die diesen Code verbessern, lauten wie folgt:

-   [Baselineversion: eine sehr schlechte leistungsfähige Anwendung](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revision 1: Bereinigen der offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
-   [Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revision 3: komprimierte Block-Sendevorgang](revision-3-compressed-block-send-2.md)
-   [Zukünftige Verbesserungen](future-improvements-2.md)

> [!WARNING]
> Die ersten Beispiele der Anwendung sorgen für eine absichtlich schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen. Verwenden Sie diese Codebeispiele nicht in Ihrer Anwendung. Sie dienen nur zur Veranschaulichung.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsfähige Windows Sockets-Anwendungen](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



