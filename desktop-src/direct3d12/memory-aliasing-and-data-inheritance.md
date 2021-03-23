---
title: Speicher Aliasing und Datenvererbung
description: Die platzierte und die reservierte Ressource können den physischen Speicher innerhalb eines Heaps als Alias. Platzierte Ressourcen ermöglichen mehr Daten Vererbungs Szenarien als reservierte Ressourcen, wenn für den Heap das Shared-Flag festgelegt wurde oder wenn die Aliasing-Ressourcen vollständig definierte Speicher Layouts aufweisen.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cace5b5997e2a460406ae72abb247224886f3926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103401"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Speicher Aliasing und Datenvererbung

Die platzierte und die reservierte Ressource können den physischen Speicher innerhalb eines Heaps als Alias. Platzierte Ressourcen ermöglichen mehr Daten Vererbungs Szenarien als reservierte Ressourcen, wenn für den Heap das Shared-Flag festgelegt wurde oder wenn die Aliasing-Ressourcen vollständig definierte Speicher Layouts aufweisen.

-   [Aliasing](#memory-aliasing-and-data-inheritance)
-   [Datenvererbung](#data-inheritance)
-   [Verwandte Themen](#related-topics)

## <a name="aliasing"></a>Aliase

Zwischen der Verwendung von zwei Ressourcen, die denselben physischen Speicher aufweisen, muss eine Aliasing-Barriere ausgegeben werden, auch wenn keine Datenvererbung gewünscht wird. Einfache Verwendungs Modelle müssen zumindest die Ziel Ressource angeben, die an einem solchen Vorgang beteiligt ist. Weitere Details und erweiterte Verwendungs Modelle finden Sie unter " [**kreateplacedresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) ".

Nachdem auf eine Ressource zugegriffen wurde, werden alle Ressourcen, die den physischen Speicher für diese Ressource freigeben, ungültig, es sei denn, es ist eine Datenvererbung zulässig. Lesevorgänge für ungültig erklärt Ressourcen führen zu nicht definiertem Ressourcen Inhalt. Schreibvorgänge für ungültig erklärt Ressourcen führen auch zu nicht definiertem Ressourcen Inhalt, es sei denn, es gibt zwei Bedingungen:

-   Die Ressource verfügt weder über das D3D12- \_ \_ ressourcenflag \_ Allow \_ \_ Renderziel noch über das D3D12- \_ \_ ressourcenflag \_ Allow \_ tiefen \_ Schablone.
-   Der Schreibvorgang ist ein Kopier-oder Löschvorgang für eine gesamte untergeordnete Quelle oder Kachel. Die Kachel Initialisierung ist nur für Ressourcen verfügbar, bei denen eine Kachel mit 64-KB \_ -Kacheln nicht \_ definiert ist und die \_ Kachel Standard für 64 KB ist \_ \_ \_ .

Überlappende Invalidierungen sind auf kleinere Granularitäten beschränkt, wenn Layouts Informationen zu dem Speicherort an dem Speicherort der texusdaten bereitstellen und wenn sich Ressourcen in bestimmten Übergangs Barrieren befinden. Allerdings können die Invalidierungen nicht kleiner sein als die Granularitäten der Ressourcen Ausrichtung.

Die Granularität der Puffer Ausrichtung beträgt 64 KB, und eine größere Ausrichtungs Granularität hat Vorrang. Dies ist bei der Betrachtung von 4-KB-Texturen wichtig, da sich mehrere 4-KB-Texturen in einem Bereich von 64 KB befinden können, ohne einander zu überlappen Allerdings kann ein Puffer Aliasing desselben 64-KB-Bereichs nicht in Verbindung mit einer dieser 4-KB-Texturen verwendet werden. Die Anwendung kann den Zugriff auf den Puffer nicht zuverlässig von der Schnittmenge der 4-KB-Texturen behalten, da GPUs in einem nicht definierten Musterdaten mit einer Größe von 4 KB innerhalb des 64-KB-Bereichs schwenken dürfen.

64-KB \_ -Kachel "nicht \_ definiert" \_ , mit 64-KB \_ -Kacheln \_ Standard \_ -Swizzle und Zeilen \_ haupttextur Layouts wird der Anwendung mitgeteilt, welche sich überlappende Ausrichtungs Granularitäten Beispielsweise kann eine Anwendung ein 2D-Renderziel-Textur Array mit 2 Array Slices, einer einzelnen MIP-Ebene und der 64-KB- \_ Kachel nicht \_ definiertes \_ Swizzle-Layout erstellen. Angenommen, die Anwendung versteht, dass die einzelnen Array Segmente 100 64 KB-Kacheln belegen. Die Anwendung kann mit dem Array Slice 0 fortfahren und den Speicher entweder für einen ~ 6MB-Puffer, eine ~ 6MB-Textur mit nicht definiertem Layout usw. wieder verwenden. Nehmen Sie weiter an, dass die Anwendung nicht mehr die erste Kachel von Array Slice 1 benötigt. Anschließend könnte die Anwendung auch dann einen 64-KB-Puffer finden, bis das Rendering erneut die erste Kachel von Array Slice 1 erfordert. Die Anwendung muss eine vollständige Kachel löschen oder kopieren, um die erste Kachel erneut mit dem Textur Array zu verwenden.

Auch Texturen mit definierten Layouts haben immer noch problematische Fälle. Textur Ressourcen Größen können sich erheblich von der Berechnung der Anwendung selbst unterscheiden, da einige Adapter Architekturen zusätzlichen Arbeitsspeicher für Texturen zuweisen, um die effektive Bandbreite während allgemeiner renderingszenarios zu verringern. Alle Invalidierungen in dieser zusätzlichen Speicher Region bewirken, dass die gesamte Ressource ungültig wird. Weitere Informationen finden Sie unter [**getresourcezucationinfo**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo) .

## <a name="data-inheritance"></a>Datenvererbung

Platzierte Ressourcen ermöglichen die meisten Datenvererbung für Texturen, auch wenn nicht definierte Speicher Layouts vorhanden sind. Anwendungen können die Daten Vererbungs Funktionen, die freigegebene zugesicherte Ressourcen ermöglichen, imitieren, indem Sie zwei Texturen mit identischen Ressourcen Eigenschaften in demselben Offset in einem freigegebenen Heap suchen. Die gesamte Ressourcen Beschreibung muss identisch sein, einschließlich des optimierten Clear-Werts und des Typs der Methode zur Ressourcen Erstellung (platziert oder reserviert). Beide Ressourcen haben jedoch möglicherweise unterschiedliche anfängliche Übergangs Barrieren.

Reservierte Ressourcen ermöglichen die Datenvererbung pro Kachel. Einschränkungen sind jedoch häufig für den Zustand der Ressourcen Übergangs Barriere vorhanden.

Zum Erben von Daten müssen sich beide Ressourcen in einem kompatiblen Zustand der Ressourcen Übergangs Barriere befinden:

-   Bei Puffern, gleichzeitigen Zugriffs Texturen und plattformübergreifenden Texturen ist der Zustand des Ressourcen Übergangs nicht wichtig, und alle Zustände sind "kompatibel".
-   Für reservierte Texturen ohne vorherige Eigenschaften oder eine andere Datenvererbung pro Kachel durch eine Kachel mit 64 KB nicht \_ \_ definierte \_ Swizzle-oder 64-KB- \_ Kachel \_ Standard- \_ Swizzle muss der Zustand der Ressourcen Übergangs Barriere, einschließlich der Kachel, den gemeinsamen Status aufweisen.
-   Für alle anderen Texturen, bei denen die Ressourcen Beschreibungen genau übereinstimmen, muss der Status der Ressourcen Übergangs Barriere für jedes entsprechende Paar von unter Berichten wie folgt sein:
    -   Sie können den Status "Allgemein" aufweisen.
    -   Gleich sein, wenn der Zustand über das gleiche GPU-Schreib Flag verfügt.

Wenn die GPU Standard-Swizzle unterstützt, werden Puffer und standardswidingtexturen möglicherweise dem gleichen Speicher zugeordnet, und Sie erben Daten zwischen Ihnen. Die Anwendung kann texeln aus der Puffer Darstellung bearbeiten, da das standardmäßige Swizzle-Muster beschreibt, wie texeln im Arbeitsspeicher angeordnet werden. Das CPU-sichtbare Swizzle-Muster entspricht dem in Puffern angezeigten GPU-sichtbaren Swizzle-Muster.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Untergeordnete Zuordnung innerhalb von Heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




