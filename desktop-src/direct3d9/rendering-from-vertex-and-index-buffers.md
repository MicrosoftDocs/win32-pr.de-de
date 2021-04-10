---
description: Indizierte und nicht indizierte Zeichnungs Methoden werden von Direct3D unterstützt.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860088"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Rendering aus Scheitelpunkt-und Index Puffer (Direct3D 9)

Indizierte und nicht indizierte Zeichnungs Methoden werden von Direct3D unterstützt. Die indizierten Methoden verwenden einen einzelnen Satz von Indizes für alle Scheitelpunkt Komponenten. Vertex-Daten werden in Scheitelpunkt Puffern gespeichert, und Indexdaten werden in Index Puffern gespeichert. Nachstehend sind einige gängige Szenarien für das Zeichnen von primitiven mithilfe von Scheitel Punkten und Index Puffern aufgeführt.

Diese Beispiele vergleichen die Verwendung von [**IDirect3DDevice9::D rawprimitiv**](/windows/desktop/api) und [**IDirect3DDevice9::D rawindexedprimitiv**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Szenario 1: Zeichnen von zwei Dreiecken ohne Indizierung

Nehmen wir an, Sie möchten das Vierfache zeichnen, das in der folgenden Abbildung gezeigt wird.

![Abbildung eines Quadrats, das aus zwei Dreiecken besteht](images/dip-fig1.png)

Wenn Sie den primitiven Objekttyp für die Dreiecks Liste zum Rendern der beiden Dreiecke verwenden, wird jedes Dreieck als 3 einzelne Scheitel Punkte gespeichert, was in der folgenden Abbildung zu einem ähnlichen Scheitelpunkt Puffer führt.

![Diagramm eines Scheitelpunkt Puffers, der drei Vertices für zwei Dreiecke definiert](images/dip-fig2.png)

Der Zeichnungs Befehl ist sehr unkompliziert. Zeichnen Sie an Position 0 innerhalb des Vertex-Puffers zwei Dreiecke. Wenn das cullingfunktionsgruppe aktiviert ist, ist die Reihenfolge der Scheitel Punkte wichtig. In diesem Beispiel wird angenommen, dass der Standardzustand gegen den Uhrzeigersinn besteht, sodass sichtbare Dreiecke im Uhrzeigersinn gezeichnet werden müssen. Der primitive Typ der Dreiecks Liste liest einfach drei Scheitel Punkte in linearer Reihenfolge aus dem Puffer für jedes Dreieck. daher zeichnet dieser Befehl Dreiecke (0, 1, 2) und (3, 4, 5):


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Szenario 2: Zeichnen von zwei Dreiecken mit Indizierung

Wie Sie bemerken werden, enthält der Vertex-Puffer doppelte Daten an den Standorten 0 und 4, 2 und 5. Das ist sinnvoll, da die beiden Dreiecke zwei gängige Scheitel Punkte gemeinsam nutzen. Diese doppelten Daten sind verschwenderisch, und der Vertex-Puffer kann mithilfe eines Index Puffers komprimiert werden. Ein kleinerer Scheitelpunkt Puffer reduziert die Menge der Vertex-Daten, die an den Grafikadapter gesendet werden müssen. Noch wichtiger ist, dass durch die Verwendung eines Index Puffers Scheitel Punkte in einem Scheitelpunkt Cache gespeichert werden können. Wenn das primitive, das gezeichnet wird, einen zuletzt verwendeten Scheitelpunkt enthält, kann dieser Scheitelpunkt aus dem Cache abgerufen werden, anstatt ihn aus dem Scheitelpunkt Puffer zu lesen. Dies führt zu einer großen Leistungssteigerung.

Ein Index Puffer ' Indexes ' in den Scheitelpunkt Puffer, sodass jeder eindeutige Scheitelpunkt nur einmal im Vertexpuffer gespeichert werden muss. Das folgende Diagramm zeigt einen indizierten Ansatz für das frühere Zeichnungs Szenario.

![Diagramm eines Index Puffers für den früheren Vertex-Puffer](images/dip-fig3.png)

Der Index Puffer speichert VB-Indexwerte, die auf einen bestimmten Scheitelpunkt innerhalb des Scheitelpunkt Puffers verweisen. Ein Scheitelpunkt Puffer kann als ein Array von Scheitel Punkten betrachtet werden, sodass der VB-Index einfach der Index in den Scheitelpunkt Puffer für den Ziel Scheitelpunkt ist. Ebenso ist ein IB-Index ein Index im Index Puffer. Dies kann sehr schnell sehr verwirrend sein, wenn Sie nicht vorsichtig sind. Stellen Sie also sicher, dass Sie das verwendete Vokabular nicht kennen: VB Index Values Index in den Vertex-Puffer, Indexwerte Index von IB in den Index Puffer, und der Index Puffer selbst speichert VB-Indexwerte.

Der Zeichnungs Befehl wird unten dargestellt. Die Bedeutungen aller Argumente werden für das nächste Zeichnungs Szenario in der Länge erörtert. Beachten Sie vorerst, dass dieser-Befehl Direct3D erneut anweist, eine Dreiecks Liste mit zwei Dreiecken zu rendernden, beginnend an Position 0 innerhalb des Index Puffers. Dieser Befehl zeichnet dieselben zwei Dreiecke in genau derselben Reihenfolge wie zuvor, um eine angemessene Ausrichtung im Uhrzeigersinn sicherzustellen:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Szenario 3: Zeichnen eines Dreiecks mit Indizierung

Legen Sie jetzt fest, dass Sie nur das zweite Dreieck zeichnen möchten, aber Sie möchten denselben Vertex-Puffer und Index Puffer verwenden, die beim Zeichnen des gesamten Quad verwendet werden, wie in der folgenden Abbildung dargestellt.

![Diagramm des Index Puffers und des Scheitelpunkt Puffers für das zweite Dreieck](images/dip-fig4.png)

Für diesen Zeichnungs Befehl ist der erste verwendete IB-Index 3. Dieser Wert wird als startIndex bezeichnet. Der niedrigste verwendete VB-Index ist 0 (null). Dieser Wert wird als minindex bezeichnet. Obwohl nur drei Scheitel Punkte zum Zeichnen des Dreiecks erforderlich sind, werden diese drei Scheitel Punkte über vier angrenzende Positionen im Vertexpuffer verteilt. die Anzahl der Speicherorte innerhalb des zusammenhängenden Blocks des Vertex-Pufferspeichers, der für den Zeichnungs Aufruf benötigt wird, wird als numvertices bezeichnet und in diesem Aufruf auf 4 festgelegt. Die Werte "minindex" und "numvertices" sind wirklich lediglich Hinweise, um den Speicherzugriff während der Verarbeitung von Software Scheitel Punkten zu vereinfachen Direct3D und könnten einfach so festgelegt werden, dass Sie den gesamten Vertex-Puffer zum Preis der Leistung einschließen.

Dies ist der Zeichnungs Befehl für den Fall eines einzelnen Dreiecks. die Bedeutung des basevertexindex-Arguments wird im folgenden erläutert:


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Szenario 4: Zeichnen eines Dreiecks mit Offset Indizierung

Basevertexindex ist ein Wert, der jedem VB-Index, der im Index Puffer gespeichert ist, tatsächlich hinzugefügt wird. Wenn z. b. während des vorherigen Aufrufes den Wert 50 für basevertexindex angenommen hätte, wäre dies funktionell identisch mit der Verwendung des Index Puffers im folgenden Diagramm für die Dauer des DrawIndexedPrimitive-Aufrufes:

![Diagramm eines Index Puffers mit dem Wert 50 für basevertexindex](images/dip-fig5.png)

Dieser Wert wird nur selten auf einen anderen Wert als 0 festgelegt, kann jedoch nützlich sein, wenn Sie den Index Puffer vom Vertex-Puffer entkoppeln möchten: Wenn Sie den Index Puffer für ein bestimmtes Mesh ausfüllen, ist die Position des Netzes im Vertex-Puffer noch nicht bekannt, Sie können einfach festlegen, dass sich die Gitter Scheitel Punkte am Anfang des Vertexpuffers befinden. Wenn es an der Zeit ist, den zeichnen-Befehl zu erstellen, übergeben Sie einfach den eigentlichen Start Speicherort als basevertexindex.

Diese Technik kann auch verwendet werden, wenn mehrere Instanzen eines Mesh mithilfe eines einzelnen Index Puffers gezeichnet werden. Wenn der Scheitelpunkt Puffer z. b. zwei Netzen mit identischer Zeichnungsreihenfolge, aber leicht unterschiedlichen Vertices (z. b. unterschiedliche diffuse Farben oder Texturkoordinaten) enthielt, können beide Netzen mithilfe verschiedener Werte für basevertexindex gezeichnet werden. Wenn Sie dieses Konzept noch einen Schritt weiter gehen, können Sie einen Index Puffer verwenden, um mehrere Instanzen eines Mesh zu zeichnen, die jeweils in einem anderen Scheitelpunkt Puffer enthalten sind, indem Sie einfach einen Drilldown durchführen und den basevertexindex nach Bedarf anpassen. Beachten Sie, dass der Wert basevertexindex auch automatisch dem minindex-Argument hinzugefügt wird, was sinnvoll ist, wenn Sie sehen, wie es verwendet wird:

Stellen Sie jetzt fest, dass wir wieder nur das zweite Dreieck des Quad mit dem gleichen Index Puffer wie zuvor zeichnen möchten. Es wird jedoch ein anderer Scheitelpunkt Puffer verwendet, in dem sich das Vierfache im VB-Index 50 befindet. Die relative Reihenfolge der vier Scheitel Punkte bleibt unverändert, nur die Anfangsposition im Scheitelpunkt Puffer unterscheidet sich. Der Index Puffer und der Vertex-Puffer würden wie im folgenden Diagramm aussehen.

![Diagramm des Index Puffers und des Scheitelpunkt Puffers mit einem VB-Index von 50](images/dip-fig6.png)

Hier ist der geeignete Draw-Befehl. Beachten Sie, dass "basevertexindex" der einzige Wert ist, der sich seit dem vorherigen Szenario geändert hat:


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

[Rendern von primitiven](rendering-primitives.md)
</dt> </dl>

 

 
