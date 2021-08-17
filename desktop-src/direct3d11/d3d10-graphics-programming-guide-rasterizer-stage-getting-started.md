---
title: Erste Schritte mit der Rasterizer-Phase
description: In diesem Abschnitt werden das Festlegen des Viewports, des Scissors-Rechtecks, des Rasterizerzustands und der Mehrfachstichprobe beschrieben.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- Multisampling, Rasterizerzustand (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e819dd92dd9c07a71f3830d3b67e371bc3d0e0c98f62fa36fdcf8ee3550ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914001"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Erste Schritte mit der Rasterizer-Phase

In diesem Abschnitt werden das Festlegen des Viewports, des Scissors-Rechtecks, des Rasterizerzustands und der Mehrfachstichprobe beschrieben.

## <a name="set-the-viewport"></a>Festlegen des Viewports

Ein Viewport ordnet Scheitelpunktpositionen (im Clipbereich) renderzielpositionen zu. In diesem Schritt werden die 3D-Positionen in den 2D-Raum skaliert. Ein Renderziel wird mit den nach unten zeigenden Y-Achsen ausgerichtet. dies erfordert, dass die Y-Koordinaten während der Viewportskala gekippt werden. Darüber hinaus werden die x- und y-Werte (Bereich der x- und y-Werte) entsprechend den folgenden Formeln skaliert, um die Viewportgröße zu passen:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



Tutorial 1 erstellt einen 640 × 480-Viewport [**mithilfe von D3D11 \_ VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) und durch Aufrufen von [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


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



Die Viewportbeschreibung gibt die Größe des Viewports, den Bereich für die Zuordnung der Tiefe (mit *MinDepth* und *MaxDepth)* und die Platzierung links oben im Viewport an. *MinDepth* muss kleiner oder gleich *MaxDepth sein.* Der Bereich für *MinDepth* und *MaxDepth* liegt zwischen 0,0 und 1,0 (einschließlich). Es ist üblich, dass der Viewport einem Renderziel zuordnen kann, dies ist jedoch nicht erforderlich. darüber hinaus muss der Viewport nicht die gleiche Größe oder Position wie das Renderziel haben.

Sie können ein Array von Viewports erstellen, aber nur einer kann auf eine primitive Ausgabe des Geometrie-Shaders angewendet werden. Es kann immer nur ein Viewport aktiv festgelegt werden. Die Pipeline verwendet während der Rasterung einen Standard-Viewport (und ein Scissor-Rechteck, die im nächsten Abschnitt erläutert werden). Der Standardwert ist immer der erste Viewport (oder Scissor-Rechteck) im Array. Um eine primitive Auswahl des Viewports im Geometrie-Shader durchzuführen, geben Sie die ViewportArrayIndex-Semantik für die entsprechende GS-Ausgabekomponente in der GS-Ausgabesignaturdeklaration an.

Die maximale Anzahl von Viewports (und Scissor-Rechtecke), die gleichzeitig an die Rasterizerphase gebunden werden können, beträgt 16 (angegeben durch **D3D11 \_ VIEWPORT \_ UND \_ SCISSORRECT \_ OBJECT COUNT PER \_ \_ \_ PIPELINE**).

## <a name="set-the-scissor-rectangle"></a>Festlegen des Scissor-Rechtecks

Ein Scissor-Rechteck bietet Ihnen eine weitere Möglichkeit, die Anzahl der Pixel zu reduzieren, die an die Ausgabe-Mergerphase gesendet werden. Pixel außerhalb des Scissor-Rechtecks werden verworfen. Die Größe des Scissor-Rechtecks wird in ganzen Zahlen angegeben. Während der Rasterung kann nur ein Scissor-Rechteck (basierend auf *ViewportArrayIndex* [in](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)der Systemwertsemantik) auf ein Dreieck angewendet werden.

Um das Scissor-Rechteck zu aktivieren, verwenden Sie den *ScissorEnable-Member* (in [**D3D11 \_ RASTERIZER \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)). Das Standardmäßige Scissor-Rechteck ist ein leeres Rechteck. Das bedeutet, dass alle Rect-Werte 0 sind. Anders ausgedrückt: Wenn Sie das Scissor-Rechteck nicht einrichten und die Scissor-Funktion aktiviert ist, senden Sie keine Pixel an die Ausgabe-Merger-Phase. Am häufigsten wird das Scissor-Rechteck auf die Größe des Viewports initialisiert.

Um ein Array von Scissor-Rechtecke auf das Gerät zu setzen, rufen Sie [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) [**mit D3D11 \_ RECT auf.**](d3d11-rect.md)


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Diese Methode verwendet zwei Parameter: (1) die Anzahl der Rechtecke im Array und (2) ein Array von Rechtecke.

Die Pipeline verwendet während der Rasterung einen standardmäßigen Scissor-Rechteckindex (der Standardwert ist ein Rechteck der Größe 0 mit deaktivierter Beschneidung). Um dies zu überschreiben, geben Sie die SV ViewportArrayIndex-Semantik für eine \_ GS-Ausgabekomponente in der GS-Ausgabesignaturdeklaration an. Dadurch wird die GS-Phase diese GS-Ausgabekomponente als vom System generierte Komponente mit dieser Semantik markieren. Die Rasterizer-Stufe erkennt diese Semantik und verwendet den Parameter, an den sie angefügt ist, als Scissor-Rechteckindex für den Zugriff auf das Array von Scissor-Rechtecke. Vergessen Sie nicht, die Rasterizerphase an die Verwendung des von Ihnen definierten Scissor-Rechtecks zu informieren, indem Sie den *ScissorEnable-Wert* in der Beschreibung des Rasterizers aktivieren, bevor Sie das Rasterizerobjekt erstellen.

## <a name="set-rasterizer-state"></a>Festlegen des Rasterizerzustands

Ab Direct3D 10 wird der Rasterizerzustand in einem Rasterizer-Zustandsobjekt gekapselt. Sie können bis zu 4096 Rasterizer-Zustandsobjekte erstellen, die dann auf das Gerät festgelegt werden können, indem Sie ein Handle an das Zustandsobjekt übergeben.

Verwenden [**Sie ID3D11Device1::CreateRasterizerState1,**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) um ein Rasterizer-Zustandsobjekt aus einer Rasterizerbeschreibung zu erstellen (siehe [**D3D11 \_ RASTERIZER \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


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



Dieser Beispielzustandssatz erreicht möglicherweise die grundlegendste Einrichtung des Rasterizers:

-   Vollformatfüllmodus
-   Cull out or remove back faces( Zurückgesichter entfernen; Annahme einer gegen den Uhrzeigersinn windenden Reihenfolge für Primitive
-   Tiefenvoreingenommenheit deaktivieren, aber Tiefenpufferung aktivieren und das Scissor-Rechteck aktivieren
-   Deaktivieren von Multisampling und Zeilen-Antialiasing

Darüber hinaus umfassen grundlegende Rasterizervorgänge immer Folgendes: Clipping (zum Frustum der Ansicht), Perspektiventeilung und Viewportskala. Nachdem Sie das Rasterizer-Zustandsobjekt erfolgreich erstellt haben, legen Sie es wie hier dargestellt auf das Gerät fest:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Multisampling

Multisamplingbeispiele für einige oder alle Komponenten eines Bilds mit einer höheren Auflösung (gefolgt von einem Downsampling auf die ursprüngliche Auflösung), um die sichtbarste Form von Aliasing zu reduzieren, die durch das Zeichnen von Polygonrändern verursacht wird. Obwohl multisampling Unterpixelbeispiele erfordert, implementieren moderne GPU-Funktionen Multisampling, sodass ein Pixel-Shader einmal pro Pixel ausgeführt wird. Dies bietet einen akzeptablen Kompromiss zwischen der Leistung (insbesondere in einer GPU-gebundenen Anwendung) und dem Antialiasing des endgültigen Images.

Um Multisampling zu verwenden, legen Sie das Feld aktivieren in der Rasterungsbeschreibung [**fest,**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)erstellen Ein Multisampling-Renderziel, und lesen Sie entweder das Renderziel mit einem Shader, um die Beispiele in eine einzelne Pixelfarbe aufzulösen, oder rufen Sie [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) auf, um die Beispiele mithilfe der Grafikkarte aufzulösen. Das häufigste Szenario ist das Zeichnen auf ein oder mehrere Renderziele mit mehrerenAmpeln.

Multisampling ist unabhängig davon, ob eine Beispielmaske verwendet wird, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) aktiviert ist oder ob Schablonenvorgänge (die immer pro Stichprobe ausgeführt werden).

Tiefentests werden durch Multisampling beeinflusst:

-   Wenn Multisampling aktiviert ist, wird die Tiefe pro Stichprobe interpoliert, und der Tiefen-/Schablonentest erfolgt pro Stichprobe. Die Pixel-Shader-Ausgabefarbe wird für alle übergebenen Stichproben dupliziert. Wenn der Pixel-Shader die Tiefe ausausgabet, wird der Tiefenwert für alle Stichproben dupliziert (obwohl in diesem Szenario der Vorteil von Multisampling verloren geht).
-   Wenn Multisampling deaktiviert ist, werden tiefen-/schablonenbasierte Tests weiterhin pro Stichprobe durchgeführt, aber die Tiefe wird nicht pro Stichprobe interpoliert.

Es gibt keine Einschränkungen für das Mischen von Multisampled- und Nicht-Multisampled-Rendering innerhalb eines einzelnen Renderziels. Wenn Sie Multisampling aktivieren und auf ein Nicht-Multisampling-Renderziel zeichnen, erzeugen Sie das gleiche Ergebnis, als ob multisampling nicht aktiviert wäre. Die Stichprobenentnahme erfolgt mit einer einzelnen Stichprobe pro Pixel.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stufe des Rasterizers](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 