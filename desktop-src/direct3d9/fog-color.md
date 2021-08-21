---
description: Die Farbtonfarbe für Pixel- und Scheitelpunkt-Scheitelpunkt wird über den \_ D3DRS-RENDERZUSTAND VONCOLOR festgelegt. Die Renderzustandswerte können eine beliebige RGB-Farbe sein, die als RGBA-Farbe angegeben ist. Die Alphakomponente wird ignoriert.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Farbverlauf (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 395bb17c9d6495ade54bc7c761b8c8024c53fbd9a51f620a45ee3a807dc6e20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988000"
---
# <a name="fog-color-direct3d-9"></a>Farbverlauf (Direct3D 9)

Die Farbtonfarbe für Pixel- und Scheitelpunkt-Scheitelpunkt wird über den \_ D3DRS-RENDERZUSTAND VONCOLOR festgelegt. Die Renderzustandswerte können eine beliebige RGB-Farbe sein, die als RGBA-Farbe angegeben ist. Die Alphakomponente wird ignoriert.

Im folgenden C++-Beispiel wird die Farbe des Farbtons auf Weiß festgelegt.


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



Die Feste Funktionspipeline und die programmierbare Pipeline werden unterschiedlich angewendet.

1.  Wenn der Treiber D3DPMISCCAPS \_ VERSCHIEBANDSPEULARALPHA unterstützt:
    -   Wenn die Feste Funktionspipeline verwendet wird und D3DRSCOLOR \_ festgelegt ist, entspricht v1.w (im Pixelshader) dem wert, der im Renderzustand "renderstate" festgelegt ist.
    -   Wenn die programmierbare Pipeline verwendet wird, entspricht v1.w (im Pixel-Shader) 0, auch wenn oD1.w explizit in einen Vertex-Shader geschrieben wird.
2.  Wenn der Treiber D3DPMISCCAPS \_ VERSCHIEBANDSPEULARALPHA NICHT unterstützt:
    -   Wenn die Feste Funktionspipeline verwendet wird und D3DRSCOLOR \_ festgelegt ist, entspricht v1.w (im Pixel-Shader) dem wert, der im Renderzustand "renderstate" festgelegt ist.
    -   Wenn oFog explizit in einen Vertex-Shader geschrieben wird, entspricht v1.w (im Pixel-Shader) oFog, die zwischen 0 und 1 klammern.
    -   Wenn keiner der beiden oben genannten Fälle zutrifft, entspricht v1.w (im Pixel-Shader) 0, auch wenn oD1.w explizit in einen Vertex-Shader geschrieben wird.

Weitere Informationen finden Sie unter [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Typen von Typen](fog-types.md)
</dt> </dl>

 

 



