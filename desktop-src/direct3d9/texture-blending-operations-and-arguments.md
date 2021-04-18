---
description: Anwendungen ordnen jeder Textur im Satz der aktuellen Texturen eine Mischungs Stufe zu. Direct3D wertet jede Mischungs Phase in der Reihenfolge aus, beginnend mit der ersten Textur in der Menge und endet mit der achten.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Textur Mischungs Vorgänge und Argumente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344178"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="d8247-104">Textur Mischungs Vorgänge und Argumente (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d8247-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="d8247-105">Anwendungen ordnen jeder Textur im Satz der aktuellen Texturen eine Mischungs Stufe zu.</span><span class="sxs-lookup"><span data-stu-id="d8247-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="d8247-106">Direct3D wertet jede Mischungs Phase in der Reihenfolge aus, beginnend mit der ersten Textur in der Menge und endet mit der achten.</span><span class="sxs-lookup"><span data-stu-id="d8247-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="d8247-107">Direct3D wendet die Informationen aus jeder Textur im Satz aktueller Texturen auf die zugeordnete Mischungs Phase an.</span><span class="sxs-lookup"><span data-stu-id="d8247-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="d8247-108">Anwendungen steuern, welche Informationen aus einer Textur Phase durch Aufrufen von [**IDirect3DDevice9:: settexturestagestate**](/windows/desktop/api)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8247-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="d8247-109">Sie können separate Vorgänge für die Farb-und Alphakanäle festlegen, und jeder Vorgang verwendet zwei Argumente.</span><span class="sxs-lookup"><span data-stu-id="d8247-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="d8247-110">Angeben von farbchannelvorgängen mithilfe des D3DTSS \_ colorop-Phasen Zustands; angeben von Alpha-Vorgängen mithilfe von D3DTSS \_ alphaop.</span><span class="sxs-lookup"><span data-stu-id="d8247-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="d8247-111">Beide Stufen Zustände verwenden Werte aus dem [**D3DTEXTUREOP**](./d3dtextureop.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="d8247-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="d8247-112">Textur Mischungs Argumente verwenden die Member D3DTSS \_ COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 und D3DTSS ALPHARG2 \_ des [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="d8247-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="d8247-113">Die entsprechenden Argument Werte werden mithilfe von [D3DTA](d3dta.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d8247-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="d8247-114">Sie können eine Textur Phase und alle nachfolgenden Textur Mischungs Stufen in der Cascade-Einstellung deaktivieren, indem Sie den Farb Vorgang für diese Phase auf D3DTOP \_ deaktivieren festlegen.</span><span class="sxs-lookup"><span data-stu-id="d8247-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="d8247-115">Wenn Sie den Farb Vorgang deaktivieren, wird auch der Alpha-Vorgang deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d8247-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="d8247-116">Alpha Vorgänge können nicht deaktiviert werden, wenn Farb Vorgänge aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d8247-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="d8247-117">Das Festlegen des Alpha-Vorgangs auf D3DTOP \_ deaktivieren, wenn die Farbmischung aktiviert ist, verursacht ein nicht definiertes Verhalten</span><span class="sxs-lookup"><span data-stu-id="d8247-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="d8247-118">Um die unterstützten Textur Mischungs Vorgänge eines Geräts zu bestimmen, Fragen Sie den TextureCaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="d8247-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8247-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8247-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8247-120">Textur Mischung</span><span class="sxs-lookup"><span data-stu-id="d8247-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
