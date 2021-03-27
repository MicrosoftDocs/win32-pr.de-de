---
title: Konfigurieren von Depth-Stencil Funktionen
description: In diesem Abschnitt werden die Schritte zum Einrichten des tiefen Schablone-Puffers und der Status der tiefen Schablone für die Ausgabe-Fusion-Phase behandelt.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728744"
---
# <a name="configuring-depth-stencil-functionality"></a>Konfigurieren von Depth-Stencil Funktionen

In diesem Abschnitt werden die Schritte zum Einrichten des tiefen Schablone-Puffers und der Status der tiefen Schablone für die Ausgabe-Fusion-Phase behandelt.

-   [Erstellen einer Depth-Stencil Ressource](#create-a-depth-stencil-resource)
-   [Depth-Stencil Zustand erstellen](#create-depth-stencil-state)
-   [Binden von Depth-Stencil Daten an die OM-Phase](#bind-depth-stencil-data-to-the-om-stage)

Wenn Sie wissen, wie Sie den tiefen Schablone-Puffer und den entsprechenden Status der tiefen Schablone verwenden, finden Sie weitere Informationen unter [Advanced-Stencil-Techniken](#advanced-stencil-techniques).

## <a name="create-a-depth-stencil-resource"></a>Erstellen einer Depth-Stencil Ressource

Erstellen Sie den tiefen Schablonen Puffer mithilfe einer Textur Ressource.


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



## <a name="create-depth-stencil-state"></a>Depth-Stencil Zustand erstellen

Der Status der tiefen Schablone teilt der Ausgabe-Fusion-Phase mit, wie der [tiefen Schablonen Test](d3d10-graphics-programming-guide-output-merger-stage.md)durchgeführt werden soll. Der tiefen Schablone-Test bestimmt, ob ein bestimmtes Pixel gezeichnet werden soll.


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



Depthenable und stencilenable aktivieren (und deaktivieren) tiefen-und Schablonen Tests. Legen Sie depthenable auf **false** fest, um tiefen Tests zu deaktivieren und das Schreiben in den tiefen Puffer zu verhindern. Legen Sie "Schablone" auf " **false** " fest, um Schablonen Tests zu deaktivieren und das Schreiben in den Schablonen Puffer zu verhindern (wenn "depthenable" den Wert " **false** " hat und "stencilenable" den Wert " **true**" hat, wird der tiefen Test immer in der Schablone

Depthenable wirkt sich nur auf die Ausgabe-Fusion-Phase aus. es wirkt sich nicht auf das Abschneiden, die tiefen Verschiebung oder das Festlegen von Werten aus, bevor die Daten in einen PixelShader eingegeben werden.

## <a name="bind-depth-stencil-data-to-the-om-stage"></a>Binden von Depth-Stencil Daten an die OM-Phase

Binden Sie den Status der tiefen Schablone.


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



Binden Sie die Tiefe der tiefen Schablone mithilfe einer Ansicht.


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



Ein Array von renderzielsichten kann an [**Verknüpfung id3d11devicecontext aus:: omantrendertargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)übermittelt werden. alle renderzielsichten entsprechen jedoch einer einzelnen Ansicht der tiefen Schablone. Das renderzielarray in Direct3D 11 ist eine Funktion, die es einer Anwendung ermöglicht, auf mehreren Renderingzielen gleichzeitig auf primitiver Ebene zu renderzielen. Renderzielarrays bieten eine bessere Leistung im Vergleich zur individuellen Festlegung von renderzielen mit mehreren Aufrufen von **Verknüpfung id3d11devicecontext aus:: omsetrendertargets** (im Wesentlichen die Methode, die in Direct3D 9 verwendet wird).

Renderziele müssen alle den gleichen Ressourcentyp aufweisen. Wenn Multisampling-Antialiasing verwendet wird, müssen alle gebundenen Renderingziele und tiefen Puffer dieselbe Stichproben Anzahl aufweisen.

Wenn ein Puffer als Renderziel verwendet wird, werden tiefen Schablonen Tests und mehrere Renderingziele nicht unterstützt.

-   Bis zu 8 Renderziele können gleichzeitig gebunden werden.
-   Alle Renderziele müssen in allen Dimensionen (Breite und Höhe) und Tiefe für die 3D-oder Array Größe für Array Typen die gleiche Größe aufweisen \* .
-   Jedes Renderziel weist möglicherweise ein anderes Datenformat auf.
-   Schreib Masken steuern, welche Daten in ein Renderziel geschrieben werden. Mit dem Ausgabe Schreibvorgang werden Masken Steuerelemente für ein pro-Renderziel und jede Komponentenebene geschrieben, welche Daten in die Renderziele geschrieben werden.

## <a name="advanced-stencil-techniques"></a>Erweiterte Schablonen Techniken

Der Schablone-Teil des tiefen Schablonen Puffers kann zum Erstellen von renderingeffekten wie zusammensetzen, herabstufen und Gliederung verwendet werden.

-   [Zusammensetzung](#compositing)
-   [Wird abgebrochen](#decaling)
-   [Kontur und Silhouetten](#outlines-and-silhouettes)
-   [Zweiseitige Schablone](#two-sided-stencil)
-   [Lesen des Depth-Stencil Puffers als Textur](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a>Zusammensetzung

Die Anwendung kann mit dem Schablonen Puffer 2D-oder 3D-Bilder in eine 3D-Szene zusammensetzen. Eine Maske im Schablone-Puffer wird verwendet, um einen Bereich der Renderingzieloberfläche zu okzieren. Gespeicherte 2D-Informationen, wie z. b. Text oder Bitmaps, können dann in den Bereich "okded" geschrieben werden. Alternativ kann die Anwendung zusätzliche 3D-primitive in den mit der Schablone maskierten Bereich der Renderingzieloberfläche rendern. Sie kann sogar eine ganze Szene darstellen.

Spiele sind häufig mehrere 3D-Szenen zusammengesetzt. Beispielsweise wird bei Fahr spielen in der Regel eine Spiegelung der Rückseite angezeigt. Die Spiegel Datenbank enthält die Ansicht der 3D-Szene hinter dem Treiber. Es handelt sich im Wesentlichen um eine zweite 3D-Szene, die mit der vorwärts Ansicht des Treibers zusammengesetzt wird

### <a name="decaling"></a>Wird abgebrochen

Direct3D-Anwendungen verwenden die-Verwendung, um zu steuern, welche Pixel von einem bestimmten primitiven Bild auf die Renderingzieloberfläche gezeichnet werden. Anwendungen wenden die Abbilder von primitiven an, damit Coplanar-Polygone ordnungsgemäß wieder hergestellt werden können.

Wenn beispielsweise Reifen Markierungen und gelbe Linien auf eine Straßenebene angewendet werden, sollten die Markierungen direkt auf der Straße angezeigt werden. Die z-Werte der Markierungen und der Straße sind jedoch identisch. Daher erzeugt der tiefen Puffer möglicherweise keine saubere Trennung zwischen den beiden. Einige Pixel im Hintergrundtyp können über dem Front-primitiv und umgekehrt gerendert werden. Das resultierende Bild wird angezeigt, um von Frame zu Rahmen zu vershicheln. Dieser Effekt heißt z-Fighting oder Flimmern.

Um dieses Problem zu beheben, verwenden Sie eine Schablone, um den Abschnitt des hintergrundprimitivs zu maskieren, in dem die Client Zugriffslizenz angezeigt wird. Deaktivieren Sie die z-Pufferung, und Renderern Sie das Bild des Front-Primitivs in den maskierten Bereich der Renderziel-Oberfläche.

Zum lösen dieses Problems können mehrere Textur Mischungs Möglichkeiten verwendet werden.

### <a name="outlines-and-silhouettes"></a>Kontur und Silhouetten

Sie können den Schablonen Puffer für abstraktere Effekte verwenden, z. b. Gliederung und Silhouette.

Wenn die Anwendung zwei Renderungs Ergebnisse übergibt: eine zum Generieren der Schablonen Maske und eine zweite, um die Schablonen Maske auf das Bild anzuwenden, aber mit den primitiven, die im zweiten Durchlauf etwas kleiner sind, enthält das resultierende Bild nur den Umriss des primitiven. Die Anwendung kann dann den Bereich der Schablone maskiert mit einer voll Tonfarbe ausfüllen, wodurch dem primitiven ein geprägte Bild angezeigt wird.

Wenn die Schablone-Maske dieselbe Größe und Form wie das primitive-Format aufweist, das Sie rendern, enthält das resultierende Bild eine Lücke, in der der primitive entsprechen sollte. Die Anwendung kann dann das Loch mit Black auffüllen, um eine Silhouette des primitiven zu schaffen.

### <a name="two-sided-stencil"></a>Two-Sided Schablone

Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonen Puffer verwendet. Die Anwendung berechnet die schattenvolumes, die durch die Schattierung von Geometrie umgewandelt werden, indem die Silhouette-Kanten berechnet und vom Licht in eine Gruppe von 3D-Volumes aufgeteilt werden. Diese Volumes werden dann zweimal im Schablonen Puffer gerendert.

Das erste Rendering zeichnet nach vorne gerichtete Polygone und erhöht die Schablonen Puffer Werte. Das zweite Rendering zeichnet die rückwärts gerichteten Polygone des Schatten Volumens und Dekremente die Schablonen Puffer Werte. Normalerweise brechen alle inkrementierten und dekrementierten Werte einander ab. Die Szene wurde jedoch bereits mit normaler Geometrie gerendert, sodass einige Pixel den z-Puffer-Test nicht bestanden haben, während das Schatten Volume gerendert wird. Werte, die im Schablonen Puffer verbleiben, entsprechen den im Schatten entsprechenden Pixeln. Diese verbleibenden Schablone-Puffer Inhalte werden als Maske verwendet, um einen großen, umfassenden, vier Vierfache in die Szene zu mischen. Wenn der Schablone-Puffer als Maske fungiert, besteht das Ergebnis darin, die Pixel in den Schatten zu verbergen.

Dies bedeutet, dass die Schatten Geometrie zweimal pro Lichtquelle gezeichnet wird und somit den Scheitelpunkt Durchsatz der GPU erhöht. Das zweiseitige Schablonen Feature wurde entwickelt, um diese Situation zu mindern. Bei dieser Vorgehensweise gibt es zwei Sätze von Schablone State (unten genannt), jeweils eine Menge für die Vorder-und die andere für die mit der Rückseite gerichteten Dreiecke. Auf diese Weise wird nur ein einzelner Durchlauf pro Schatten Volume pro Licht gezeichnet.

Ein Beispiel für die zweiseitige Schablonen Implementierung finden Sie im [ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx)-Beispiel.

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a>Lesen des Depth-Stencil Puffers als Textur

Ein inaktiver tiefen Schablone-Puffer kann von einem Shader als Textur gelesen werden. Eine Anwendung, die einen tiefen Schablone-Puffer liest, wenn eine Textur in zwei Durchläufen gerendert wird, wird der erste Pass in den tiefen Schablone-Puffer geschrieben, und der zweite Durchlauf liest aus dem Puffer. Dadurch kann ein Shader Tiefe-oder Schablonen Werte, die zuvor in den Puffer geschrieben wurden, mit dem Wert für das Pixel vergleichen, das in der Vergangenheit gerendert wird. Das Ergebnis des Vergleichs kann verwendet werden, um Effekte wie z. b. eine Schatten Zuordnung oder weiche Partikel in einem Partikelsystem zu erstellen.

Zum Erstellen eines tiefen Schablone-Puffers, der sowohl als tiefen Schablone als auch als Shaderressource verwendet werden kann, müssen einige Änderungen am Beispielcode im Abschnitt [Erstellen einer Depth-Stencil Ressource](#create-a-depth-stencil-resource) vorgenommen werden.

-   Die tiefen Schablone-Ressource muss ein typloses Format aufweisen, wie z. b. das DXGI- \_ Format \_ R32 \_ typlose.
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   Die tiefen Schablone-Ressource muss sowohl die d3d10 Bind- \_ \_ \_ und d3d10 \_ Bind- \_ Shader- \_ ressourcenbindungsflags verwenden.
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

Außerdem muss für den tiefen Puffer eine shaderressourcenansicht erstellt werden, die eine [**D3D11 \_ Shader- \_ Ressourcen \_ Ansicht \_**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) (Debug-Struktur) und " [**ID3D11Device:: | ateshaderresourceview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)" verwendet. Die Shader-Ressourcen Ansicht verwendet ein typisiertes Format, z. b. das **DXGI- \_ Format \_ R32 \_ float** , das dem typlosen Format entspricht, das beim Erstellen der tiefen Schablone-Ressource angegeben wurde.

Im ersten renderdurchlauf wird der tiefen Puffer gebunden, wie im Abschnitt [Binden von Depth-Stencil Daten an den OM-Stufen](#bind-depth-stencil-data-to-the-om-stage) beschrieben. Beachten Sie, dass das Format an die [**D3D11- \_ tiefen \_ Schablone \_ ansichtsansicht \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Das Format verwendet ein typisiertes Format, z. b. **DXGI- \_ Format \_ d32 \_ float**. Nach dem ersten renderdurchlauf enthält der tiefen Puffer die tiefen Werte für die Szene.

Im zweiten Renderpass wird die [**Verknüpfung id3d11devicecontext aus:: omsetrendertargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) -Funktion verwendet, um die Ansicht der tiefen Schablone auf **null** oder eine andere Tiefe der tiefen Schablone festzulegen, und die Shader-Ressourcen Ansicht wird mithilfe von [**ID3D11EffectShaderResourceVariable:: setresource**](id3dx11effectshaderresourcevariable-setresource.md)an den Shader übergeben. Dies ermöglicht es dem Shader, die tiefen Werte zu suchen, die im ersten Renderingdurchlauf berechnet wurden. Beachten Sie, dass eine Transformation zum Abrufen von tiefen Werten angewendet werden muss, wenn sich die Sicht des ersten Renderpass von dem zweiten renderdurchlauf unterscheidet. Wenn z. b. eine schattenmappenmethode verwendet wird, wird der erste renderdurchlauf aus der Perspektive einer Lichtquelle geleitet, während der zweite renderdurchlauf aus der Perspektive des Viewers erfolgt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 