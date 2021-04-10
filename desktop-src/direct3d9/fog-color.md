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
# <a name="fog-color-direct3d-9"></a><span data-ttu-id="c5a41-105">Nebelfarbe (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c5a41-105">Fog Color (Direct3D 9)</span></span>

<span data-ttu-id="c5a41-106">Die Nebelfarbe für Pixel und Scheitelpunkt Nebel wird über den D3DRS \_ fogcolor-renderzustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5a41-106">Fog color for both pixel and vertex fog is set through the D3DRS\_FOGCOLOR render state.</span></span> <span data-ttu-id="c5a41-107">Die Werte für den Rendering-Zustand können eine beliebige RGB-Farbe sein, die als RGBA-Farbe angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5a41-107">The render state values can be any RGB color, specified as an RGBA color.</span></span> <span data-ttu-id="c5a41-108">Die Alpha Komponente wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c5a41-108">The alpha component is ignored.</span></span>

<span data-ttu-id="c5a41-109">Im folgenden C++-Beispiel wird die Nebelfarbe auf weiß festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5a41-109">The following C++ example sets the fog color to white.</span></span>


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



<span data-ttu-id="c5a41-110">Der Nebel wird von der Fixed-Funktions Pipeline und der programmierbaren Pipeline unterschiedlich angewendet.</span><span class="sxs-lookup"><span data-stu-id="c5a41-110">Fog is applied differently by the fixed function pipeline and the programmable pipeline.</span></span>

1.  <span data-ttu-id="c5a41-111">Wenn der Treiber D3DPMISCCAPS \_ fogandspecularalpha unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c5a41-111">If the driver supports D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="c5a41-112">Wenn die Fixed-Funktions Pipeline verwendet und D3DRS \_ fogcolor festgelegt wird, entspricht v1. w (im Pixelshader) dem Wert, der in der "Fog renderstate" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c5a41-112">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, v1.w (in the pixel shader) equals the value set in fog renderstate.</span></span>
    -   <span data-ttu-id="c5a41-113">Wenn die programmierbare Pipeline verwendet wird, ist v1. w (im Pixel-Shader) gleich 0, auch wenn oD1. w explizit in einem Scheitelpunkt-Shader geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c5a41-113">If the programmable pipeline is used, then v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>
2.  <span data-ttu-id="c5a41-114">Wenn der Treiber D3DPMISCCAPS \_ fogandspecularalpha nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c5a41-114">If the driver does NOT support D3DPMISCCAPS\_FOGANDSPECULARALPHA:</span></span>
    -   <span data-ttu-id="c5a41-115">Wenn die Fixed-Funktions Pipeline verwendet und D3DRS \_ fogcolor festgelegt wird, ist v1. w (im Pixel-Shader) der Wert, der in der "Fog renderstate"-Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c5a41-115">If the fixed function pipeline is used and D3DRS\_FOGCOLOR is set, then v1.w (in the pixel shader) equals value set in fog renderstate.</span></span>
    -   <span data-ttu-id="c5a41-116">Wenn ofog explizit in einem Scheitelpunkt-Shader geschrieben wird, ist v1. w (im Pixel-Shader) ofog, geklemmt zwischen 0 und 1.</span><span class="sxs-lookup"><span data-stu-id="c5a41-116">If oFog is explicitly written in a vertex shader, v1.w (in the pixel shader) equals oFog, clamped between 0 and 1.</span></span>
    -   <span data-ttu-id="c5a41-117">Wenn keines der beiden oben genannten Fälle zutrifft, ist v1. w (im Pixel-Shader) gleich 0, auch wenn oD1. w explizit in einem Scheitelpunkt-Shader geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c5a41-117">If neither of the above two cases applies, v1.w (in the pixel shader) equals 0, even if oD1.w is explicitly written in a vertex shader.</span></span>

<span data-ttu-id="c5a41-118">Weitere Informationen finden Sie unter [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="c5a41-118">For more information, see [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5a41-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5a41-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5a41-120">Nebel Typen</span><span class="sxs-lookup"><span data-stu-id="c5a41-120">Fog Types</span></span>](fog-types.md)
</dt> </dl>

 

 



