---
description: In diesem Abschnitt wird ein Teil einer Beispielanwendung untersucht, die sehr langsam über das Netzwerk betrieben wird. In diesem Abschnitt werden Änderungen am ursprünglichen Code vorgenommen, um die Leistung zu verbessern.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Verbessern einer langsamen Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff8f996267328805dc120d39218784a08383fb68ae9f6927e8983b6e1bec2d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097890"
---
# <a name="improving-a-slow-application"></a>Verbessern einer langsamen Anwendung

In diesem Abschnitt wird ein Teil einer Beispielanwendung untersucht, die sehr langsam über das Netzwerk betrieben wird. In diesem Abschnitt werden Änderungen am ursprünglichen Code vorgenommen, um die Leistung zu verbessern.

Das Modellbeispiel ist der aktualisierte Teil für ein Spiel namens Life. Die Anwendung wird so geschrieben, dass der Client die Berechnungen für die Updates ausführt und sie an den Server sendet. Der Server zeigt dann das resultierende Life-Feld an. Die Ausgabe des Clients ist ein Bytestream, der in Dreiergruppen (Triplets) gruppiert ist, die jeweils eine Zellenaktualisierung darstellen. Die Bytes im Triplet stellen die Zeile, spalte bzw. den Wert für die Zelle dar.

Dieses Beispiel beginnt mit einer absichtlich leistungsstärksten Anwendung, die die Grundlage für Leistungsverbesserungen bildet. Von dort aus wird der Code dreimal verbessert, um verschiedene Probleme zu beheben, die sich auf die Leistung auswirken. Diese Beispiele sollten in der Reihenfolge gelesen werden, da sich jede Iteration gegenüber der vorherigen Version verbessert.

Der Baselinecode und die Revisionen, die diesen Code verbessern, sind die folgenden:

-   [Baselineversion: Eine Anwendung mit sehr schlechter Leistung](the-baseline-version-a-very-poor-performing-application-2.md)
-   [Revision 1: Bereinigen des offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
-   [Revision 2: Neugestaltung für weniger Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
-   [Revision 3: Compressed Block Send](revision-3-compressed-block-send-2.md)
-   [Zukünftige Verbesserungen](future-improvements-2.md)

> [!WARNING]
> Die ersten Beispiele der Anwendung bieten absichtlich schlechte Leistung, um leistungsverbesserungen zu veranschaulichen, die durch Codeänderungen möglich sind. Verwenden Sie diese Codebeispiele nicht in Ihrer Anwendung. sie dienen nur zur Veranschaulichung.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hochleistungsanwendungen Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



