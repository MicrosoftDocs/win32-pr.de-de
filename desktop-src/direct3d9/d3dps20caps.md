---
description: Pixelshaderfunktionsflags.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995267"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="6cf20-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6cf20-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="6cf20-104">Pixelshaderfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="6cf20-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="6cf20-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="6cf20-105">\#define</span></span>                                     | <span data-ttu-id="6cf20-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6cf20-106">Value</span></span>          | <span data-ttu-id="6cf20-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cf20-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf20-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="6cf20-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="6cf20-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="6cf20-109">(1 << 0)</span></span> | <span data-ttu-id="6cf20-110">Beliebiges Swizzling wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6cf20-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="6cf20-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="6cf20-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="6cf20-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="6cf20-112">(1 << 1)</span></span> | <span data-ttu-id="6cf20-113">Farbverlaufsanweisungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6cf20-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6cf20-114">D3DD3DPSHADERCAPS2 \_ \_ 0-PRÄDIKATION</span><span class="sxs-lookup"><span data-stu-id="6cf20-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="6cf20-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="6cf20-115">(1 << 2)</span></span> | <span data-ttu-id="6cf20-116">Anweisungsprädikation wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6cf20-116">Instruction predication is supported.</span></span> <span data-ttu-id="6cf20-117">Siehe [setp \_ comp - ps](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="6cf20-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="6cf20-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="6cf20-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="6cf20-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="6cf20-119">(1 << 3)</span></span> | <span data-ttu-id="6cf20-120">Es gibt keine Beschränkung für die Anzahl abhängiger Lesefunktionen pro Anweisung.</span><span class="sxs-lookup"><span data-stu-id="6cf20-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="6cf20-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="6cf20-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="6cf20-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="6cf20-122">(1 << 4)</span></span> | <span data-ttu-id="6cf20-123">Es gibt keine Beschränkung für die Anzahl von Texanweisungen.</span><span class="sxs-lookup"><span data-stu-id="6cf20-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="6cf20-124">D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="6cf20-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="6cf20-125">24</span><span class="sxs-lookup"><span data-stu-id="6cf20-125">24</span></span>             | <span data-ttu-id="6cf20-126">Die maximale Schachtelungsebene von Anweisungen für die dynamische Flusssteuerung (Break, Breakc, ifc).</span><span class="sxs-lookup"><span data-stu-id="6cf20-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="6cf20-127">D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="6cf20-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="6cf20-128">0</span><span class="sxs-lookup"><span data-stu-id="6cf20-128">0</span></span>              | <span data-ttu-id="6cf20-129">Die minimale Schachtelungsebene der Anweisungen für die dynamische Flusssteuerung (Break, Breakc, ifc).</span><span class="sxs-lookup"><span data-stu-id="6cf20-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="6cf20-130">D3DPS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="6cf20-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="6cf20-131">32</span><span class="sxs-lookup"><span data-stu-id="6cf20-131">32</span></span>             | <span data-ttu-id="6cf20-132">Der Treiber unterstützt nur diese vielen temporären Registrierungen.</span><span class="sxs-lookup"><span data-stu-id="6cf20-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="6cf20-133">D3DPS20 \_ \_ MIN. NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="6cf20-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="6cf20-134">12</span><span class="sxs-lookup"><span data-stu-id="6cf20-134">12</span></span>             | <span data-ttu-id="6cf20-135">Der Treiber unterstützt mindestens diese vielen temporären Registrierungen.</span><span class="sxs-lookup"><span data-stu-id="6cf20-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="6cf20-136">D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="6cf20-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="6cf20-137">4</span><span class="sxs-lookup"><span data-stu-id="6cf20-137">4</span></span>              | <span data-ttu-id="6cf20-138">Die maximale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span><span class="sxs-lookup"><span data-stu-id="6cf20-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="6cf20-139">D3DPS20 \_ \_ MIN. STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="6cf20-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="6cf20-140">1</span><span class="sxs-lookup"><span data-stu-id="6cf20-140">1</span></span>              | <span data-ttu-id="6cf20-141">Die minimale Tiefe der Schachtelung der Schleife [– vs](../direct3dhlsl/loop---vs.md)rep / [– vs](../direct3dhlsl/rep---vs.md) und call – [vs](../direct3dhlsl/call---vs.md) / [callnz bool – vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span><span class="sxs-lookup"><span data-stu-id="6cf20-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="6cf20-142">D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="6cf20-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="6cf20-143">512</span><span class="sxs-lookup"><span data-stu-id="6cf20-143">512</span></span>            | <span data-ttu-id="6cf20-144">Der Treiber unterstützt alle diese vielen Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="6cf20-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="6cf20-145">D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="6cf20-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="6cf20-146">96</span><span class="sxs-lookup"><span data-stu-id="6cf20-146">96</span></span>             | <span data-ttu-id="6cf20-147">Der Treiber unterstützt mindestens diese vielen Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="6cf20-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="6cf20-148">Diese Konstanten werden vom D3DPSHADERCAPS2 \_ 0-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="6cf20-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="6cf20-149">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="6cf20-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="6cf20-150">Header</span><span class="sxs-lookup"><span data-stu-id="6cf20-150">Header</span></span>                   | <span data-ttu-id="6cf20-151">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="6cf20-151">d3d9caps.h</span></span> |
| <span data-ttu-id="6cf20-152">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="6cf20-152">Minimum operating system</span></span> | <span data-ttu-id="6cf20-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="6cf20-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6cf20-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6cf20-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf20-155">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6cf20-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="6cf20-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="6cf20-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
