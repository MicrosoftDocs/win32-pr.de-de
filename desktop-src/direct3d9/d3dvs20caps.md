---
description: Vertex-Shader-Konstanten Konstanten. Diese Konstanten werden vom VS20Caps-Member von D3DCAPS9 verwendet.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344616"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="39f0a-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="39f0a-104">D3DVS20CAPS</span></span>

<span data-ttu-id="39f0a-105">Vertex-Shader-Konstanten Konstanten.</span><span class="sxs-lookup"><span data-stu-id="39f0a-105">Vertex shader caps constants.</span></span> <span data-ttu-id="39f0a-106">Diese Konstanten werden vom VS20Caps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="39f0a-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="39f0a-107">\#definieren</span><span class="sxs-lookup"><span data-stu-id="39f0a-107">\#define</span></span>                              | <span data-ttu-id="39f0a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="39f0a-108">Value</span></span>          | <span data-ttu-id="39f0a-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39f0a-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f0a-110">D3DVS20CAPS- \_ Prädikat</span><span class="sxs-lookup"><span data-stu-id="39f0a-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="39f0a-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="39f0a-111">(1 << 0)</span></span> | <span data-ttu-id="39f0a-112">Das Anweisungs Prädikat wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39f0a-112">Instruction predication is supported.</span></span> <span data-ttu-id="39f0a-113">Weitere Informationen finden Sie unter [SETP \_ Comp-vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="39f0a-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="39f0a-114">D3DVS20 \_ Max \_ dynamicflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="39f0a-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="39f0a-115">24</span><span class="sxs-lookup"><span data-stu-id="39f0a-115">24</span></span>             | <span data-ttu-id="39f0a-116">Die maximale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen ([break-vs](../direct3dhlsl/break---vs.md), [break- \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [if \_ Comp-vs](../direct3dhlsl/if-comp---vs.md), if \_ Comp-vs, if [pred-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="39f0a-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="39f0a-117">D3DVS20 \_ Min \_ dynamicflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="39f0a-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="39f0a-118">0</span><span class="sxs-lookup"><span data-stu-id="39f0a-118">0</span></span>              | <span data-ttu-id="39f0a-119">Die minimale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen ([break-vs](../direct3dhlsl/break---vs.md), [break- \_ vs](../direct3dhlsl/break-comp---vs.md), [break p-vs](../direct3dhlsl/breakp---vs.md), [if \_ Comp-vs](../direct3dhlsl/if-comp---vs.md), if \_ Comp-vs, if [pred-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="39f0a-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="39f0a-120">D3DVS20 \_ Max. \_ numTemps</span><span class="sxs-lookup"><span data-stu-id="39f0a-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="39f0a-121">32</span><span class="sxs-lookup"><span data-stu-id="39f0a-121">32</span></span>             | <span data-ttu-id="39f0a-122">Die maximal unterstützte Anzahl von temporären Registern.</span><span class="sxs-lookup"><span data-stu-id="39f0a-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="39f0a-123">D3DVS20 \_ Min. \_ numTemps</span><span class="sxs-lookup"><span data-stu-id="39f0a-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="39f0a-124">12</span><span class="sxs-lookup"><span data-stu-id="39f0a-124">12</span></span>             | <span data-ttu-id="39f0a-125">Die Mindestanzahl der unterstützten temporären Register.</span><span class="sxs-lookup"><span data-stu-id="39f0a-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="39f0a-126">D3DVS20 \_ Max \_ staticflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="39f0a-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="39f0a-127">4</span><span class="sxs-lookup"><span data-stu-id="39f0a-127">4</span></span>              | <span data-ttu-id="39f0a-128">Die maximale [Schachtelungs Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="39f0a-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="39f0a-129">D3DVS20 \_ Min \_ staticflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="39f0a-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="39f0a-130">1</span><span class="sxs-lookup"><span data-stu-id="39f0a-130">1</span></span>              | <span data-ttu-id="39f0a-131">Die minimale Tiefe der [Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="39f0a-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="39f0a-132">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="39f0a-132">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="39f0a-133">Header</span><span class="sxs-lookup"><span data-stu-id="39f0a-133">Header</span></span>                   | <span data-ttu-id="39f0a-134">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="39f0a-134">d3d9caps.h</span></span> |
| <span data-ttu-id="39f0a-135">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="39f0a-135">Minimum operating system</span></span> | <span data-ttu-id="39f0a-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="39f0a-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="39f0a-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39f0a-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39f0a-138">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="39f0a-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="39f0a-139">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="39f0a-139">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
