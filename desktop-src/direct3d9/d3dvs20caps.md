---
description: Vertex-Shader kapselt Konstanten. Diese Konstanten werden vom VS20Caps-Member von D3DCAPS9 verwendet.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342945"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="860c6-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="860c6-104">D3DVS20CAPS</span></span>

<span data-ttu-id="860c6-105">Vertex-Shader kapselt Konstanten.</span><span class="sxs-lookup"><span data-stu-id="860c6-105">Vertex shader caps constants.</span></span> <span data-ttu-id="860c6-106">Diese Konstanten werden vom VS20Caps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="860c6-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="860c6-107">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="860c6-107">\#define</span></span>                              | <span data-ttu-id="860c6-108">Wert</span><span class="sxs-lookup"><span data-stu-id="860c6-108">Value</span></span>          | <span data-ttu-id="860c6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="860c6-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="860c6-110">D3DVS20CAPS-PRÄDIKATION \_</span><span class="sxs-lookup"><span data-stu-id="860c6-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="860c6-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="860c6-111">(1 << 0)</span></span> | <span data-ttu-id="860c6-112">Anweisungsprädikation wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="860c6-112">Instruction predication is supported.</span></span> <span data-ttu-id="860c6-113">Siehe [setp \_ comp - vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="860c6-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="860c6-114">D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="860c6-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="860c6-115">24</span><span class="sxs-lookup"><span data-stu-id="860c6-115">24</span></span>             | <span data-ttu-id="860c6-116">Der maximale Grad an Schachtelung dynamischer Ablaufsteuerungsanweisungen ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), wenn comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), wenn \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="860c6-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="860c6-117">D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="860c6-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="860c6-118">0</span><span class="sxs-lookup"><span data-stu-id="860c6-118">0</span></span>              | <span data-ttu-id="860c6-119">Die Mindestebene der Schachtelung dynamischer Ablaufsteuerungsanweisungen ([break - vs](../direct3dhlsl/break---vs.md), break comp - [ \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), wenn \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="860c6-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="860c6-120">D3DVS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="860c6-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="860c6-121">32</span><span class="sxs-lookup"><span data-stu-id="860c6-121">32</span></span>             | <span data-ttu-id="860c6-122">Die maximale Anzahl von unterstützten temporären Registern.</span><span class="sxs-lookup"><span data-stu-id="860c6-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="860c6-123">D3DVS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="860c6-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="860c6-124">12</span><span class="sxs-lookup"><span data-stu-id="860c6-124">12</span></span>             | <span data-ttu-id="860c6-125">Die Mindestanzahl von unterstützten temporären Registern.</span><span class="sxs-lookup"><span data-stu-id="860c6-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="860c6-126">D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="860c6-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="860c6-127">4</span><span class="sxs-lookup"><span data-stu-id="860c6-127">4</span></span>              | <span data-ttu-id="860c6-128">Die maximale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span><span class="sxs-lookup"><span data-stu-id="860c6-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="860c6-129">D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="860c6-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="860c6-130">1</span><span class="sxs-lookup"><span data-stu-id="860c6-130">1</span></span>              | <span data-ttu-id="860c6-131">Die minimale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span><span class="sxs-lookup"><span data-stu-id="860c6-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="860c6-132">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="860c6-132">Constant Information</span></span>



| <span data-ttu-id="860c6-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="860c6-133">Requirement</span></span>                         | <span data-ttu-id="860c6-134">Wert</span><span class="sxs-lookup"><span data-stu-id="860c6-134">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="860c6-135">Header</span><span class="sxs-lookup"><span data-stu-id="860c6-135">Header</span></span>                   | <span data-ttu-id="860c6-136">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="860c6-136">d3d9caps.h</span></span> |
| <span data-ttu-id="860c6-137">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="860c6-137">Minimum operating system</span></span> | <span data-ttu-id="860c6-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="860c6-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="860c6-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="860c6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="860c6-140">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="860c6-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="860c6-141">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="860c6-141">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
