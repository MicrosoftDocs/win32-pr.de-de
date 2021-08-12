---
description: Zum Erstellen auf dem Bildschirm oder zum Ausführen von Gleitkommavorgängen müssen Sie im richtigen Farbraum arbeiten.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Konvertieren von Daten für den Farbraum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391d7e1cfd2882603529e28261e6872020dfbb1bbf461a9fd6f5d03efb3aaee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289635"
---
# <a name="converting-data-for-the-color-space"></a>Konvertieren von Daten für den Farbraum

Zum Erstellen auf dem Bildschirm oder zum Ausführen von Gleitkommavorgängen müssen Sie im richtigen Farbraum arbeiten. Es wird empfohlen, Gleitkommavorgänge in einem linearen Farbraum auszuführen. Konvertieren Sie dann die Daten in standardmäßigen RGB-Datenfarbraum (sRGB, gamma 2.2-korrigiert), um Ihre Bilder auf dem Bildschirm darzustellen. Die Darstellung auf dem Bildschirm im sRGB-Farbraum ist wichtig für die Farbgenauigkeit. Wenn Bilder nicht gamma 2.2-korrigiert werden, weisen sie zu viele Bits oder zu viel Bandbreite zu, um hervorzustellen, dass Personen nicht unterscheiden können, und zu wenige Bits oder Bandbreite für Schattenwerte, für die Personen sensibel sind, und würden daher mehr Bits oder Bandbreite benötigen, um die gleiche visuelle Qualität aufrechtzuerhalten. Um die beste Farbgenauigkeit sicherzustellen, zeigen Sie daher Bilder auf dem Bildschirm an, die mit Gamma 2,2 korrigiert wurden.

-   [Farbgenauigkeit](#color-accuracy)
-   [Zugehörige Themen](#related-topics)

## <a name="color-accuracy"></a>Farbgenauigkeit

Zur Darstellung enthalten Anzeigeformate mit ganzzahligen Werten (z. B. [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) [**DXGI \_ FORMAT \_ R10G10B10 \_ XR BIAS \_ \_ A2 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)usw.) immer sRGB-gammakorrelierte Daten. Gleitkommaanzeigeformate (derzeit nur [**DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT)**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)enthalten Linearwertdaten.

Der \_ [SRGB-Formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) gibt dem Betriebssystem an, dass die App sRGB-Daten auf dem Bildschirm platzieren kann. Die App muss sRGB-Daten immer in Hintergrundpuffern mit ganzzahligen Formaten platzieren, um die sRGB-Daten auf dem Bildschirm darzustellen, auch wenn die Daten nicht über diesen Formatmodifizierer im Formatnamen verfügen. Eine vollständige Liste der Anzeige-Scan-Out-Formate:

-   [DXGI-Formatunterstützung für Direct3D Feature Level 12.1-Hardware](hardware-support-for-direct3d-12-1-formats.md)
-   [DXGI-Formatunterstützung für Direct3D Feature Level 12.0-Hardware](hardware-support-for-direct3d-12-0-formats.md)
-   [DXGI-Formatunterstützung für Direct3D-Featureebene 11.1-Hardware](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [DXGI-Formatunterstützung für Direct3D Feature Level 11.0-Hardware](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Hardwareunterstützung für Direct3D 10Level9-Formate](/previous-versions//ff471324(v=vs.85))
-   [Hardwareunterstützung für Direct3D 10.1-Formate](/previous-versions//cc627091(v=vs.85))
-   [Hardwareunterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

Wenn Sie Gleitkommaausgabewerte aus dem Pixel-Shader mit dem SRGB-Formatmodifizierer, der an die Pipeline gebunden ist, in Renderzielansichten **(RenderTargetView** s) \_ schreiben, konvertieren Sie sie in gamma 2.2-korrigierten [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Farbraum. [](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline) Wenn Shader-Ressourcenansichten **(ShaderResourceView** s) mit dem \_ SRGB-Formatmodifizierer an die Pipeline gebunden sind, konvertieren Sie die Werte aus dem gamma 2.2 korrigierten Farbraum in linearen Farbraum, wenn Sie sie aus **shaderResourceView** s lesen. Der Shader kann dann Vorgänge für sie ausführen.

Verwenden Sie beispielsweise codeähnlichen Code, um Gleitkommaausgabewerte aus einem Shader in ein **RenderTargetView-Format** zu schreiben:


```
struct PSOut
{
    float4 color : SV_Target;
};

PSOut S( PSIn input )
{
    PSOut output;
    output.color = float4( 1.0, 0.0, 0.0, 1.0 );
    return output;
}
```



Wenn die S-Routine zurückgegeben wird, werden die Gleitkommawerte (1, 0, 0, 1) in das **RenderTargetView-Format** konvertiert. Wenn Sie dann den \_ [SRGB-Formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) **renderTargetView** zuweisen, erfolgt die Gammakonvertierung.

Mit diesen Schritten wird sichergestellt, dass der auf dem Bildschirm angezeigte Inhalt die beste Farbgenauigkeit aufwies.

**So stellen Sie die Farbgenauigkeit in der Pipeline sicher**

1.  Wenn eine Textur über sRGB-Inhalt verfügt, stellen Sie sicher, dass **ShaderResourceView** über den \_ SRGB-Formatmodifizierer verfügt. Wenn Sie also aus **ShaderResourceView** in den Shader lesen, konvertieren Sie den Texturinhalt von gamma 2.2-korrigierten Farbraum in linearen Farbraum. [](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
2.  Stellen Sie sicher, dass **renderTargetView** auch über den \_ [SRGB-Formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) verfügt, damit die Shaderausgabewerte gamma konvertiert werden.

Wenn Sie die vorherigen Schritte ausführen, hat der inhalt, der auf dem Bildschirm angezeigt wird, die beste Farbgenauigkeit, wenn Sie die [**IDXGISwapChain1::P resent1-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) aufrufen.

Sie können die [**ID3D11Device::CreateRenderTargetView-Methode**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) verwenden, um **\_ DXGI FORMAT \_ \* \_ SRGB-Ansichten** für Hintergrundpuffer aus einer Swapkette zu erstellen, die Sie nur mit einem **\_ DXGI FORMAT \_ \* \_ UNORM-Format** erstellen. Dies ist eine besondere Ausnahme von der Regel zum Erstellen von Renderzielsichten, die besagt, dass Sie ein anderes Format mit **ID3D11Device::CreateRenderTargetView** nur verwenden können, wenn Sie die Ressource erstellt haben, die Sie mit **DXGI \_ FORMAT \_ \* \_ TYPELESS** anzeigen möchten.

Weitere Informationen zu Regeln zum Konvertieren von Daten finden Sie unter [Datenkonvertierungsregeln.](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion)

Informationen zum gleichzeitigen Lesen von und Schreiben in eine Textur finden Sie unter [Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Darstellung mit dem Flip-Modell, den geänderten Rechtecke und scrollbaren Bereichen](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
