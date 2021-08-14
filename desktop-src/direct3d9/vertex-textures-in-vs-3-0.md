---
description: Das Vertex-Shader 3.0-Modell unterstützt die Textursuche im Vertex-Shader mithilfe der texldl - vs texture load-Anweisung.
ms.assetid: 595cb5c0-da12-4fe9-944c-a61d8ed990b4
title: Vertextexturen in vs_3_0 (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4cbd4aa1e1830d29656fea2bc7b028191bee158eede119c9a47ae2457d10e99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519447"
---
# <a name="vertex-textures-in-vs_3_0-directx-hlsl"></a>Vertextexturen in \_ vs. \_ 3 0 (DirectX HLSL)

Das Vertex-Shader 3.0-Modell unterstützt die Textursuche im Vertex-Shader mithilfe der [texldl - vs](../direct3dhlsl/texldl---vs.md) texture load-Anweisung. Die Vertex-Engine enthält vier Textursamplerstufen mit den Namen [D3DVERTEXTEXTURESAMPLER0,](d3dvertextexturesampler.md)D3DVERTEXTEXTURESAMPLER1, D3DVERTEXTEXTURESAMPLER2 und D3DVERTEXTEXTURESAMPLER3. Diese unterscheiden sich von den Verschiebungszuordnungs-Samplern und Texturs samplern in der Pixel-Engine.

Zum Beispiel für Texturen, die in diesen vier Phasen festgelegt sind, können Sie die Scheitelpunkt-Engine verwenden und die Phasen mit der [**CheckDeviceFormat-Methode**](/windows/desktop/api) programmieren. Legen Sie Texturen in diesen Phasen mithilfe von [**SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)mit dem Stufenindex [D3DVERTEXTEXTURESAMPLER0](d3dvertextexturesampler.md) bis D3DVERTEXTEXTURESAMPLER3 fest. Im Vertex-Shader, dem Samplerregister (wie in PS 2 0), wurde ein neues Register eingeführt, das den \_ \_ Vertextextur-Sampler darstellt. Dieses Register muss im Shader definiert werden, bevor es verwendet wird.

Eine Anwendung kann abfragen, ob ein Format als Scheitelpunkttextur unterstützt wird, indem [**sie CheckDeviceFormat**](/windows/desktop/api) mit [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE aufruft.](d3dusage-query.md)

> [!Note]  
> Dies ist ein Abfrageflag, sodass es in einer Createxxx-Funktion nicht akzeptiert wird. Eine im Standardpool erstellte Scheitelpunkttextur kann als Pixeltextur festgelegt werden und umgekehrt. Um die Softwarevertexverarbeitung zu verwenden, muss die Scheitelpunkttextur jedoch im Scratchpool erstellt werden (unabhängig davon, ob es sich um ein Gerät im gemischten Modus oder ein Software-Scheitelpunktverarbeitungsgerät handelt).

 

Die Funktionalität ist mit den Pixeltexturen identisch, mit Ausnahme der folgenden:

-   Die anisotrope Texturfilterung wird nicht unterstützt, daher wird \_ D3DSAMP MAXANISOTROPY ignoriert, und D3DTEXF ANISOTROPIC kann nicht für die Vergrößerung oder Vergrößerung für diese Phasen festgelegt \_ werden.
-   Die Rate der Änderungsinformationen ist nicht verfügbar, daher muss die Anwendung die Detailebene berechnen und diese Informationen als Parameter für [texldl - im](../direct3dhlsl/texldl---vs.md)Vergleich zu bereitstellen.

Es gelten folgende Beschränkungen:

-   Wie bei Pixel-Shadern wird D3DSAMP ELEMENTINDEX verwendet, um herauszufinden, aus welchem Element Stichproben erstellt werden sollen, wenn \_ Mehrelementtexturen unterstützt werden.
-   Der D3DSAMP \_ DMAPOFFSET-Zustand wird für diese Phasen ignoriert.
-   Verwenden [**Sie CheckDeviceFormat**](/windows/desktop/api) mit [D3DUSAGE \_ QUERY \_ VERTEXTEXTURE"](d3dusage-query.md) zum Abfragen einer Textur, um zu überprüfen, ob sie als Scheitelpunkttextur verwendet werden kann.
-   VertexTextureFilterCaps gibt an, welche Arten von Filtern an den Scheitelpunkttextur-Samplern zulässig sind. [D3DPTFILTERCAPS \_ MINFANISOTROPIC und](d3dptfiltercaps.md) D3DPTFILTERCAPS \_ MAGFANISOTROPIC sind nichtig.

## <a name="sampling-stage-registers"></a>Register der Samplingphase

Ein Samplingstufenregister identifiziert eine Samplingeinheit, die in Texturlade-Anweisungen verwendet werden kann. Eine Samplingeinheit entspricht der Textursamplerphase und kapselt den in [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)bereitgestellten samplingspezifischen Zustand.

Jeder Sampler identifiziert eindeutig eine einzelne Texturoberfläche, die mithilfe von SetTexture auf den entsprechenden [**Sampler festgelegt wird.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Die gleiche Texturoberfläche kann jedoch bei mehreren Samplern festgelegt werden.

Zur Zeichnen-Zeit kann eine Textur nicht gleichzeitig als Renderziel und textur in einer Phase festgelegt werden.

Da im Vergleich zu 3 0 vier Sampler unterstützt werden, können bis zu vier Texturoberflächen in einem einzelnen \_ \_ Shaderpass gelesen werden. Ein Samplerregister wird möglicherweise nur als Argument in der Texturlade-Anweisung angezeigt: [texldl - vs](../direct3dhlsl/texldl---vs.md).

Im Vergleich zu 3 0 muss ein Sampler am Anfang des Shaderprogramms mit dem \_ \_ [dcl \_ samplerType (sm3 – vs asm)](../direct3dhlsl/dcl-samplertype---vs.md) deklariert werden (wie in ps \_ 2 \_ 0).

## <a name="software-processing"></a>Softwareverarbeitung

Dieses Feature wird bei der Softwarevertexverarbeitung unterstützt. Die unterstützten Filtertypen können durch Aufrufen von [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) und Überprüfen von VertexTextureFilterCaps überprüft werden. Alle veröffentlichten Texturformate werden als Scheitelpunkttexturen in der Softwarevertexverarbeitung unterstützt.

Anwendungen können überprüfen, ob ein bestimmtes Texturformat im Softwarevertexverarbeitungsmodus unterstützt wird, indem [**sie CheckDeviceFormat**](/windows/desktop/api) aufrufen und (D3DVERTEXTEXTURESAMPLER \| [**D3DUSAGE \_ SOFTWAREPROCESSING)**](d3dusage.md)als Verwendung bereitstellen. Alle Formate werden für die Softwarevertexverarbeitung unterstützt. Der Scratchpool ist für die Softwarevertexverarbeitung erforderlich.

## <a name="api-changes"></a>API-Änderungen


```
   
// New define
#define D3DVERTEXTEXTURESAMPLER0 (D3DDMAPSAMPLER+1)
#define D3DVERTEXTEXTURESAMPLER1 (D3DDMAPSAMPLER+2)
#define D3DVERTEXTEXTURESAMPLER2 (D3DDMAPSAMPLER+3)
#define D3DVERTEXTEXTURESAMPLER3 (D3DDMAPSAMPLER+4)
    

#define D3DVERTEXTEXTURESAMPLER  (0x00100000L)

// New caps field in D3DCAPS9
DWORD VertexTextureFilterCaps;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertexpipeline](vertex-pipeline.md)
</dt> </dl>

 

 
