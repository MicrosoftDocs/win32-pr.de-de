---
description: Direct3D 9 unterstützt Punkte, Linien, Dreiecke und Raster Primitive.
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: Higher-Order Primitives (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67767dd955fa5c0c5c21315d7c1c510de422870c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745561"
---
# <a name="higher-order-primitives-direct3d-9"></a>Higher-Order Primitives (Direct3D 9)

Direct3D 9 unterstützt Punkte, Linien, Dreiecke und Raster Primitive. Diese wurden erweitert, um eine Interpolations Erweiterung höher als linear zu unterstützen. Obwohl Dreiecke und Linien einen räumlichen Block aufweisen, werden Sie bisher mit linearer interpolung gerendert. In Direct3D 9 unterstützt Direct3D das Rendering dieser primitiven Typen in höherer Reihenfolge, bis zu Quintic, Interpolations. Außerdem wird jetzt ein neuer vier vierfach primitiver Typ unterstützt. Dieser neue Typ kann auch mit einer Interpolations höheren Reihenfolge gerendert werden. Diese Funktion wird hauptsächlich durch die Anforderungen für die Animation und das Rendering von Zeichen gesteuert. Sie kann auch für andere Oberflächen verwendet werden, wie z. b. ein Gebiet oder Wasser.

Primitive höherer Ordnung unterstützen Interpolationen höherer Ordnung, wenn Sie als Listen, Streifen, Lüfter oder indizierte Netze an die API übermittelt werden. Dies wird erreicht, indem zusätzliche Informationen verwendet werden, die in den Vertices selbst codiert sind. Normale Vektoren können z. b. verwendet werden, um tangential Flächen an den Scheitel Punkten zu definieren, um die kubische interpolung zu aktivieren. Die meisten Implementierungen unterstützen eine Interpolations Funktion mit höherer Reihenfolge durch Mosaik in planare Dreiecke. Der Mosaik Schritt wird logisch vor der Vertex-Shader-Stufe angewendet. Da die Vertex-Shader-API keine Semantik für die Eingabedaten zuordnet, wird ein spezieller Mechanismus bereitgestellt, um die vertexstreamkomponente zu identifizieren, die die Position darstellt, und optional den normalen Vektor. Alle anderen Komponenten werden entsprechend interpoliert.

In diesem Abschnitt werden primitive von höherer Ordnung eingeführt, und es wird erläutert, wie Sie in Ihren Anwendungen verwendet werden können. Die Informationen sind in folgende Themen unterteilt:

-   [Verbesserte Qualität durch Lösungs Erweiterung](#improved-quality-through-resolution-enhancement)
-   [Direkte Zuordnung von Spline-Based Tools](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>Verbesserte Qualität durch Lösungs Erweiterung

Aktuelle primitive sind nicht ideal für die Darstellung von glatten Oberflächen. Interpolations Methoden höherer Ordnung, wie z. b. Kubische Polynomen, ermöglichen genauere Berechnungen beim Rendern von Kurven Formen. Dies sorgt für mehr Realismus durch das reduzieren oder eliminieren von Elementen, die in den Fassaden Kanten oder in Glanz oberflächenbeleuchtung sichtbar sind. Wenn ein Mosaik Vorgang auf dem Chip durchgeführt wird, wirken sich die Mosaik Dreiecke nicht auf die Busbandbreite aus. In vielen Fällen kann ein wenig Mosaik Grad Verbesserungen bei der Bildqualität mit minimalen Auswirkungen auf die Leistung bereitstellen.

Direct3D 9 bietet eine einfache Möglichkeit, um die Lösungs Erweiterung auf Inhalte anzuwenden, die von vorhandenen Polygon orientierten Tools und Grafik Pipelines erstellt wurden. Die Anwendung muss nur eine gewünschte Mosaik Ebene bereitstellen und die Daten mithilfe der standardmäßigen Dreiecks Syntax übertragen, die normale Vektoren enthält.

## <a name="direct-mapping-from-spline-based-tools"></a>Direkte Zuordnung von Spline-Based Tools

Viele aktuelle Erstellungs Tools unterstützen Grundwerte höherer Ordnung, um leistungsfähigere Modellierungs Vorgänge zu ermöglichen, als bei planaren Dreieck-Meshes häufig bereitgestellt werden. Wenn effizient verwendet wird, damit die Anzahl der generierten Patches angemessen ist, können solche Tools Inhalte erzeugen, die direkt von der API gerendert werden können. Um diese Anforderung zu erfüllen, wurde ein neuer Einstiegspunkt hinzugefügt, der den eingehenden Scheitelpunkt Datenstrom als 2D-Array von Steuerungs Punkten interpretiert und die gewünschte Auflösung durchführt.

-   [Verwenden von Higher-Order primitiven (Direct3D 9)](using-higher-order-primitives.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 



