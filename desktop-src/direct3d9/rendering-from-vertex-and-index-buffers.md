---
description: Sowohl indizierte als auch nicht indizierte Zeichnungsmethoden werden von Direct3D unterstützt.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendern von Scheitelpunkt- und Indexpuffern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4290dc2ff40e1ec0448e3948342aa3b02ac62bf9866a44958ea53bee9658d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092629"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Rendern von Scheitelpunkt- und Indexpuffern (Direct3D 9)

Sowohl indizierte als auch nicht indizierte Zeichnungsmethoden werden von Direct3D unterstützt. Die indizierten Methoden verwenden einen einzelnen Satz von Indizes für alle Scheitelpunktkomponenten. Scheitelpunktdaten werden in Scheitelpunktpuffern und Indexdaten in Indexpuffern gespeichert. Unten sind einige häufige Szenarien für das Zeichnen von Primitiven mithilfe von Scheitelpunkt- und Indexpuffern aufgeführt.

In diesen Beispielen wird die Verwendung von [**IDirect3DDevice9::D rawPrimitive**](/windows/desktop/api) und [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) verglichen.

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Szenario 1: Zeichnen von zwei Dreiecken ohne Indizierung

Angenommen, Sie möchten das Quad zeichnen, das in der folgenden Abbildung dargestellt ist.

![Abbildung eines Quadrats, das aus zwei Dreiecken besteht](images/dip-fig1.png)

Wenn Sie den primitiven Typ Dreiecksliste verwenden, um die beiden Dreiecke zu rendern, wird jedes Dreieck als drei einzelne Scheitelpunkte gespeichert, was zu einem ähnlichen Scheitelpunktpuffer wie in der folgenden Abbildung führt.

![Diagramm eines Scheitelpunktpuffers, der drei Scheitelpunkte für zwei Dreiecke definiert](images/dip-fig2.png)

Der Zeichnungsaufruf ist sehr einfach. Zeichnen Sie ab Position 0 innerhalb des Scheitelpunktpuffers zwei Dreiecke. Wenn Culling aktiviert ist, ist die Reihenfolge der Scheitelungen wichtig. In diesem Beispiel wird der standardmäßige Cullingzustand gegen den Uhrzeigersinn angenommen, sodass sichtbare Dreiecke in der Reihenfolge im Uhrzeigersinn gezeichnet werden müssen. Der primitive Typ Dreiecksliste liest einfach drei Scheitelungen in linearer Reihenfolge aus dem Puffer für jedes Dreieck, sodass dieser Aufruf Dreiecke (0, 1, 2) und (3, 4, 5) zeichnen wird:


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Szenario 2: Zeichnen von zwei Dreiecken mit Indizierung

Wie Sie feststellen werden, enthält der Scheitelpunktpuffer doppelte Daten an den Speicherorten 0 und 4, 2 und 5. Dies ist sinnvoll, da die beiden Dreiecke zwei gemeinsame Scheitelungen haben. Diese doppelten Daten sind verschwendet, und der Scheitelpunktpuffer kann mithilfe eines Indexpuffers komprimiert werden. Ein kleinerer Scheitelpunktpuffer reduziert die Menge der Scheitelpunktdaten, die an die Grafikkarte gesendet werden müssen. Noch wichtiger ist, dass der Adapter mithilfe eines Indexpuffers Scheitelpunkte in einem Scheitelpunktcache speichern kann. Wenn der zu zeichnete Primitive einen zuletzt verwendeten Scheitelpunkt enthält, kann dieser Scheitelpunkt aus dem Cache abgerufen werden, anstatt ihn aus dem Scheitelpunktpuffer zu lesen, was zu einer großen Leistungssteigerung führt.

Ein Indexpuffer 'indiziert' in den Scheitelpunktpuffer, sodass jeder eindeutige Scheitelpunkt nur einmal im Scheitelpunktpuffer gespeichert werden muss. Das folgende Diagramm zeigt einen indizierten Ansatz für das frühere Zeichnungsszenario.

![Diagramm eines Indexpuffers für den früheren Scheitelpunktpuffer](images/dip-fig3.png)

Der Indexpuffer speichert VB Indexwerte, die auf einen bestimmten Scheitelpunkt innerhalb des Scheitelpunktpuffers verweisen. Ein Scheitelpunktpuffer kann als Array von Scheitelpunkten bezeichnet werden, sodass der VB Index einfach der Index im Scheitelpunktpuffer für den Zielvertex ist. Ebenso ist ein IB-Index ein Index im Indexpuffer. Dies kann sehr schnell verwirrend werden, wenn Sie nicht vorsichtig sind. Stellen Sie daher sicher, dass Sie das verwendete Vokabular klar finden: VB Indexwerte werden in den Scheitelpunktpuffer indiziert, IB-Indexwerte werden in den Indexpuffer indiziert, und der Indexpuffer selbst speichert VB Indexwerte.

Der Zeichnungsaufruf ist unten dargestellt. Die Bedeutungen aller Argumente werden für das nächste Zeichnungsszenario ausführlich erläutert. Beachten Sie zunächst, dass dieser Aufruf Direct3D erneut anweisen soll, eine Dreiecksliste mit zwei Dreiecken zu rendern, beginnend bei Position 0 innerhalb des Indexpuffers. Dieser Aufruf zeichnen die gleichen zwei Dreiecke in der gleichen Reihenfolge wie zuvor, um eine ordnungsgemäße Ausrichtung im Uhrzeigersinn sicherzustellen:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Szenario 3: Zeichnen eines Dreiecks mit Indizierung

Nun möchten Sie nur das zweite Dreieck zeichnen, aber sie möchten denselben Scheitelpunktpuffer und Indexpuffer verwenden, der beim Zeichnen des gesamten Quads verwendet wird, wie im folgenden Diagramm dargestellt.

![Diagramm des Indexpuffers und des Scheitelpunktpuffers für das zweite Dreieck](images/dip-fig4.png)

Für diesen Zeichnungsaufruf wird der erste IB-Index 3 verwendet. dieser Wert wird als StartIndex bezeichnet. Der niedrigste verwendete VB Index ist 0. dieser Wert wird als MinIndex bezeichnet. Obwohl zum Zeichnen des Dreiecks nur drei Scheitelpunkte erforderlich sind, sind diese drei Scheitelpunkte auf vier angrenzende Positionen im Scheitelpunktpuffer verteilt. Die Anzahl der Positionen innerhalb des zusammenhängenden Blocks des Scheitelpunktpufferspeichers, die für den Zeichnungsaufruf erforderlich sind, wird als NumVertices bezeichnet und in diesem Aufruf auf 4 festgelegt. Die Werte MinIndex und NumVertices sind eigentlich nur Hinweise, die Direct3D bei der Optimierung des Arbeitsspeicherzugriffs während der Softwarevertexverarbeitung unterstützen. Sie können einfach so festgelegt werden, dass sie den gesamten Scheitelpunktpuffer zum Preis der Leistung enthalten.

Hier sehen Sie den Zeichnungsaufruf für den Fall eines einzelnen Dreiecks: Die Bedeutung des BaseVertexIndex-Arguments wird als Nächstes erläutert:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Szenario 4: Zeichnen eines Dreiecks mit Offsetindizierung

BaseVertexIndex ist ein Wert, der effektiv jedem im Indexpuffer gespeicherten VB Index hinzugefügt wird. Wenn wir beispielsweise während des vorherigen Aufrufs den Wert 50 für BaseVertexIndex übergeben hätten, wäre dies funktionell identisch mit der Verwendung des Indexpuffers im folgenden Diagramm für die Dauer des DrawIndexedPrimitive-Aufrufs:

![Diagramm eines Indexpuffers mit einem Wert von 50 für basevertexindex](images/dip-fig5.png)

Dieser Wert wird selten auf einen anderen Wert als 0 festgelegt, kann aber nützlich sein, wenn Sie den Indexpuffer vom Scheitelpunktpuffer entkoppeln möchten: Wenn sie den Indexpuffer für ein bestimmtes Gitternetz ausfüllen, ist die Position des Gitters im Scheitelpunktpuffer noch nicht bekannt, können Sie einfach vorgeben, dass sich die Gitternetzvertices am Anfang des Scheitelpunktpuffers befinden. Wenn es an der Zeit ist, den Zeichnen-Aufruf zu erstellen, übergeben Sie einfach die tatsächliche Startposition als BaseVertexIndex.

Diese Technik kann auch verwendet werden, wenn mehrere Instanzen eines Gitters mit einem einzelnen Indexpuffer gezeichnungt werden. Wenn der Scheitelpunktpuffer z. B. zwei Gitternetze mit identischer Zeichnen-Reihenfolge, aber leicht unterschiedlichen Scheitelpunkte (möglicherweise unterschiedliche diffuse Farben oder Texturkoordinaten) enthält, können beide Gitternetze mit unterschiedlichen Werten für BaseVertexIndex gezeichnet werden. Wenn Sie dieses Konzept noch einen Schritt weiter gehen, können Sie einen Indexpuffer verwenden, um mehrere Instanzen eines Gitters zu zeichnen, die jeweils in einem anderen Scheitelpunktpuffer enthalten sind, indem Sie einfach den scheitelpunktpuffer reaktivieren und den BaseVertexIndex nach Bedarf anpassen. Beachten Sie, dass der BaseVertexIndex-Wert auch automatisch dem MinIndex-Argument hinzugefügt wird, was sinnvoll ist, wenn Sie sehen, wie er verwendet wird:

Nun soll wieder nur das zweite Dreieck des Quad-Quadrats mit dem gleichen Indexpuffer wie zuvor ge zeichnen werden. Es wird jedoch ein anderer Scheitelpunktpuffer verwendet, in dem sich das Quad-VB Index 50 befindet. Die relative Reihenfolge der quadrischen Scheitelpunkte bleibt unverändert, nur die Anfangsposition innerhalb des Scheitelpunktpuffers ist unterschiedlich. Der Indexpuffer und der Scheitelpunktpuffer würden wie im folgenden Diagramm aussehen.

![Diagramm des Indexpuffers und des Scheitelpunktpuffers mit einem VB-Index von 50](images/dip-fig6.png)

Hier ist der entsprechende Zeichnen-Aufruf. Beachten Sie, dass BaseVertexIndex der einzige Wert ist, der sich im vorherigen Szenario geändert hat:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern von Primitiven](rendering-primitives.md)
</dt> </dl>

 

 
