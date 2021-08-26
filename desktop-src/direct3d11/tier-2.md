---
title: Ebene 2
description: In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f5a5b018e5e48e6b2a1b86771b925cb88cf070ecd2b1303d359640eac565bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027790"
---
# <a name="tier-2"></a>Ebene 2

In diesem Abschnitt wird die Unterstützung der Ebene 2 beschrieben.

-   Hardware mindestens auf Featureebene 11.1.
-   Alle Features des vorherigen Tarifs (ohne spezifische Einschränkungen der [Ebene 1)](tier-1.md) sowie die Ergänzungen in den folgenden Elementen:
-   Shaderanweisungen zum Klammern von LOD- und zugeordneten Statusfeedbacks sind verfügbar. Weitere Informationen finden Sie unter [HLSL-Kachelressourcen.](hlsl-tiled-resources-exposure.md)
-   Lesefunktionen von nicht zugeordneten Kacheln geben 0 in allen nicht fehlenden Komponenten des Formats und den Standardwert für fehlende Komponenten zurück.
-   Schreibvorgänge in nicht zugeordnete Kacheln werden nicht mehr in den Arbeitsspeicher übertragen, können aber in Caches enden, die nachfolgende Lesevorgänge an dieselbe Adresse möglicherweise oder nicht aufnehmen.
-   Texturfilterung mit einem Fußabdruck, der **NULL-** und **Nicht-NULL-Kacheln** umgeht, trägt 0 (mit Standardwerten für fehlende Formatkomponenten) für Texel auf **NULL-Kacheln** zum gesamten Filtervorgang bei. Einige frühe Hardwarekomponenten erfüllen diese Anforderung nicht und geben 0 (mit Standardwerten für fehlende Formatkomponenten) für das vollständige Filterergebnis zurück, wenn Texel (mit einer Gewichtung ungleich null) auf eine **NULL-Kachel** fallen. Keine andere Hardware darf die Anforderung verfehlen, alle (nicht mit Null gewichteten) Texel in den Filtervorgang einzubeziehen.
-    NULL-Texelzugriffe bewirken, dass der [**CheckAccessFullyMapped-Vorgang**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) für das Statusfeedback für eine gelesene Textur FALSE zurückgibt. Dies ist unabhängig davon, wie das Texturzugriffsergebnis im Shader maskiert werden kann und wie viele Komponenten im Texturformat vorliegen (die Kombination davon kann den Anschein haben, dass auf die Textur nicht zugegriffen werden muss).
-   Ausrichtungseinschränkungen für Standardkachelformen: Mipmaps, die mindestens eine Standardkachel in allen Dimensionen füllen, verwenden garantiert die Standardkachel, wobei der Rest als **Einheit** in N Kacheln gepackt wird (N wird der Anwendung gemeldet). Die Anwendung kann die N Kacheln beliebig unzusammenhängenden Positionen in einem Kachelpool zuordnen, muss jedoch entweder alle oder keine der gepackten Kacheln zuordnen. Die Mip-Komprimierung ist ein eindeutiger Satz gepackter Kacheln pro Arrayslice.
-   Die Filterung der minimalen/maximalen Reduzierung wird unterstützt. Informationen zur Filterung der minimalen/maximalen Reduzierung finden Sie unter [Textursamplingfeatures für Kachelressourcen.](tiled-resources-texture-sampling-features.md)
-   Gekachelte Ressourcen mit Mipmaps, die in einer Dimension kleiner als die Standardkachelgröße sind, dürfen keine Arraygröße größer als 1 aufweisen.
-   Einschränkungen für den Zugriff auf Kacheln bei doppelten Zuordnungen, die unter Einschränkungen des [Kachelzugriffs mit doppelten Zuordnungen](tile-access-limitations-with-duplicate-mappings-.md)beschrieben werden, gelten weiterhin.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Features-Ebenen für gekachelte Ressourcen](tiled-resources-features-tiers.md)
</dt> </dl>

 

 