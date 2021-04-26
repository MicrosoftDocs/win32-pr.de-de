---
title: Shadermodell 5.1-Objekte
description: Die folgenden Objekte wurden dem Shadermodell 5.1 hinzugefügt.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c56fbe035f63bd8f25a8b34377c333c2ce9946c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993857"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="71950-103">Shadermodell 5.1-Objekte</span><span class="sxs-lookup"><span data-stu-id="71950-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="71950-104">Die folgenden Objekte wurden dem Shadermodell 5.1 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="71950-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="71950-105">Für die [Rasterizer-Auftragsansichten](/windows/desktop/direct3d11/rasterizer-order-views) (verfügbar in D3D11.3 und D3D12) sind die folgenden Objekte neu und nur im Pixelshader zulässig.</span><span class="sxs-lookup"><span data-stu-id="71950-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="71950-106">Beachten Sie, dass die unterstützten Methoden mit den entsprechenden UAV-Objekten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="71950-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="71950-107">Rasterizer-Objekt</span><span class="sxs-lookup"><span data-stu-id="71950-107">Rasterizer Object</span></span>                  | <span data-ttu-id="71950-108">UAV-Objekt</span><span class="sxs-lookup"><span data-stu-id="71950-108">UAV Object</span></span>                                                    |
| <span data-ttu-id="71950-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="71950-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="71950-110">**Rwbuffer**</span><span class="sxs-lookup"><span data-stu-id="71950-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="71950-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="71950-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="71950-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="71950-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="71950-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="71950-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="71950-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="71950-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="71950-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="71950-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="71950-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="71950-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="71950-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="71950-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="71950-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="71950-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="71950-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="71950-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="71950-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="71950-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="71950-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="71950-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="71950-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="71950-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="71950-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="71950-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="71950-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="71950-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="71950-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71950-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71950-126">Shadermodell 5.1</span><span class="sxs-lookup"><span data-stu-id="71950-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="71950-127">HLSL Shader Model 5.1 Features for Direct3D 12 (HLSL-Shadermodell 5.1-Features für Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="71950-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
