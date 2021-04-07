---
description: Um auf dem Bildschirm zu verfassen oder Gleit Komma Vorgänge auszuführen, müssen Sie im richtigen Farbraum arbeiten.
ms.assetid: 1DD8E2D3-430F-4EE4-9C41-78736C904920
title: Daten für den Farbraum werden umgerechnet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b5dbec2f826c40d5274cbddb3b54d1cdd9f695
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745936"
---
# <a name="converting-data-for-the-color-space"></a>Daten für den Farbraum werden umgerechnet

Um auf dem Bildschirm zu verfassen oder Gleit Komma Vorgänge auszuführen, müssen Sie im richtigen Farbraum arbeiten. Es wird empfohlen, Gleit Komma Operationen in einem linearen Farbraum auszuführen. Konvertieren Sie dann die Daten in Standard-RGB-Daten (sRGB, Gamma 2,2-korrigiert), um die Bilder auf dem Bildschirm darzustellen. Die Darstellung des Bildschirms im sRGB-Farbraum ist wichtig für die Farbgenauigkeit. Wenn Bilder nicht Gamma 2,2-korrigiert sind, weisen Sie zu viele Bits oder zu viel Bandbreite zu, um zu kennzeichnet, dass Benutzer nicht unterscheiden können, und zu wenige Bits oder Bandbreite, um Schatten Werte zu verwenden, die von den Personen abhängig sind, und somit mehr Bits oder Bandbreite benötigen, um dieselbe visuelle Qualität beizubehalten. Stellen Sie daher Bilder auf dem Bildschirm dar, die Gamma 2,2-korrigiert sind, um die beste Farbgenauigkeit sicherzustellen.

-   [Farbgenauigkeit](#color-accuracy)
-   [Zugehörige Themen](#related-topics)

## <a name="color-accuracy"></a>Farbgenauigkeit

Für die Darstellung enthalten Anzeige Formate mit ganzzahligen Werten (z. b. [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format), [**DXGI \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)usw.) immer sRGB-Daten, die von Gamma korrigiert wurden. Gleit Komma Wert-Anzeige Formate (derzeit nur [**DXGI- \_ Format \_ R16G16B16A16 \_ float**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) enthalten Daten mit linearen Werten.

Der \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) gibt dem Betriebssystem an, dass die APP sRGB-Daten auf dem Bildschirm platzieren soll. Die APP muss sRGB-Daten immer in Back-Puffer mit ganzzahligen Werten platzieren, um die sRGB-Daten auf dem Bildschirm darzustellen, auch wenn die Daten nicht über diesen formatmodifizierer im Format Namen verfügen. Eine komplette Liste der Formate zum Anzeigen von Scans:

-   [DXGI-Format Unterstützung für Direct3D Featureebene 12,1 Hardware](hardware-support-for-direct3d-12-1-formats.md)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 12,0 Hardware](hardware-support-for-direct3d-12-0-formats.md)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 11,1 Hardware](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [DXGI-Format Unterstützung für Direct3D Featureebene 11,0 Hardware](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Hardware Unterstützung für Direct3D 10level9-Formate](/previous-versions//ff471324(v=vs.85))
-   [Hardware Unterstützung für Direct3D 10,1-Formate](/previous-versions//cc627091(v=vs.85))
-   [Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))

Wenn Sie Gleit Komma Ausgabewerte aus dem Pixelshader in **renderzielsichten (rendertargetview** s) mit dem \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) schreiben, der an die [Pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline)gebunden ist, konvertieren Sie Sie in den in Gamma 2,2 korrigierten Farbraum. Ebenso, wenn Shader-Resource-Sichten (**shaderresourceview** s) mit dem \_ sRGB-formatmodifizierer an die Pipeline gebunden sind, konvertieren Sie die Werte aus dem Gamma 2,2-korrigierten Farbraum in den linearen Farbraum, wenn Sie Sie aus den **shaderresourceview** s lesen. Der Shader kann dann Vorgänge für Sie ausführen.

Verwenden Sie z. b. Code, der diesem ähnelt, um Gleit Komma-Ausgabewerte aus einem Shader in ein **rendertargetview** -Format zu schreiben:


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



Wenn die-Routine des s zurückgibt, werden die Gleit Komma Werte (1, 0, 0, 1) in das **rendertargetview** -Format konvertiert. Wenn Sie dann der \_ **rendertargetview** den sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) zuweisen, erfolgt die Gamma Konvertierung.

Diese Schritte müssen ausgeführt werden, um sicherzustellen, dass der auf dem Bildschirm angezeigte Inhalt über die beste Farbgenauigkeit verfügt.

**So sorgen Sie für eine Farbgenauigkeit in der Pipeline**

1.  Wenn eine Textur über sRGB-Inhalt verfügt, stellen Sie sicher, dass **shaderresourceview** den \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) aufweist, sodass Sie den Textur Inhalt von Gamma 2,2-korrigierter Farbraum in den linearen Farbraum konvertieren, wenn Sie aus der **shaderresourceview** in den Shader lesen.
2.  Stellen Sie sicher, dass **rendertargetview** auch den \_ sRGB- [formatmodifizierer](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) aufweist, damit die Shader-Ausgabewerte Gamma konvertiert werden.

Wenn Sie die obigen Schritte ausführen und die [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) -Methode aufruft, hat der auf dem Bildschirm angezeigte Inhalt die beste Farbgenauigkeit.

Mit der [**ID3D11Device:: samaterendertargetview**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview) -Methode können Sie **\_ \_ \* \_ sRGB-Sichten im DXGI-Format** auf Back Puffern aus einer Swapkette erstellen, die Sie nur mit dem **\_ \_ \* \_ unorm-Format DXGI-Format** erstellen. Dies ist eine besondere Ausnahme von der Regel zum Erstellen von renderzielsichten, die besagt, dass Sie ein anderes Format mit **ID3D11Device:: ":: angetview** " verwenden können, nur wenn Sie die Ressource erstellt haben, die Sie mit **\_ \_ \* \_ typlosen DXGI-Format** anzeigen möchten.

Weitere Informationen zu Regeln für das Konvertieren von Daten finden Sie unter [Daten Konvertierungsregeln](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-data-conversion).

Informationen zum gleichzeitigen Lesen aus einer Textur und zum Schreiben in eine Textur finden Sie unter [entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-unpacking-packing-dxgi-format).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern der Präsentation mit dem Flip-Modell, den geänderten Rechtecke und den Bereichen](dxgi-1-2-presentation-improvements.md)
</dt> </dl>

 

 
