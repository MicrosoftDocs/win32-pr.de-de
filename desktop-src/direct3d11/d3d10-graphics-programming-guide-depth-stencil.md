---
title: Konfigurieren Depth-Stencil Funktionalität
description: In diesem Abschnitt werden die Schritte zum Einrichten des Tiefenschablonenpuffers und des Tiefenschablonenzustands für die Ausgabezusammenführungsphase beschrieben.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e994c5a11215d245d8101edff410a91ffb788583b07f651fdfbd1f2771d7deab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990190"
---
# <a name="configuring-depth-stencil-functionality"></a>Konfigurieren Depth-Stencil Funktionalität

In diesem Abschnitt werden die Schritte zum Einrichten des Tiefenschablonenpuffers und des Tiefenschablonenzustands für die Ausgabezusammenführungsphase beschrieben.

-   [Erstellen einer Depth-Stencil-Ressource](#create-a-depth-stencil-resource)
-   [Erstellen Depth-Stencil Zustands](#create-depth-stencil-state)
-   [Binden Depth-Stencil Daten an die OM-Phase](#bind-depth-stencil-data-to-the-om-stage)

Sobald Sie wissen, wie Sie den Tiefenschablonenpuffer und den entsprechenden Tiefenschablonenzustand verwenden, lesen Sie [erweiterte Schablonentechniken.](#advanced-stencil-techniques)

## <a name="create-a-depth-stencil-resource"></a>Erstellen einer Depth-Stencil-Ressource

Erstellen Sie den Tiefenschablonenpuffer mithilfe einer Texturressource.


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a>Erstellen Depth-Stencil Zustands

Der Tiefenschablonenzustand teilt der Ausgabezusammenführungsphase mit, wie der [Tiefenschablonentest](d3d10-graphics-programming-guide-output-merger-stage.md)ausgeführt werden soll. Der Tiefenschablonentest bestimmt, ob ein bestimmtes Pixel gezeichnet werden soll.


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



DepthEnable und StencilEnable aktivieren (und deaktivieren) Tiefen- und Schablonentests. Legen Sie DepthEnable auf **FALSE** fest, um Tiefentests zu deaktivieren und das Schreiben in den Tiefenpuffer zu verhindern. Legen Sie StencilEnable auf **FALSE** fest, um Schablonentests zu deaktivieren und das Schreiben in den Schablonenpuffer zu verhindern (wenn DepthEnable **auf FALSE** und StencilEnable auf **TRUE** festgelegt ist, besteht der Tiefentest immer im Schablonenvorgang).

DepthEnable wirkt sich nur auf die Ausgabezusammenführungsphase aus. Sie wirkt sich nicht auf clipping, depth bias oder das Zusammenbinden von Werten aus, bevor die Daten in einen Pixel-Shader eingegeben werden.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Binden Depth-Stencil Daten an die OM-Phase

Binden Sie den Tiefenschablonenzustand.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Binden Sie die Tiefenschablonenressource mithilfe einer Ansicht.


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



Ein Array von Renderzielansichten kann an [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)übergeben werden. Alle diese Renderzielansichten entsprechen jedoch einer einzelnen Tiefenschablonenansicht. Das Renderzielarray in Direct3D 11 ist ein Feature, das es einer Anwendung ermöglicht, auf mehreren Renderzielen gleichzeitig auf primitiver Ebene zu rendern. Renderzielarrays bieten eine höhere Leistung als das individuelle Festlegen von Renderzielen mit mehreren Aufrufen von **ID3D11DeviceContext::OMSetRenderTargets** (im Wesentlichen die in Direct3D 9 verwendete Methode).

Renderziele müssen alle denselben Ressourcentyp aufweisen. Wenn Multisample-Antialiasing verwendet wird, müssen alle gebundenen Renderziele und Tiefenpuffer die gleiche Stichprobenanzahl aufweisen.

Wenn ein Puffer als Renderziel verwendet wird, werden Tiefenschablonentests und mehrere Renderziele nicht unterstützt.

-   Bis zu acht Renderziele können gleichzeitig gebunden werden.
-   Alle Renderziele müssen in allen Dimensionen die gleiche Größe aufweisen (Breite und Höhe und Tiefe für 3D oder Arraygröße für \* Arraytypen).
-   Jedes Renderziel kann ein anderes Datenformat aufweisen.
-   Schreibmasken steuern, welche Daten in ein Renderziel geschrieben werden. Das Ausgabesteuerelement "Schreibmasken" auf einem Pro-Renderziel auf Komponentenebene, welche Daten in die Renderziele geschrieben werden.

## <a name="advanced-stencil-techniques"></a>Erweiterte Schablonentechniken

Der Schablonenteil des Tiefenschablonenpuffers kann zum Erstellen von Renderingeffekten wie Compositing, Decaling und Gliederung verwendet werden.

-   [Compositing](#compositing)
-   [Decaling (Dekalieren)](#decaling)
-   [Konturen und Umrisse](#outlines-and-silhouettes)
-   [Zweiseitige Schablone](#two-sided-stencil)
-   [Lesen des Depth-Stencil Puffers als Textur](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Compositing

Ihre Anwendung kann den Schablonenpuffer verwenden, um 2D- oder 3D-Bilder in einer 3D-Szene zusammenzufügen. Eine Maske im Schablonenpuffer wird verwendet, um einen Bereich der Renderingzieloberfläche auszublenden. Gespeicherte 2D-Informationen, z. B. Text oder Bitmaps, können dann in den verdeckten Bereich geschrieben werden. Alternativ kann Ihre Anwendung zusätzliche 3D-Primitive in den schablonenmaskierten Bereich der Renderingzieloberfläche rendern. Es kann sogar eine ganze Szene rendern.

Spiele kombinierten häufig mehrere 3D-Szenen. Beispielsweise zeigen Fahrspiele in der Regel einen Rückspiegel an. Der Spiegel enthält die Ansicht der 3D-Szene hinter dem Treiber. Es handelt sich im Wesentlichen um eine zweite 3D-Szene, die mit der Vorwärtsansicht des Treibers zusammengesetzt ist.

### <a name="decaling"></a>Decaling (Dekalieren)

Direct3D-Anwendungen verwenden die Dekalierung, um zu steuern, welche Pixel aus einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden Decals auf die Bilder von Primitiven an, damit koplanare Polygone ordnungsgemäß gerendert werden können.

Wenn Sie z. B. Reifenmarkierungen und gelbe Linien auf eine Fahrstrecke anwenden, sollten die Kennzeichnungen direkt über der Straße angezeigt werden. Die z-Werte der Markierungen und der Straße sind jedoch identisch. Daher erzeugt der Tiefenpuffer möglicherweise keine saubere Trennung zwischen den beiden. Einige Pixel im primitiven Hintergrundelement können über dem ersten Primitiven gerendert werden und umgekehrt. Das resultierende Bild scheint von Frame zu Frame zu shimmern. Dieser Effekt wird als Z-Fighting oder Flimmering bezeichnet.

Um dieses Problem zu beheben, verwenden Sie eine Schablone, um den Abschnitt des primitiven Hintergrundelements zu maskieren, in dem die Skalierung angezeigt wird. Deaktivieren Sie die Z-Pufferung, und rendern Sie das Bild des ersten Primitiven in den maskierten Bereich der Renderzieloberfläche.

Mehrere Texturmischungen können verwendet werden, um dieses Problem zu lösen.

### <a name="outlines-and-silhouettes"></a>Konturen und Umrisse

Sie können den Schablonenpuffer für abstrakteren Effekt verwenden, z. B. Gliederung und Silhouetting.

Wenn Ihre Anwendung zwei Renderdurchläufe durchläuft – einen zum Generieren der Schablonenmaske und einen zweiten zum Anwenden der Schablonenmaske auf das Bild, aber mit den Primitiven, die im zweiten Durchlauf etwas kleiner sind – enthält das resultierende Bild nur die Kontur des Primitiven. Die Anwendung kann dann den Schablonenmaskenbereich des Bilds mit einer Volltonfarbe füllen, wodurch dem Primitiven ein einprägtes Aussehen gegeben wird.

Wenn die Schablonenmaske die gleiche Größe und Form wie der primitive, den Sie rendern, enthält das resultierende Bild eine Lücke, in der sich der Primitive befinden sollte. Ihre Anwendung kann dann die Lücke mit Schwarz füllen, um eine Mischung des Primitiven zu erzeugen.

### <a name="two-sided-stencil"></a>Two-Sided Schablone

Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonenpuffer verwendet. Die Anwendung berechnet die Schattenvolumen, die durch verdeckende Geometrie umgewandelt werden, indem die Kanten der Kanten berechnet und vom Licht weg in eine Reihe von 3D-Volumes zusammengestellt werden. Diese Volumes werden dann zweimal in den Schablonenpuffer gerendert.

Das erste Rendern zeichnet vorwärts gerichtete Polygone und erhöht die Schablonenpufferwerte. Beim zweiten Rendern werden die rückwärts gerichteten Polygone des Schattenvolumens zeichnet und die Schablonenpufferwerte dekrementiert. Normalerweise brechen sich alle inkrementierten und dekrementierten Werte gegenseitig ab. Die Szene wurde jedoch bereits mit normaler Geometrie gerendert, sodass einige Pixel beim Z-Puffertest fehlschlagen, wenn das Schattenvolumen gerendert wird. Die werte, die im Schablonenpuffer übrig bleiben, entsprechen den Pixeln im Schatten. Diese verbleibenden Schablonenpufferinhalte werden als Maske verwendet, um ein großes, allumfassendes schwarzes Quader alphanumerierend in die Szene einzublenden. Wenn der Schablonenpuffer als Maske fungiert, besteht das Ergebnis darin, Pixel in den Schatten zu dunkler zu machen.

Dies bedeutet, dass die Schattengeometrie zweimal pro Lichtquelle gezeichnet wird, wodurch der Scheitelpunktdurchsatz der GPU unter Druck gesetzt wird. Die zweiseitige Schablonenfunktion wurde entwickelt, um diese Situation zu entschärfen. Bei diesem Ansatz gibt es zwei Sätze des Schablonenzustands (unten benannt), eine für die vorderen Dreiecke und die andere für die hinteren Dreiecke. Auf diese Weise wird nur ein einzelner Durchlauf pro Schattenvolumen pro Licht gezeichnet.

Ein Beispiel für die Implementierung einer zweiseitigen Schablone finden Sie im [ShadowVolume10-Beispiel.](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Lesen des Depth-Stencil Puffers als Textur

Ein inaktiver Tiefenschablonenpuffer kann von einem Shader als Textur gelesen werden. Eine Anwendung, die einen Tiefenschablonenpuffer als Textur liest, wird in zwei Durchläufen gerendert, der erste Durchlauf schreibt in den Tiefenschablonenpuffer und der zweite Durchlauf liest aus dem Puffer. Dadurch kann ein Shader Tiefen- oder Schablonenwerte vergleichen, die zuvor in den Puffer geschrieben wurden, mit dem Wert für das geschweifte Pixel, das gerendert wird. Das Ergebnis des Vergleichs kann verwendet werden, um Effekte wie Schattenzuordnung oder weiche Partikel in einem Partikelsystem zu erstellen.

Um einen Tiefenschablonenpuffer zu erstellen, der sowohl als Tiefenschablonenressource als auch als Shaderressource verwendet werden kann, müssen einige Änderungen am Beispielcode im Abschnitt [Erstellen einer Depth-Stencil Ressource](#create-a-depth-stencil-resource) vorgenommen werden.

-   Die Tiefenschablonenressource muss ein typloses Format wie DXGI \_ FORMAT \_ R32 \_ TYPELESS aufweisen.
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   Die Tiefenschablonenressource muss die Bindungsflags D3D10 \_ BIND \_ DEPTH \_ STENCIL und D3D10 \_ BIND \_ SHADER RESOURCE \_ verwenden.
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

Darüber hinaus muss eine Shaderressourcenansicht für den Tiefenpuffer mithilfe einer [**D3D11 \_ SHADER \_ RESOURCE VIEW \_ \_ DESC-Struktur**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) und [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)erstellt werden. Die Shaderressourcenansicht verwendet ein typisiertes Format wie **DXGI \_ FORMAT \_ R32 \_ FLOAT,** das dem typlosen Format entspricht, das beim Erstellen der Tiefenschablonenressource angegeben wurde.

Im ersten Renderdurchlauf wird der Tiefenpuffer wie im Abschnitt [Binden von Depth-Stencil Daten an die OM-Phase](#bind-depth-stencil-data-to-the-om-stage) beschrieben gebunden. Beachten Sie, dass das format an [**D3D11 \_ DEPTH \_ STENCIL \_ VIEW \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)übergeben wird. Format verwendet ein typisiertes Format wie **DXGI \_ FORMAT \_ D32 \_ FLOAT**. Nach dem ersten Renderdurchlauf enthält der Tiefenpuffer die Tiefenwerte für die Szene.

Im zweiten Renderdurchlauf wird die [**Id3D11DeviceContext::OMSetRenderTargets-Funktion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) verwendet, um die Tiefenschablonenansicht auf **NULL** oder eine andere Tiefenschablonenressource festzulegen, und die Shaderressourcenansicht wird mit [**id3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md)an den Shader übergeben. Dadurch kann der Shader die im ersten Renderingdurchlauf berechneten Tiefenwerte nachschlagen. Beachten Sie, dass eine Transformation angewendet werden muss, um Tiefenwerte abzurufen, wenn sich der Standpunkt des ersten Renderdurchlaufs vom zweiten Renderdurchlauf unterscheidet. Wenn z. B. eine Schattenzuordnungstechnik verwendet wird, wird der erste Renderdurchlauf aus der Perspektive einer Lichtquelle durchgeführt, während der zweite Renderdurchlauf aus sicht des Betrachters erfolgt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabezusammenführungsphase](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 