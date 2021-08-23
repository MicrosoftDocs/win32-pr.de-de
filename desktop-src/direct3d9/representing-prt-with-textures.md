---
description: Das PRTDemo-Beispiel und der PRTCmdLine-Simulator, die im DirectX SDK enthalten sind, stellen Übertragungsvektoren an den Scheitellinien eines Gitters dar.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Darstellen von PRT mit Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e827e24258d75a91aa75c9eb51ed6563d476ab16f75fedc31a7071bca28a4a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797923"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Darstellen von PRT mit Texturen (Direct3D 9)

Das PRTDemo-Beispiel und der PRTCmdLine-Simulator, die im DirectX SDK enthalten sind, stellen Übertragungsvektoren an den Scheitellinien eines Gitters dar. Um das PRT-Signal genau darstellen zu können, kann dies Mosaiken erfordern, die für aktuelle Spiele möglicherweise unpraktisch sind. Die Darstellung von Übertragungsvektoren in Texturzuordnungen ist ein alternativer Ansatz, der unabhängig von der Gitternetzkomplexität die gleichen Datenkosten hat. Es gibt mehrere Möglichkeiten zum Generieren von Übertragungsvektortexturzuordnungen mithilfe der D3DX PRT-Bibliothek.

## <a name="precomputing-transfer-vectors"></a>Vorberechnung von Übertragungsvektoren

Ein Ansatz wäre das Ändern der PRTDemo- und PRTCmdLine-Beispiele, um einen Übertragungsvektor bei jedem Texel in einer Parametrisierung einer Oberfläche zu berechnen. Dazu ist Folgendes erforderlich:

1.  Ändern Sie den Aufruf von [**D3DXCreatePRTEngine,**](d3dxcreateprtengine.md) um Texturkoordinaten aus dem Gitternetz zu extrahieren (ExtractUVs muss **TRUE sein).**
2.  Ersetzen [**Sie D3DXCreatePRTBuffer-Aufrufe**](d3dxcreateprtbuffer.md) durch [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) mit der gleichen Texturgröße.

Alle ID3DXPRTEngine-Methoden funktionieren mit Simulationen pro Texel, mit Ausnahme von: ComputeBounceAdaptive, ComputeSSAdaptive, ComputeSS und ComputeDirectLightingSHAdaptive. Die Texturraumsimulation generiert zwar das richtige Ergebnis, kann aber häufig recht langsam sein, da sie wahrscheinlich Übertragungsvektoren mit hoher Dichte berechnen wird.

Ein weiterer Ansatz besteht in der Berechnung einer adaptiven PRT-Simulation pro Scheitelpunkt (mit Texturkoordinaten, die für die Pro-Texel-Daten verwendet werden) und anschließendes Aufrufen von [**ID3DXPRTEngine::ResampleBuffer**](id3dxprtengine--resamplebuffer.md) (mithilfe eines Ausgabepuffers, der mit [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) in der entsprechenden Auflösung erstellt wurde). Dies funktioniert mit allen D3DX PRT-Funktionen im SDK und kann häufig viel effizienter sein als das direkte Berechnen eines Übertragungspuffers pro Texel.

## <a name="runtime-calculations"></a>Laufzeitberechnungen

Wenn ein einzelner Cluster verwendet wird, können die Ergebnisse wie jede andere Textur gefiltert und Mip zugeordnet werden, und der Pixel-Shader ist identisch mit dem Vertex-Shadercode, der mit PRTDemo enthalten ist.

Wenn die Komprimierung mehrere Cluster generiert, können Sie die Daten nicht filtern oder mipmapieren, da Clusteringindizes nicht kontinuierlich sind. Hier sind einige Alternativen für die Verarbeitung von Daten mit mehreren Clustern:

-   Nehmen Sie die Filterung selbst im Pixel-Shader vor. Leider ist dies aus Leistungsgründen im Allgemeinen nicht praktikabel.
-   Wenn es sich bei den Texturen um texturen mit geringer Auflösung handelt, die keine Mip-Mapping-Texturen (d. h. Lichtkarten) sind, ist es höchstwahrscheinlich effizienter, die Beleuchtung direkt im Texturraum zu berechnen, wo keine Filterung erfolgt, und das Objekt mit einer schattierten Textur zu rendern. Dies ist im Wesentlichen eine dynamische Lichtkarte, die vollständig auf der GPU erstellt wird.
-   Wenn ein Texturatlas verwendet wird (siehe Verwenden von [UVAtlas (Direct3D 9)](using-uvatlas.md)), können Sie die Szene manuell clustern, indem Sie alle Übertragungsvektoren in einer verbundenen Komponente im Texturraum im selben Cluster haben. Auf diese Weise können Sie die Textur filtern, da sich alle Texel, auf die zugegriffen wird, durch Konstruktion im selben Cluster befingen. Die Cluster-ID für ein bestimmtes Gesicht kann vom Vertex-Shader propagiert werden.

Pixel-Shader verfügen über wesentlich weniger konstante Register, die nicht indiziert werden können, sodass sich der Pixel-Shader etwas von dem Vertex-Shader unterscheiden kann. Das Speichern pro Cluster funktioniert in einer dynamischen Textur mit niedriger Auflösung und die Verwendung von Texturlasten wäre die effizienteste Möglichkeit zum Rendern, wenn mehrere Cluster verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorausberechnungsübertragung der Radiance](precomputed-radiance-transfer.md)
</dt> <dt>

[PRT-Demobeispiel](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[PRT-Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



