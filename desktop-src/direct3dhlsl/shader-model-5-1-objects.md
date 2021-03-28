---
title: Shader-Modell 5,1-Objekte
description: Die folgenden Objekte wurden dem Shader-Modell 5,1 hinzugefügt.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315573"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="4b5c9-103">Shader-Modell 5,1-Objekte</span><span class="sxs-lookup"><span data-stu-id="4b5c9-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="4b5c9-104">Die folgenden Objekte wurden dem Shader-Modell 5,1 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4b5c9-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="4b5c9-105">Die folgenden Objekte sind für die [Reihenfolge Sichten der Rasterizer](/windows/desktop/direct3d11/rasterizer-order-views) (verfügbar in D3D 11.3 und D3D12) neu und nur im Pixelshader zulässig.</span><span class="sxs-lookup"><span data-stu-id="4b5c9-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="4b5c9-106">Beachten Sie, dass die Methoden, die Sie unterstützen, mit den entsprechenden UAV-Objekten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="4b5c9-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="4b5c9-107">Rasterizer-Objekt</span><span class="sxs-lookup"><span data-stu-id="4b5c9-107">Rasterizer Object</span></span>                  | <span data-ttu-id="4b5c9-108">UAV-Objekt</span><span class="sxs-lookup"><span data-stu-id="4b5c9-108">UAV Object</span></span>                                                    |
| <span data-ttu-id="4b5c9-109">Rasterizerorderedbuffer</span><span class="sxs-lookup"><span data-stu-id="4b5c9-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="4b5c9-110">**Rwbuffer**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="4b5c9-111">Rasterizerorderedbyteaddressbuffer</span><span class="sxs-lookup"><span data-stu-id="4b5c9-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="4b5c9-112">**Rwbyteaddressbuffer**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="4b5c9-113">Rasterizerorderedstructuredbuffer</span><span class="sxs-lookup"><span data-stu-id="4b5c9-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="4b5c9-114">**Rwstructuredbuffer**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="4b5c9-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="4b5c9-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="4b5c9-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="4b5c9-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="4b5c9-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="4b5c9-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="4b5c9-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="4b5c9-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="4b5c9-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="4b5c9-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="4b5c9-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="4b5c9-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="4b5c9-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="4b5c9-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="4b5c9-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="4b5c9-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="4b5c9-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b5c9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b5c9-126">Shadermodell 5,1</span><span class="sxs-lookup"><span data-stu-id="4b5c9-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="4b5c9-127">HLSL-Shader-Modell 5,1 Features für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="4b5c9-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 