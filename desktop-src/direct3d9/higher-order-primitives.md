---
description: Direct3D 9 unterstützt Punkte, Linien, Dreiecke und Rasterprimitive.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Higher-Order Primitive (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36ee67cfe4d4a802303091288f3906778e6cb3cdc1ad811602a80bc161d0a1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122121"
---
# <a name="higher-order-primitives-direct3d-9"></a>Higher-Order Primitive (Direct3D 9)

Direct3D 9 unterstützt Punkte, Linien, Dreiecke und Rasterprimitive. Diese wurden erweitert, um interpolation höherer Ordnung über linear hinaus zu unterstützen. Obwohl Dreiecke und Linien eine räumliche Vergrößerung aufweisen, wurden sie bisher beide mit linearer Interpolation gerendert. In Direct3D 9 unterstützt Direct3D das Rendern dieser primitiven Typen mit höherer Reihenfolge, bis hin zur interpolischen Interpolation. Darüber hinaus wird jetzt ein neuer primitiver Quad-Typ unterstützt. Dieser neue Typ kann auch mit interpolation höherer Ordnung gerendert werden. Dieses Feature basiert in erster Linie auf den Anforderungen für Die Animation und das Rendern von Zeichen. Sie kann auch für andere Oberflächen wie Gelände oder Wasser verwendet werden.

Primitive höherer Ordnung unterstützen interpolation höherer Ordnung, wenn sie an die API als Listen, Strips, Lüfter oder indizierte Gitternetze übertragen werden. Dies wird erreicht, indem zusätzliche Informationen verwendet werden, die in den Scheitelpunkten selbst codiert sind. Beispielsweise können normale Vektoren verwendet werden, um Tangentenebenen an den Scheitelpunkten zu definieren, um kubische Interpolation zu ermöglichen. Die meisten Implementierungen unterstützen die Interpolation höherer Ordnung durch Mosaik in planare Dreiecke. Der Mosaikschritt wird logisch vor der Vertex-Shaderphase angewendet. Da die Vertex-Shader-API keine Semantik für ihre Eingabedaten erzwingt, wird ein spezieller Mechanismus bereitgestellt, um die Vertexstreamkomponente, die die Position darstellt, und optional den normalen Vektor zu identifizieren. Alle anderen Komponenten werden entsprechend interpoliert.

In diesem Abschnitt werden Primitive höherer Ordnung vorgestellt und erläutert, wie sie in Ihren Anwendungen verwendet werden können. Die Informationen sind in die folgenden Themen unterteilt.

-   [Verbesserte Qualität durch Auflösungserweiterung](#improved-quality-through-resolution-enhancement)
-   [Direkte Zuordnung von Spline-Based Tools](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Verbesserte Qualität durch Auflösungserweiterung

Aktuelle Primitive eignen sich nicht ideal für die Darstellung von weichen Oberflächen. Interpolationsmethoden höherer Ordnung, z. B. kubische Polynome, ermöglichen genauere Berechnungen beim Rendern von gekrümmten Formen. Dies sorgt für mehr Realität, indem Facetingartefakte reduziert oder beseitigt werden, die an Kanten oder an der Beleuchtung von Glanzoberflächen sichtbar sind. Darüber hinaus wirken sich die Mosaikdreiecke nicht auf die Busbandbreite aus, wenn ein Mosaik auf dem Chip auftritt. In vielen Fällen kann ein kleiner Teil des Mosaiks Verbesserungen der Imagequalität mit minimalen Auswirkungen auf die Leistung ermöglichen.

Direct3D 9 bietet eine einfache Möglichkeit zum Anwenden der Auflösungserweiterung auf Inhalte, die von vorhandenen polygonorientierten Tools und Grafikpipelines erstellt wurden. Die Anwendung muss nur einen gewünschten Mosaikgrad bereitstellen und die Daten mithilfe der Standarddreiecksyntax übertragen, die normale Vektoren enthält.

## <a name="direct-mapping-from-spline-based-tools"></a>Direkte Zuordnung von Spline-Based Tools

Viele aktuelle Erstellungstools unterstützen primitive Typen höherer Ordnung, um leistungsfähigere Modellierungsvorgänge zu ermöglichen, als bei planaren Dreiecksgittermodellen üblicherweise bereitgestellt werden. Bei effizienter Verwendung, sodass die Anzahl der generierten Patches angemessen ist, können solche Tools Inhalte erzeugen, die direkt von der API gerendert werden können. Um diese Anforderung zu erfüllen, wurde ein neuer Einstiegspunkt hinzugefügt, der den eingehenden Scheitelpunktdatenstrom als ein 2D-Array von Kontrollpunkten interpretiert und mit der gewünschten Auflösung zusammenfügt.

-   [Verwenden von Higher-Order Primitiven (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 



