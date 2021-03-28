---
title: Einstieg in die Rasterizer-Phase
description: In diesem Abschnitt wird das Festlegen des Viewports, des Scheren Rechtecks, des Status des Rasterizers und der mehrfach Stichproben Erstellung beschrieben.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- Multisampling, Status des Rasterizers (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315213"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Einstieg in die Rasterizer-Phase

In diesem Abschnitt wird das Festlegen des Viewports, des Scheren Rechtecks, des Status des Rasterizers und der mehrfach Stichproben Erstellung beschrieben.

## <a name="set-the-viewport"></a>Festlegen des Viewports

Ein Viewport ordnet Scheitelpunkt Positionen (im Clip Bereich) den renderzielpositionen zu. In diesem Schritt werden die 3D-Positionen in 2D-Raum skaliert. Ein Renderziel ist mit den Y-Achsen ausgerichtet, die nach unten zeigen. Dies erfordert, dass die Y-Koordinaten während der viewportskala gekippt werden. Außerdem werden die x-und y-Blöcke (Bereich der x-und y-Werte) skaliert, sodass Sie der Viewportgröße entsprechend den folgenden Formeln entsprechen:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



In Tutorial 1 wird ein 640 × 480-Viewport mithilfe von [**D3D11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) und durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports)erstellt.


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



Die viewportbeschreibung gibt die Größe des Viewports, den Bereich, dem die Tiefe zugeordnet werden soll (mit *mintiefe* und *maxtiefe*) und die Platzierung der oberen linken Ecke des Viewports an. *Mintiefe* muss kleiner oder gleich *maxtiefe* sein. der Bereich für *mintiefe* und *maxtiefe* liegt zwischen 0,0 und 1,0 (einschließlich). Es ist üblich, dass der Viewport einem Renderziel zugeordnet wird, dies ist jedoch nicht erforderlich. Außerdem muss der Viewport nicht dieselbe Größe oder Position aufweisen wie das Renderziel.

Sie können ein Array von Viewports erstellen, aber nur eines kann auf eine primitive Ausgabe vom Geometry-Shader angewendet werden. Es kann jeweils nur ein Viewport aktiv festgelegt werden. Die Pipeline verwendet während der rasterisierung einen standardviewport (und das im nächsten Abschnitt erörterte Scheren-Rechteck). Der Standardwert ist immer das erste Viewport (oder Scheren Rechteck) im Array. Um eine einzelne Auswahl des Viewports im Geometry-Shader auszuführen, geben Sie die "viewportarrayindex"-Semantik in der entsprechenden GS-Ausgabe Komponente in der GS-Ausgabe Signatur Deklaration an.

Die maximale Anzahl von Viewports (und Scheren Rechtecke), die zu einem beliebigen Zeitpunkt an die Raster-Stufe gebunden werden können, ist 16 (angegeben durch **D3D11 \_ Viewport \_ und \_ scissorrect- \_ Objekt \_ Anzahl \_ pro \_ Pipeline**).

## <a name="set-the-scissor-rectangle"></a>Festlegen des Scheren Rechtecks

Mit einem Scheren Rechteck haben Sie weitere Möglichkeiten, die Anzahl der Pixel zu verringern, die an die Ausgabe Zusammenführungs Phase gesendet werden. Pixel außerhalb des Scheren Rechtecks werden verworfen. Die Größe des Scheren Rechtecks wird in ganzen Zahlen angegeben. Auf ein Dreieck kann während der rasterisierung nur ein Scheren-Rechteck (auf der Grundlage von *viewportarrayindex* in der [Semantik des System Werts](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) angewendet werden.

Um das Scheren-Rechteck zu aktivieren, verwenden Sie den *scissorenable* -Member (in [**D3D11 \_ Rasterizer \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)). Das standardmäßige Scheren-Rechteck ist ein leeres Rechteck. Das heißt, alle Rect-Werte sind 0 (null). Anders ausgedrückt: Wenn Sie das Scheren-Rechteck nicht einrichten und Scheren aktiviert ist, senden Sie keine Pixel an die Ausgabe-Fusion-Phase. Das gängigste Setup ist das Initialisieren des Scheren Rechtecks mit der Größe des Viewports.

Um ein Array von Scheren Rechtecke auf das Gerät festzulegen, müssen Sie [**Verknüpfung id3d11devicecontext aus:: rssetcissorrects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) mit [**D3D11 \_ Rect**](d3d11-rect.md)abrufen.


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Diese Methode nimmt zwei Parameter an: (1) die Anzahl der Rechtecke im Array und (2) ein Array von Rechtecke.

Die Pipeline verwendet einen standardmäßigen Scheren-Rechteck Index während der rasterisierung (der Standardwert ist ein Rechteck der Größe 0 (null), bei dem Clipping deaktiviert ist). Um dies zu überschreiben, geben \_ Sie die Semantik von SV viewportarrayindex zu einer GS-Ausgabe Komponente in der GS-Ausgabe Signatur Deklaration an. Dies bewirkt, dass die GS-Phase diese GS-Ausgabe Komponente als vom systemgenerierte Komponente mit dieser Semantik markiert. Diese Semantik wird von der Raster-Stufe erkannt, und der Parameter, an den Sie angefügt ist, wird als Scheren Rechtecks Index verwendet, um auf das Array von Scheren Rechtecke zuzugreifen. Vergessen Sie nicht, die Raster-Phase anzuweisen, das von Ihnen definierte Scheren-Rechteck zu verwenden, indem Sie den *scissorenable* -Wert in der Beschreibung des Rasterizers aktivieren, bevor Sie das Raster-Objekt erstellen.

## <a name="set-rasterizer-state"></a>Status des Rasterizers festlegen

Beginnend mit Direct3D 10 ist der Raster State in einem Raster State-Objekt gekapselt. Sie können bis zu 4096 Raster State-Objekte erstellen, die dann auf das Gerät festgelegt werden können, indem Sie ein Handle an das State-Objekt übergeben.

Verwenden Sie [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) , um ein Raster State-Objekt aus einer Beschreibung des Rasterizers zu erstellen (siehe [**D3D11 \_ Raster \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



Dieser Beispielsatz von Zuständen ist möglicherweise die einfachste Einrichtung des Rasterizers:

-   Vollfüll Modus
-   Entfernen oder Entfernen von Hinterflächen gegen den Uhrzeigersinn ausgewickelte Reihenfolge für primitive annehmen
-   Deaktivieren der tiefen Verschiebung, Aktivieren der tiefen Pufferung und Aktivieren des Scheren Rechtecks
-   Deaktivieren von multisamplinggrad und Zeilen-Antialiasing

Außerdem enthalten die grundlegenden Raster-Vorgänge immer Folgendes: Clipping (in der Ansicht "Frustum"), Perspektiven Teilung und viewportskala. Nachdem das Raster State-Objekt erfolgreich erstellt wurde, legen Sie es wie folgt auf das Gerät fest:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Multisampling

Bei der Multisampling-Funktion werden einige oder alle Komponenten eines Bilds mit einer höheren Auflösung (gefolgt von einer Herabstufung der ursprünglichen Auflösung) als Stichprobe angezeigt, um die am häufigsten sichtbare Form von Aliasing durch das Zeichnen von Polygon Kanten zu verringern. Obwohl multisamplinggrad subpixelbeispiele erfordert, implementieren moderne GPU multisamplinggrad, sodass ein Pixelshader einmal pro Pixel ausgeführt wird. Dies bietet einen akzeptablen Kompromiss zwischen Leistung (insbesondere in einer GPU-gebundenen Anwendung) und Antialiasing des endgültigen Bilds.

Wenn Sie Multisampling verwenden möchten, legen Sie das Feld aktivieren in der [**Beschreibung der rasterisierung**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)fest, erstellen Sie ein Multisampling-Renderziel, und lesen Sie entweder das Renderziel mit einem Shader, um die Beispiele in eine einzelne Pixelfarbe aufzulösen oder [**Verknüpfung id3d11devicecontext aus:: resolvesbresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) aufzurufen, um die Beispiele mithilfe der Grafikkarte aufzulösen. Das häufigste Szenario ist das Zeichnen eines oder mehrerer Multisampling-Renderziele.

Multisampling ist unabhängig davon, ob eine Beispiel Maske verwendet wird, ob [die Alpha-zu-Abdeckung-](d3d10-graphics-programming-guide-blend-state.md) Funktion aktiviert ist, oder ob es sich um Schablonen Vorgänge handelt (die immer pro Stichprobe ausgeführt werden).

Die tiefen Tests sind von Multisampling betroffen:

-   Wenn multisamplinggrad aktiviert ist, wird die Tiefe pro Stichprobe interpoliert, und der tiefen-/Schablone-Test erfolgt pro Beispiel. die Pixel-Shader-Ausgabe Farbe wird für alle bestandenen Beispiele dupliziert. Wenn der Pixelshader eine Tiefe ausgibt, wird der tiefen Wert für alle Stichproben dupliziert (obwohl dieses Szenario den Vorteil von Multisampling verliert).
-   Wenn die multisamplinggrad-Funktion deaktiviert ist, werden tiefen/Schablone-Tests immer noch pro Stichprobe ausgeführt, aber die Tiefe wird nicht pro Stichprobe interpoliert.

Es gibt keine Einschränkungen für das Mischen von Multisampling-und nicht-Multisampling-Rendering innerhalb eines einzelnen Renderziels. Wenn Sie multisamplinggrad aktivieren und zu einem Renderziel ohne multisamplinggrad ziehen, führen Sie das gleiche Ergebnis wie bei aktivierter multisamplinggrad-Funktion aus. die Stichprobenentnahme erfolgt mit einem einzelnen Beispiel pro Pixel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stufe des Rasterizers](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 