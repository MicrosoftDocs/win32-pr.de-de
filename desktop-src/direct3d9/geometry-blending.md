---
description: Direct3D ermöglicht es einer Anwendung, die Umsetzung ihrer Szenen zu steigern, indem segmentierte polygonale Objekte gerendert werden, insbesondere Zeichen, die über reibungslos gemischte Gelenke verfügen.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Geometrie Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745384"
---
# <a name="geometry-blending-direct3d-9"></a>Geometrie Mischung (Direct3D 9)

Direct3D ermöglicht es einer Anwendung, die Umsetzung ihrer Szenen zu steigern, indem segmentierte polygonale Objekte gerendert werden, insbesondere Zeichen, die über reibungslos gemischte Gelenke verfügen. Diese Effekte werden häufig als "Skinning" bezeichnet. Das System erreicht diesen Effekt, indem er zusätzliche Transformations Matrizen für die Welt auf einen einzelnen Satz von Vertices anwendet, um mehrere Ergebnisse zu erstellen, und dann eine lineare Mischung zwischen den resultierenden Scheitel Punkten durchführen, um einen einzelnen Satz von Geometrie für das Rendering zu erstellen. Die folgende Abbildung einer Banane zeigt diesen Prozess.

![Abbildung des Prozesses zum Mischen von zwei Objekten mit der Bananen Textur](images/geometry-blend.png)

Die obige Abbildung zeigt, wie Sie sich den Geometry-Mischungs Prozess vorstellen können. Bei einem einzelnen Renderingbefehl übernimmt das System die Scheitel Punkte für die Banane, transformiert Sie zweimal, und zwar ohne Änderung und einmal mit einer einfachen Drehung, und kombiniert die Ergebnisse, um eine gekrümmten Banane zu erstellen. Das System mischt die Scheitelpunkt Position sowie den Scheitelpunkt normal, wenn Beleuchtung aktiviert ist. Anwendungen sind nicht auf zwei Mischungs Pfade beschränkt. Direct3D kann Geometrie zwischen bis zu vier Welt Matrizen, einschließlich der Standard-World Matrix, [**D3DTS \_ World**](d3dts-world.md), mischen.

> [!Note]
>
> Wenn Beleuchtung aktiviert ist, werden Vertex-Normale durch eine entsprechende inverse World-View-Matrix transformiert, die auf die gleiche Weise gewichtet wird wie die Berechnungen der Scheitelpunkt Position. Das System normalisiert den resultierenden normalen Vektor, wenn der D3DRS \_ normalizenormals-Rendering-Zustand auf **true** festgelegt ist.

 

Ohne Geometrie Mischung werden dynamische artikulierte Modelle häufig in Segmenten gerendert. Stellen Sie sich beispielsweise ein 3D-Modell der menschlichen Arm vor. In der einfachsten Ansicht besteht ein Arm aus zwei Teilen: dem oberen Arm, der mit dem Text verbunden ist, und dem unteren Arm, der eine Verbindung mit der Hand herstellt. Beide sind am-Bogen angeschlossen, und der untere Arm dreht sich an diesem Punkt. Eine Anwendung, die einen Arm rendert, behält möglicherweise Scheitelpunkt Daten für den oberen und unteren Arm bei, jeweils mit einer separaten Welt Transformationsmatrix. Dies wird im folgenden Codebeispiel veranschaulicht.


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



Um den Arm zu rendern, werden zwei renderingaufrufe durchgeführt, wie im folgenden Code dargestellt.


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



Die folgende Abbildung stellt eine Banane dar, die zur Verwendung dieser Technik geändert wird.

![Abbildung einer gemischten Banane ohne Geometrie Mischung](images/noblend.png)

Die Unterschiede zwischen der gemischten Geometrie und der nicht gemischten Geometrie sind offensichtlich. Dieses Beispiel ist ziemlich extrem. In einer realen Anwendung werden die Gelenke segmentierter Modelle so entworfen, dass die Nähte nicht so offensichtlich sind. Allerdings sind die Nähte manchmal sichtbar, was eine Konstante Herausforderung für Modell Designer darstellt.

Geometrie Mischung in Direct3D stellt eine Alternative zum klassischen segmentierten Modellierungs Szenario dar. Die verbesserte visuelle Qualität segmentierter Objekte ergibt sich jedoch aus den Kosten der Mischungs Berechnungen während des Renderings. Um die Auswirkungen dieser zusätzlichen Vorgänge zu minimieren, wird die Direct3D Geometry-Pipeline optimiert, um Geometrie mit dem geringstmöglichen Verwaltungsaufwand zu kombinieren. Anwendungen, die die von Direct3D angebotenen Geometrie-Mischungs Dienste Intelligent verwenden, können den Realismus ihrer Zeichen verbessern und gleichzeitig ernsthafte Auswirkungen auf die Leistung vermeiden.

## <a name="blending-transform-and-render-states"></a>Mischen von Transformations-und renderzuständen

Die [**IDirect3DDevice9:: setTransform**](/windows/desktop/api) -Methode erkennt die Makros [**D3DTS \_ World**](d3dts-world.md) und [**D3DTS \_ worldn**](d3dts-worldn.md) , die den Werten entsprechen, die vom [**D3DTS \_ worldmatrix**](d3dts-worldmatrix.md) -Makro definiert werden können. Diese Makros werden verwendet, um die Matrizen zu identifizieren, zwischen denen die Geometrie gemischt wird.

Der [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) -Enumerationstyp enthält den D3DRS \_ vertexblend-Rendering-Zustand zum Aktivieren und Steuern der Geometrie Mischung. Gültige Werte für diesen Rendering-Zustand werden durch den [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -enumerierten Typ definiert. Wenn Geometrie Mischung aktiviert ist, muss das Scheitelpunkt Format die entsprechende Anzahl von Mischungs Gewichtungen enthalten.

## <a name="blending-weights"></a>Mischen von Gewichtungen

Ein Mischungs Gewicht, manchmal auch als Beta-Gewichtung bezeichnet, steuert, in welchem Ausmaß eine bestimmte Weltmatrix auf einen Scheitelpunkt wirkt. Beim Mischen von Gewichtungen handelt es sich um Gleit Komma Werte zwischen 0,0 und 1,0, die im Vertex-Format codiert sind. der Wert 0,0 bedeutet, dass der Scheitelpunkt nicht mit dieser Matrix gemischt ist, und 1,0 bedeutet, dass der Scheitelpunkt vollständig von der Matrix betroffen ist.

Geometrie-Mischungs Gewichtungen werden im Vertex-Format codiert und unmittelbar nach der Position der einzelnen Scheitel Punkte angezeigt, wie in [Fixed Function f VF Codes (Direct3D 9)](fixed-function-fvf-codes.md)beschrieben. Sie geben die Anzahl der Mischungs Gewichtungen im Vertex-Format an, indem Sie eine der [FVF-Konstanten](d3dfvf.md) in die vertexbeschreibung einschließen, die Sie den Renderingmethoden bereitstellen.

Das System führt eine lineare Mischung zwischen den gewichteten Ergebnissen der Blend-Matrizen aus. Die folgende Gleichung ist die komplette Mischungs Formel.

![Gleichung linearer Mischungs-, using World Transformation Matrizen](images/vert-blend-formula.png)

In der vorangehenden Gleichung ist vblend der Ausgabe Scheitelpunkt. die v-Elemente sind die Scheitel Punkte, die von der angewendeten Weltmatrix ([**D3DTS \_ worldn**](d3dts-worldn.md)) erstellt werden. Die W-Elemente sind die entsprechenden Gewichtungswerte im Scheitelpunkt Format. Ein Scheitelpunkt zwischen n Matrizen kann-1 enthalten, der Gewichtungswerte für jede Mischungs Matrix (mit Ausnahme des letzten) kombiniert. Das System generiert automatisch die Gewichtung für die letzte Weltmatrix, sodass die Summe aller Gewichtungen 1,0 ist, ausgedrückt in Sigma-Notation. Diese Formel kann für jeden der von Direct3D unterstützten Fällen vereinfacht werden, was in den folgenden Gleichungen gezeigt wird.

![Gleichungen linearer Blending für drei Mischungs Fälle](images/vert-blend-formulas-simple.png)

Dies sind die vereinfachten Formen der kompletten Mischungs Formel für die zwei, drei und vier Blend Matrix Fälle.

> [!Note]  
> Obwohl Direct3D FVF-Deskriptoren enthält, um Vertices zu definieren, die bis zu fünf Mischungs Gewichtungen enthalten, können in dieser Version von DirectX nur drei verwendet werden.

 

Weitere Informationen finden Sie in den folgenden Themen.

-   [Verwenden von Geometrie Mischung (Direct3D 9)](using-geometry-blending.md)
-   [Indiziertes Vertex-Blending (Direct3D 9)](indexed-vertex-blending.md)
-   [Vertex-Tweening (Direct3D 9)](vertex-tweening.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Scheitelpunkt Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
