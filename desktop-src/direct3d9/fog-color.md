---
description: Die Nebelfarbe für Pixel und Scheitelpunkt Nebel wird über den D3DRS \_ fogcolor-renderzustand festgelegt. Die Werte für den Rendering-Zustand können eine beliebige RGB-Farbe sein, die als RGBA-Farbe angegeben wird. Die Alpha Komponente wird ignoriert.
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: Nebelfarbe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041113"
---
# <a name="fog-color-direct3d-9"></a>Nebelfarbe (Direct3D 9)

Die Nebelfarbe für Pixel und Scheitelpunkt Nebel wird über den D3DRS \_ fogcolor-renderzustand festgelegt. Die Werte für den Rendering-Zustand können eine beliebige RGB-Farbe sein, die als RGBA-Farbe angegeben wird. Die Alpha Komponente wird ignoriert.

Im folgenden C++-Beispiel wird die Nebelfarbe auf weiß festgelegt.


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



Der Nebel wird von der Fixed-Funktions Pipeline und der programmierbaren Pipeline unterschiedlich angewendet.

1.  Wenn der Treiber D3DPMISCCAPS \_ fogandspecularalpha unterstützt:
    -   Wenn die Fixed-Funktions Pipeline verwendet und D3DRS \_ fogcolor festgelegt wird, entspricht v1. w (im Pixelshader) dem Wert, der in der "Fog renderstate" festgelegt ist.
    -   Wenn die programmierbare Pipeline verwendet wird, ist v1. w (im Pixel-Shader) gleich 0, auch wenn oD1. w explizit in einem Scheitelpunkt-Shader geschrieben wird.
2.  Wenn der Treiber D3DPMISCCAPS \_ fogandspecularalpha nicht unterstützt:
    -   Wenn die Fixed-Funktions Pipeline verwendet und D3DRS \_ fogcolor festgelegt wird, ist v1. w (im Pixel-Shader) der Wert, der in der "Fog renderstate"-Eigenschaft festgelegt ist.
    -   Wenn ofog explizit in einem Scheitelpunkt-Shader geschrieben wird, ist v1. w (im Pixel-Shader) ofog, geklemmt zwischen 0 und 1.
    -   Wenn keines der beiden oben genannten Fälle zutrifft, ist v1. w (im Pixel-Shader) gleich 0, auch wenn oD1. w explizit in einem Scheitelpunkt-Shader geschrieben wird.

Weitere Informationen finden Sie unter [D3DPMISCCAPS](d3dpmisccaps.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nebel Typen](fog-types.md)
</dt> </dl>

 

 



