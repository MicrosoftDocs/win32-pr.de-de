---
description: Das prtdemo-Beispiel und der prtcmdline-Simulator, die im DirectX SDK enthalten sind, stellen Übertragungs Vektoren an den Scheitel Punkten eines Netzes dar.
ms.assetid: cee049e8-3245-4fce-ab2f-ba251eacc72a
title: Darstellen von PRT mit Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4647cfc85451ede9507e007ed556a203a3cd890a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213978"
---
# <a name="representing-prt-with-textures-direct3d-9"></a>Darstellen von PRT mit Texturen (Direct3D 9)

Das prtdemo-Beispiel und der prtcmdline-Simulator, die im DirectX SDK enthalten sind, stellen Übertragungs Vektoren an den Scheitel Punkten eines Netzes dar. Damit das PRT-Signal genau dargestellt werden kann, ist dies möglicherweise ein Mosaik, das für aktuelle Spiele nicht praktikabel ist. Das darstellen von Übertragungs Vektoren in Textur Karten ist ein alternativer Ansatz, bei dem die gleichen Datenkosten unabhängig von der Mesh-Komplexität entstehen. Es gibt mehrere Möglichkeiten, Übertragungs Vektor-Textur Zuordnungen mithilfe der D3DX PRT-Bibliothek zu generieren.

## <a name="precomputing-transfer-vectors"></a>Vorab berechnen von Übertragungs Vektoren

Ein Ansatz wäre das Ändern der prtdemo-und prtcmdline-Beispiele, um bei jeder textrisierung einer Oberfläche einen Übertragungs Vektor zu berechnen. Gehen Sie dazu wie folgt vor:

1.  Ändern Sie den [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) -Aufrufwert, um Texturkoordinaten aus dem Mesh zu extrahieren (extractuvs müssen **true** sein).
2.  Ersetzen Sie [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) -Aufrufe durch [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) , indem Sie die gleiche Textur Größe verwenden.

Alle ID3DXPRTEngine-Methoden können mit Ausnahme von computebounceadaptive, computessadaptive, computess und computedirectlightingshadaptive mit pro-texsimulationen verwendet werden. Während die Textur Raumsimulation das richtige Ergebnis generiert, kann Sie häufig recht langsam sein, da Sie höchstwahrscheinlich Übertragungs Vektoren mit hoher Dichte berechnen wird.

Ein anderer Ansatz ist die Berechnung einer adaptiven pro-Vertex-PRT-Simulation (mit Texturkoordinaten, die für die pro-tex-Daten verwendet werden) und anschließendem Aufrufs von [**ID3DXPRTEngine:: resamplebuffer**](id3dxprtengine--resamplebuffer.md) (mithilfe eines Ausgabepuffers, der mit [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md) bei entsprechender Auflösung erstellt wurde). Dies funktioniert mit allen D3DX PRT-Funktionen im SDK und ist häufig viel effizienter als das direkte Berechnen eines pro-texübertragungs Puffers.

## <a name="runtime-calculations"></a>Lauf Zeit Berechnungen

Wenn ein einzelner Cluster verwendet wird, können die Ergebnisse gefiltert und MIP-zugeordnet werden, wie jede andere Textur, und der Pixelshader ist identisch mit dem Vertex-Shader-Code, der mit prtdemo ausgeliefert wird.

Wenn bei der Komprimierung mehrere Cluster generiert werden, können die Daten nicht gefiltert oder falsch zugeordnet werden, da Clustering-Indizes nicht kontinuierlich sind. Im folgenden finden Sie einige Alternativen zur Verarbeitung von multiclusterdaten:

-   Führen Sie den gesamten Filter im Pixel-Shader aus. Leider ist dies aus Leistungsgründen in der Regel unpraktisch.
-   Wenn es sich bei den Texturen um nicht MIP-zugeordnete Texturen mit geringer Auflösung handelt (d. h. Licht Maps), ist es höchstwahrscheinlich effizienter, die Beleuchtung direkt im Textur Bereich zu berechnen, wobei keine Filterung stattfindet, und das Objekt mit einer schattierten Textur zu Rendering. Dabei handelt es sich im Wesentlichen um eine dynamische lichtkarte, die vollständig auf der GPU erstellt wird.
-   Wenn ein Textur Atlas verwendet wird (siehe [Verwenden von uvatlas (Direct3D 9)](using-uvatlas.md)), können Sie die Szene manuell gruppieren, indem Sie alle Übertragungs Vektoren in einer verbundenen Komponente im Textur Raum im gleichen Cluster befinden. Auf diese Weise können Sie die Textur filtern, da sich alle zugänglichen texeln durch die Konstruktion im gleichen Cluster befinden würden. Die Cluster-ID für eine bestimmte Fläche kann vom Vertexshader weitergegeben werden.

Pixel-Shader haben weitaus weniger Konstante Register, die nicht indiziert werden können. Daher unterscheidet sich der Pixelshader etwas von dem Vertexshader. Das Speichern der pro-Cluster-Arbeit in einer dynamischen Textur mit niedriger Auflösung und die Verwendung von Textur Ladungen wäre die effizienteste Methode zum Rendering, wenn mehrere Cluster verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Voraus berechnete Strahlungs Übertragung](precomputed-radiance-transfer.md)
</dt> <dt>

[Beispiel für eine PRT-Demo](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx)
</dt> <dt>

[PRT-Simulator (prtcmdline.exe)](https://msdn.microsoft.com/library/Ee418766(v=VS.85).aspx)
</dt> </dl>

 

 



