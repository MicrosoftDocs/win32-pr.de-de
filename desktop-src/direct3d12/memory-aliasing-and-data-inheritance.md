---
title: Arbeitsspeicheraliasing und Datenvererbung
description: Platzierte und reservierte Ressourcen können einen Alias für physischen Speicher innerhalb eines Heaps verwenden. Platzierte Ressourcen ermöglichen mehr Datenvererbungsszenarien als reservierte Ressourcen, wenn auf dem Heap das freigegebene Flag festgelegt ist oder wenn die Ressourcen mit Alias über vollständig definierte Speicherlayouts verfügen.
ms.assetid: 53C5804B-0F81-41AF-83D2-A96DCDFDC94A
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b584ef95f4ee89bc98940c8407427203a19f55046134e1d3c15cb672fef8fef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460920"
---
# <a name="memory-aliasing-and-data-inheritance"></a>Arbeitsspeicheraliasing und Datenvererbung

Platzierte und reservierte Ressourcen können einen Alias für physischen Speicher innerhalb eines Heaps verwenden. Platzierte Ressourcen ermöglichen mehr Datenvererbungsszenarien als reservierte Ressourcen, wenn auf dem Heap das freigegebene Flag festgelegt ist oder wenn die Ressourcen mit Alias über vollständig definierte Speicherlayouts verfügen.

-   [Aliasing](#memory-aliasing-and-data-inheritance)
-   [Datenvererbung](#data-inheritance)
-   [Zugehörige Themen](#related-topics)

## <a name="aliasing"></a>Aliase

Zwischen der Verwendung von zwei Ressourcen, die denselben physischen Speicher gemeinsam nutzen, muss eine Aliasingbarriere ausgegeben werden, auch wenn die Datenvererbung nicht gewünscht ist. Einfache Verwendungsmodelle müssen mindestens die Zielressource bezeichnen, die an einem solchen Vorgang beteiligt ist. Weitere Informationen und erweiterte Verwendungsmodelle finden Sie unter [**CreatePlacedResource.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource)

Nachdem auf eine Ressource zugegriffen wurde, werden alle Ressourcen, die physischen Speicher gemeinsam mit dieser Ressource nutzen, ungültig, es sei denn, die Datenvererbung ist zulässig. Leses ungültiger Ressourcen führen zu nicht definierten Ressourceninhalten. Schreibvorgänge in ungültige Ressourcen führen auch zu nicht definierten Ressourceninhalten, es sei denn, es treten zwei Bedingungen auf:

-   Die Ressource verfügt weder über das D3D12-RESSOURCENFLAG ALLOW RENDER TARGET noch \_ \_ über das \_ \_ \_ D3D12 \_ RESOURCE FLAG ALLOW DEPTH \_ \_ \_ \_ STENCIL.
-   Der Schreibvorgang ist ein Kopier- oder Benachrichtigungsvorgang für eine gesamte Unterressource oder Kachel. Die Kachelin initialisierung ist nur für Ressourcen mit 64 KB \_ TILE \_ UNDEFINED \_ SWIZZLE und 64KB \_ TILE STANDARD \_ \_ SWIZZLE verfügbar.

Überlappende Invalidierungen werden auf kleinere Granularitäten abgestuft, wenn Layouts Informationen zum Speicherort der Texeldaten und zu ressourcen in bestimmten Übergangsbarrierenzuständen bereitstellen. Invalidierungen können jedoch nicht kleiner als granulare Ressourcenausrichtungen sein.

Eine Pufferausrichtungsgranularität beträgt 64 KB, und eine höhere Ausrichtungsgranularität hat Vorrang. Dies ist wichtig, wenn Sie 4-KB-Texturen in Betracht ziehen, da sich mehrere 4-KB-Texturen in einem 64-KB-Bereich befinden können, ohne sich überlappen zu müssen. Ein Puffer, der denselben 64-KB-Bereich als Alias verwendet, kann jedoch nicht zusammen mit einer dieser 4-KB-Texturen verwendet werden. Die Anwendung kann nicht zuverlässig den Zugriff auf den Puffer davon abhalten, die 4-KB-Texturen zu überschneiden, da GPUs 4-KB-Texturdaten innerhalb des 64-KB-Bereich in einem nicht definierten Muster schwenken dürfen.

64 KB \_ TILE \_ UNDEFINED \_ SWIZZLE, 64KB TILE STANDARD SWIZZLE und ROW MAJOR Texturlayouts informieren die Anwendung darüber, welche überlappenden \_ Ausrichtungsgranularitäten \_ \_ ungültig \_ wurden. Beispiel: Eine Anwendung kann ein 2D-Renderzieltexturarray mit zwei Arrayslices, einer einzelnen MIP-Ebene und dem 64-KB-TILE \_ \_ UNDEFINED \_ SWIZZLE-Layout erstellen. Angenommen, die Anwendung versteht, dass jeder Arrayslice 100 Kacheln mit 64 KB belegt. Die Anwendung kann auf die Verwendung von Arrayslice 0 verzichten und diesen Arbeitsspeicher entweder für einen Puffer von ~6 MB, eine ~6 MB-Textur mit nicht definiertem Layout usw. wiederverwendbar machen. Gehen Sie weiter davon aus, dass die Anwendung die erste Kachel des Arrayslices 1 nicht mehr benötigt. Anschließend könnte die Anwendung dort auch einen Puffer mit 64 KB finden, bis das Rendering erneut die erste Kachel des Arrayslices 1 erfordert. Die Anwendung müsste eine vollständige Kachel löschen oder kopieren, um die erste Kachel mit dem Texturarray erneut zu verwenden.

Selbst Texturen mit definierten Layouts haben jedoch weiterhin problematische Fälle. Die Größen von Texturressourcen können sich erheblich von dem unterscheiden, was die Anwendung selbst berechnen kann, da einige Adapterarchitekturen zusätzlichen Arbeitsspeicher für Texturen zuordnen, um die effektive Bandbreite in gängigen Renderingszenarien zu reduzieren. Alle Invalidierungen in diesem zusätzlichen Arbeitsspeicherbereich führen dazu, dass die gesamte Ressource ungültig wird. Weitere Informationen finden Sie unter [**GetResourceAllocationInfo.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getresourceallocationinfo)

## <a name="data-inheritance"></a>Datenvererbung

Platzierte Ressourcen ermöglichen die größte Datenvererbung für Texturen, auch bei nicht definierten Speicherlayouts. Anwendungen können die Datenvererbungsfunktionen imitieren, die freigegebene, für einen Committed bestimmte Ressourcen ermöglichen, indem sie zwei Texturen mit identischen Ressourceneigenschaften am gleichen Offset in einem freigegebenen Heap suchen. Die gesamte Ressourcenbeschreibung muss identisch sein, einschließlich des optimierten eindeutigen Werts und des Typs der Ressourcenerstellungsmethode (platziert oder reserviert). Aber beide Ressourcen haben möglicherweise unterschiedliche anfängliche Übergangsbarrierenzustände.

Reservierte Ressourcen ermöglichen die Datenvererbung pro Kachel. Für Zustände von Ressourcenübergangsbarrieren gelten jedoch häufig Einschränkungen.

Zum Erben von Daten müssen sich beide Ressourcen in einem kompatiblen Ressourcenübergangs-Barrierenzustand (Resource Transition Barrier, Barriere) befingen:

-   Bei Puffern, Texturen mit gleichzeitigem Zugriff und adapterübergreifenden Texturen ist der Zustand des Ressourcenübergangs nicht wichtig, und alle Zustände sind "kompatibel".
-   Für reservierte Texturen ohne die vorherigen Eigenschaften oder andere Datenvererbung pro Kachel über 64 KB \_ TILE \_ UNDEFINED \_ SWIZZLE oder 64KB \_ TILE STANDARD \_ \_ SWIZZLE muss der Zustand der Ressourcenübergangsbarriere einschließlich der Kachel den allgemeinen Zustand aufweisen.
-   Für alle anderen Texturen, bei denen die Ressourcenbeschreibungen genau übereinstimmen, muss der Zustand der Ressourcenübergangsbarriere für jedes entsprechende Paar von Unterressourcen:
    -   Sie haben den allgemeinen Zustand.
    -   Ist gleich, wenn der Zustand das gleiche GPU-Schreibflag auf sich hat.

Wenn die GPU Swizzle Standard unterstützt, können Puffer und Standard-Swizzle-Texturen als Alias für denselben Arbeitsspeicher verwendet werden und Daten zwischen ihnen erben. Die Anwendung kann Texel aus der Pufferdarstellung bearbeiten, da das standardmäßige Swizzle-Muster beschreibt, wie Texel im Arbeitsspeicher angelegt werden. Das CPU-sichtbare Swizzlemuster entspricht dem GPU-sichtbaren Swizzle-Muster in Puffern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterzuweisung innerhalb von Heaps](suballocation-within-heaps.md)
</dt> </dl>

 

 




