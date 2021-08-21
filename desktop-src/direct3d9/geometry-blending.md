---
description: Direct3D ermöglicht es einer Anwendung, die Realität ihrer Szenen zu erhöhen, indem segmentierte polygonale Objekte , insbesondere Zeichen, gerendert werden, die über nahtlos verblendete Fugen verfügen.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Geometriemischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71bb449b592c69ae2cf41487aef229718149eb4c1465d90f8b358d30458b69c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122176"
---
# <a name="geometry-blending-direct3d-9"></a>Geometriemischung (Direct3D 9)

Direct3D ermöglicht es einer Anwendung, die Realität ihrer Szenen zu erhöhen, indem segmentierte polygonale Objekte , insbesondere Zeichen, gerendert werden, die über nahtlos verblendete Fugen verfügen. Diese Effekte werden häufig als Skinning bezeichnet. Das System erreicht diesen Effekt, indem es zusätzliche Welttransformationsmatrizen auf einen einzelnen Satz von Scheitelpunkten anwendet, um mehrere Ergebnisse zu erstellen, und dann eine lineare Mischung zwischen den resultierenden Scheitelpunkten durchführt, um einen einzelnen Satz von Geometrien für das Rendering zu erstellen. Die folgende Abbildung einer Banane zeigt diesen Prozess.

![Abbildung des Prozesses zum Mischen von zwei Objekten mit der Textur der Textur "Banane"](images/geometry-blend.png)

Die obige Abbildung zeigt, wie Sie sich den Geometry-Blending-Prozess vorstellen können. In einem einzigen Renderingaufruf nimmt das System die Scheitelpunkte für die Banane entgegen, transformiert sie zweimal – einmal ohne Änderung und einmal mit einer einfachen Drehung – und kombiniert die Ergebnisse, um eine Leichterte zu erzeugen. Das System kombiniert die Scheitelpunktposition sowie die Scheitelpunktnorm normal, wenn die Beleuchtung aktiviert ist. Anwendungen sind nicht auf zwei Mischungspfade beschränkt: Direct3D kann Geometrie zwischen bis zu vier Weltmatrizen kombinieren, einschließlich der Standard-Weltmatrix [**D3DTS \_ WORLD**](d3dts-world.md).

> [!Note]
>
> Wenn die Beleuchtung aktiviert ist, werden Scheitelpunktnormalen durch eine entsprechende umgekehrte Weltansichtsmatrix transformiert, die auf die gleiche Weise gewichtet wird wie die Scheitelpunktpositionsberechnungen. Das System normalisiert den resultierenden Normalvektor, wenn der D3DRS \_ NORMALIZENORMALS-Renderzustand auf **TRUE** festgelegt ist.

 

Ohne Geometriemischung werden dynamische artikulierte Modelle häufig in Segmenten gerendert. Betrachten Sie beispielsweise ein 3D-Modell des menschlichen Armes. In der einfachsten Ansicht hat ein Arm zwei Teile: den oberen Arm, der mit dem Körper verbunden ist, und den unteren Arm, der mit der Hand verbunden ist. Die beiden sind am Ellenbogen verbunden, und der untere Arm dreht sich an diesem Punkt. Eine Anwendung, die einen Arm rendert, behält möglicherweise Scheitelpunktdaten für den oberen und unteren Arm bei, die jeweils eine separate Welttransformationsmatrix aufweisen. Dies wird im folgenden Codebeispiel veranschaulicht.


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



Um den Arm zu rendern, werden zwei Renderingaufrufe durchgeführt, wie im folgenden Code gezeigt.


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



Die folgende Abbildung ist eine Banane, die für die Verwendung dieser Technik geändert wurde.

![Abbildung einer gemischten Banane ohne Geometrieblending](images/noblend.png)

Die Unterschiede zwischen der gemischten Geometrie und der Nichtblendgeometrie sind offensichtlich. Dieses Beispiel ist etwas extrem. In einer realen Anwendung sind die Fugen von segmentierten Modellen so konzipiert, dass Nahten nicht so offensichtlich sind. Allerdings sind Nahten manchmal sichtbar, was für Modelldesigner immer wieder herausforderungend ist.

Die Geometriemischung in Direct3D stellt eine Alternative zum klassischen Segmentmodellierungsszenario dar. Die verbesserte visuelle Qualität von segmentierten Objekten geht jedoch auf Kosten der Mischungsberechnungen während des Renderings. Um die Auswirkungen dieser zusätzlichen Vorgänge zu minimieren, ist die Direct3D-Geometriepipeline so optimiert, dass geometrie mit möglichst wenig Aufwand kombiniert wird. Anwendungen, die die von Direct3D angebotenen Geometriemischungsdienste intelligent verwenden, können die Realität ihrer Zeichen verbessern und gleichzeitig schwerwiegende Leistungssteigerungen vermeiden.

## <a name="blending-transform-and-render-states"></a>Überblenden von Transformations- und Renderzuständen

Die [**IDirect3DDevice9::SetTransform-Methode**](/windows/desktop/api) erkennt die [**D3DTS \_ WORLD-**](d3dts-world.md) und [**D3DTS \_ WORLDn-Makros,**](d3dts-worldn.md) die Werten entsprechen, die durch das [**D3DTS \_ WORLDMATRIX-Makro**](d3dts-worldmatrix.md) definiert werden können. Diese Makros werden verwendet, um die Matrizen zu identifizieren, zwischen denen die Geometrie gemischt wird.

Der [**D3DRENDERSTATETYPE-Enumerationstyp**](./d3drenderstatetype.md) enthält den D3DRS \_ VERTEXBLEND-Renderzustand zum Aktivieren und Steuern der Geometriemischung. Gültige Werte für diesen Renderzustand werden vom [**D3DVERTEXBLENDFLAGS-Enumerationstyp**](./d3dvertexblendflags.md) definiert. Wenn geometry blending aktiviert ist, muss das Scheitelpunktformat die entsprechende Anzahl von Mischungsgewichtungen enthalten.

## <a name="blending-weights"></a>Mischungsgewichtungen

Eine Mischungsgewichtung, manchmal als Betagewichtung bezeichnet, steuert das Ausmaß, in dem sich eine bestimmte Weltmatrix auf einen Scheitelpunkt auswirkt. Blendinggewichtungen sind Gleitkommawerte im Bereich von 0,0 bis 1,0, codiert im Scheitelpunktformat, wobei ein Wert von 0,0 bedeutet, dass der Scheitelpunkt nicht mit dieser Matrix kombiniert wird, und 1,0 bedeutet, dass der Scheitelpunkt vollständig von der Matrix betroffen ist.

Geometriemischungsgewichtungen werden im Scheitelpunktformat codiert und werden unmittelbar nach der Position für jeden Scheitelpunkt angezeigt, wie unter [FVF-Codes für feste Funktionen (Direct3D 9)](fixed-function-fvf-codes.md)beschrieben. Sie kommunizieren die Anzahl der Mischungsgewichtungen im Scheitelpunktformat, indem Sie eine der [FVF-Konstanten](d3dfvf.md) in die Vertexbeschreibung einschließen, die Sie den Renderingmethoden bereitstellen.

Das System führt eine lineare Mischung zwischen den gewichteten Ergebnissen der Mischungsmatrizen aus. Die folgende Gleichung ist die vollständige Mischungsformel.

![Gleichung der linearen Überblendung unter Verwendung von Welttransformationsmatrizen](images/vert-blend-formula.png)

In der obigen Gleichung ist vBlend der Ausgabevertex, die v-Elemente sind die Scheitelpunkte, die von der angewendeten Weltmatrix erzeugt werden ([**D3DTS \_ WORLDn**](d3dts-worldn.md)). Die W-Elemente sind die entsprechenden Gewichtungswerte innerhalb des Scheitelpunktformats. Ein Scheitelpunkt, der zwischen n Matrizen gemischt wird, kann einen Gewichtungswert für die Mischung aufweisen, einen für jede Mischungsmatrix, mit Ausnahme des letzten. Das System generiert automatisch die Gewichtung für die letzte Weltmatrix, sodass die Summe aller Gewichtungen 1,0 beträgt, die hier in Sigma-Notation ausgedrückt wird. Diese Formel kann für jeden der von Direct3D unterstützten Fälle vereinfacht werden. Dies ist in den folgenden Gleichungen dargestellt.

![Gleichungen der linearen Überblendung für drei Überblendungsfälle](images/vert-blend-formulas-simple.png)

Dies sind die vereinfachten Formen der vollständigen Mischungsformel für die beiden, drei und vier Blendmatrixfälle.

> [!Note]  
> Obwohl Direct3D FVF-Deskriptoren zum Definieren von Scheitelpunkten enthält, die bis zu fünf Mischungsgewichtungen enthalten, können in dieser DirectX-Version nur drei verwendet werden.

 

Weitere Informationen finden Sie in den folgenden Themen.

-   [Verwenden von Geometry Blending (Direct3D 9)](using-geometry-blending.md)
-   [Indexed Vertex Blending (Direct3D 9) (Indizierte Vertexmischung (Direct3D 9))](indexed-vertex-blending.md)
-   [Vertex-Tweening (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 
