---
description: Funktionsflags für Pixelshader.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127533"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="98857-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="98857-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="98857-104">Funktionsflags für Pixelshader.</span><span class="sxs-lookup"><span data-stu-id="98857-104">Pixel shader capability flags.</span></span>



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98857-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="98857-105">\#define</span></span>                                     | <span data-ttu-id="98857-106">Wert</span><span class="sxs-lookup"><span data-stu-id="98857-106">Value</span></span>          | <span data-ttu-id="98857-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98857-107">Description</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="98857-108">D3DD3DPSHADERCAPS2 \_ 0, \_ willkürliche aryswizzle</span><span class="sxs-lookup"><span data-stu-id="98857-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="98857-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="98857-109">(1 << 0)</span></span> | <span data-ttu-id="98857-110">Willkürliche swizzelnder werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98857-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="98857-111">D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions</span><span class="sxs-lookup"><span data-stu-id="98857-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="98857-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="98857-112">(1 << 1)</span></span> | <span data-ttu-id="98857-113">Farbverlaufs Anweisungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98857-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="98857-114">D3DD3DPSHADERCAPS2 \_ 0- \_ Prädikat</span><span class="sxs-lookup"><span data-stu-id="98857-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="98857-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="98857-115">(1 << 2)</span></span> | <span data-ttu-id="98857-116">Das Anweisungs Prädikat wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="98857-116">Instruction predication is supported.</span></span> <span data-ttu-id="98857-117">Weitere Informationen finden Sie unter [SETP \_ Comp-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="98857-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="98857-118">D3DD3DPSHADERCAPS2 \_ 0 \_ nodependentleslimit</span><span class="sxs-lookup"><span data-stu-id="98857-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="98857-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="98857-119">(1 << 3)</span></span> | <span data-ttu-id="98857-120">Es gibt keine Beschränkung für die Anzahl der abhängigen Lesevorgänge pro Anweisung.</span><span class="sxs-lookup"><span data-stu-id="98857-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="98857-121">D3DD3DPSHADERCAPS2 \_ 0 \_ notexinstructionlimit</span><span class="sxs-lookup"><span data-stu-id="98857-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="98857-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="98857-122">(1 << 4)</span></span> | <span data-ttu-id="98857-123">Es gibt keine Beschränkung für die Anzahl der TeX-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="98857-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="98857-124">D3DPS20 \_ Max \_ dynamicflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="98857-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="98857-125">24</span><span class="sxs-lookup"><span data-stu-id="98857-125">24</span></span>             | <span data-ttu-id="98857-126">Die maximale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen (Break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="98857-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="98857-127">D3DPS20 \_ Min \_ dynamicflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="98857-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="98857-128">0</span><span class="sxs-lookup"><span data-stu-id="98857-128">0</span></span>              | <span data-ttu-id="98857-129">Die minimale Schachtelungs Ebene der dynamischen Fluss Steuerungs Anweisungen (Break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="98857-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="98857-130">D3DPS20 \_ Max. \_ numTemps</span><span class="sxs-lookup"><span data-stu-id="98857-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="98857-131">32</span><span class="sxs-lookup"><span data-stu-id="98857-131">32</span></span>             | <span data-ttu-id="98857-132">Der Treiber unterstützt höchstens dieses viele temporäre Register.</span><span class="sxs-lookup"><span data-stu-id="98857-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="98857-133">D3DPS20 \_ Min. \_ numTemps</span><span class="sxs-lookup"><span data-stu-id="98857-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="98857-134">12</span><span class="sxs-lookup"><span data-stu-id="98857-134">12</span></span>             | <span data-ttu-id="98857-135">Der Treiber unterstützt mindestens dieses viele temporäre Register.</span><span class="sxs-lookup"><span data-stu-id="98857-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="98857-136">D3DPS20 \_ Max \_ staticflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="98857-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="98857-137">4</span><span class="sxs-lookup"><span data-stu-id="98857-137">4</span></span>              | <span data-ttu-id="98857-138">Die maximale [Schachtelungs Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="98857-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="98857-139">D3DPS20 \_ Min \_ staticflowcontroltiefe</span><span class="sxs-lookup"><span data-stu-id="98857-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="98857-140">1</span><span class="sxs-lookup"><span data-stu-id="98857-140">1</span></span>              | <span data-ttu-id="98857-141">Die minimale Tiefe der [Schachtelung der Schleifen-vs](../direct3dhlsl/loop---vs.md) / [-](../direct3dhlsl/rep---vs.md) und [](../direct3dhlsl/call---vs.md) / [callnz-bool-vs-](../direct3dhlsl/callnz-bool---vs.md) Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="98857-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="98857-142">D3DPS20 \_ Max. \_ numinstructionslots</span><span class="sxs-lookup"><span data-stu-id="98857-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="98857-143">512</span><span class="sxs-lookup"><span data-stu-id="98857-143">512</span></span>            | <span data-ttu-id="98857-144">Der Treiber unterstützt höchstens diese zahlreichen Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="98857-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="98857-145">D3DPS20 \_ Min. \_ numinstructionslots</span><span class="sxs-lookup"><span data-stu-id="98857-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="98857-146">96</span><span class="sxs-lookup"><span data-stu-id="98857-146">96</span></span>             | <span data-ttu-id="98857-147">Der Treiber unterstützt mindestens diese Anzahl von Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="98857-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="98857-148">Diese Konstanten werden vom D3DPSHADERCAPS2 0- \_ Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="98857-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="98857-149">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="98857-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="98857-150">Header</span><span class="sxs-lookup"><span data-stu-id="98857-150">Header</span></span>                   | <span data-ttu-id="98857-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="98857-151">d3d9caps.h</span></span> |
| <span data-ttu-id="98857-152">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="98857-152">Minimum operating system</span></span> | <span data-ttu-id="98857-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="98857-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="98857-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="98857-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98857-155">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="98857-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="98857-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="98857-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
