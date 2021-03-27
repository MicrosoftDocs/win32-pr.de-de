---
title: Ebene 2
description: In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858355"
---
# <a name="tier-2"></a>Ebene 2

In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.

-   Hardware auf Featureebene 11,1.
-   Alle Features der vorherigen Ebene (ohne Einschränkungen der [Ebene 1](tier-1.md) ) sowie die Ergänzungen der folgenden Elemente:
-   Shaderanweisungen zum Spannen von Lod und zugeordneten Status Feedback sind verfügbar. Weitere Informationen finden Sie unter Verfügbarkeit von [HLSL-gekachelten Ressourcen](hlsl-tiled-resources-exposure.md).
-   Lesevorgänge von nicht zugeordneten Kacheln geben 0 (null) in allen nicht fehlenden Komponenten des Formats und die Standardeinstellung für fehlende Komponenten zurück.
-   Schreibvorgänge in nicht zugeordnete Kacheln werden nicht mehr in den Arbeitsspeicher aufgenommen, werden jedoch möglicherweise in Caches gespeichert, bei denen nachfolgende Lesevorgänge in die gleiche Adresse möglicherweise nicht abgerufen werden.
-   Bei der Textur Filterung mit einem Speicherplatz, der auf Kacheln von **null** und nicht **null** liegt, wird 0 (mit Standardwerten für fehlende Format Komponenten) für texeln auf **null** -Kacheln in den Gesamt Filter Vorgang einbezogen. Einige frühe Hardware erfüllt diese Anforderung nicht und gibt 0 (mit Standardwerten für fehlende Format Komponenten) für das vollständige Filterergebnis zurück, wenn eine texeln (mit einer Gewichtung ungleich null) auf eine **null** -Kachel fallen. Keine andere Hardware darf die Anforderung zum Einbeziehen aller (ungleich NULL gewichteten) texeln in den Filter Vorgang übersehen.
-   **Null** -texuszugriffe bewirken, dass der [**checkaccessfullymapping**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) -Vorgang für ein Textur Lesevorgang den Wert "false" zurückgibt. Dies ist unabhängig davon, wie das Ergebnis des Textur Zugriffs im Shader im Shader maskiert werden kann und wie viele Komponenten im Textur Format vorliegen (die Kombination aus, die den Anschein hat, dass auf die Textur nicht zugegriffen werden muss).
-   Ausrichtungs Einschränkungen für Standard Kachel Formen: bei MipMaps, bei denen mindestens eine Standard Kachel in allen Dimensionen ausgefüllt wird, wird garantiert die Standard-tiult verwendet, wobei der Rest als **Einheit als Einheit** in n Kacheln (der der Anwendung gemeldet wird) als gepackt betrachtet wird. Die Anwendung kann die N-Kacheln willkürlich nicht zusammenhängenden Positionen in einem Kachel Pool zuordnen, muss jedoch entweder alle oder keine der gepackten Kacheln zuordnen. Die MIP-Verpackung ist ein eindeutiger Satz von gepackten Kacheln pro Array Slice.
-   Die minimale/maximale Reduzierungs Filterung wird unterstützt. Informationen zur minimalen/maximalen Reduzierungs Filterung finden Sie unter [Kacheln von Funktionen für Textur Stichproben](tiled-resources-texture-sampling-features.md).
-   Für gekachelte Ressourcen mit allen Mipmaps, die kleiner als die Standard Kachel Größe in einer Dimension sind, darf die Array Größe nicht größer als 1 sein.
-   Einschränkungen für den Zugriff auf Kacheln, wenn doppelte Zuordnungen vorhanden sind, die unter [Kachel Zugriffs Einschränkungen mit doppelten Zuordnungen](tile-access-limitations-with-duplicate-mappings-.md)beschrieben werden, werden weiterhin angewendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tarife der Kachel "Ressourcen"](tiled-resources-features-tiers.md)
</dt> </dl>

 

 