---
description: Treiber-Schablonenfunktionsflags.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6716748d77fe4c3620413f43ae4a4ae48076c09f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997377"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="9bda2-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="9bda2-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="9bda2-104">Treiber-Schablonenfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="9bda2-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="9bda2-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="9bda2-105">\#define</span></span>                 | <span data-ttu-id="9bda2-106">Wert</span><span class="sxs-lookup"><span data-stu-id="9bda2-106">Value</span></span>       | <span data-ttu-id="9bda2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9bda2-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bda2-108">D3DSTENCILCAPS \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="9bda2-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="9bda2-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="9bda2-109">0x00000001L</span></span> | <span data-ttu-id="9bda2-110">Aktualisieren Sie den Eintrag im Schablonenpuffer nicht.</span><span class="sxs-lookup"><span data-stu-id="9bda2-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="9bda2-111">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9bda2-111">This is the default value.</span></span>                             |
| <span data-ttu-id="9bda2-112">D3DSTENCILCAPS \_ 0 (NULL)</span><span class="sxs-lookup"><span data-stu-id="9bda2-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="9bda2-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="9bda2-113">0x00000002L</span></span> | <span data-ttu-id="9bda2-114">Legen Sie den Schablonenpuffereintrag auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="9bda2-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="9bda2-115">D3DSTENCILCAPS \_ REPLACE</span><span class="sxs-lookup"><span data-stu-id="9bda2-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="9bda2-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="9bda2-116">0x00000004L</span></span> | <span data-ttu-id="9bda2-117">Ersetzen Sie den Schablonenpuffereintrag durch den Verweiswert.</span><span class="sxs-lookup"><span data-stu-id="9bda2-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="9bda2-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="9bda2-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="9bda2-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="9bda2-119">0x00000008L</span></span> | <span data-ttu-id="9bda2-120">Erhöhen Sie den Schablonenpuffereintrag, und klammern Sie sich an den Maximalwert.</span><span class="sxs-lookup"><span data-stu-id="9bda2-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="9bda2-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="9bda2-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="9bda2-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="9bda2-122">0x00000010L</span></span> | <span data-ttu-id="9bda2-123">Dekrementieren Sie den Schablonenpuffereintrag, und klammern Sie an 0 (null).</span><span class="sxs-lookup"><span data-stu-id="9bda2-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="9bda2-124">D3DSTENCILCAPS \_ INVERT</span><span class="sxs-lookup"><span data-stu-id="9bda2-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="9bda2-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="9bda2-125">0x00000020L</span></span> | <span data-ttu-id="9bda2-126">Invertiert die Bits im Schablonenpuffereintrag.</span><span class="sxs-lookup"><span data-stu-id="9bda2-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="9bda2-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="9bda2-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="9bda2-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="9bda2-128">0x00000040L</span></span> | <span data-ttu-id="9bda2-129">Erhöhen Sie den Eintrag stencil-buffer, und umschließen Sie diesen auf 0 (null), wenn der neue Wert den Maximalwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="9bda2-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="9bda2-130">D3DSTENCILCAPS \_ DECR</span><span class="sxs-lookup"><span data-stu-id="9bda2-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="9bda2-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="9bda2-131">0x00000080L</span></span> | <span data-ttu-id="9bda2-132">Dekrementen Sie den Eintrag stencil-buffer, und umschließen Sie den Maximalen Wert, wenn der neue Wert kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="9bda2-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="9bda2-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="9bda2-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="9bda2-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="9bda2-134">0x00000100L</span></span> | <span data-ttu-id="9bda2-135">Das Gerät unterstützt die zweiseitige Schablone.</span><span class="sxs-lookup"><span data-stu-id="9bda2-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="9bda2-136">Schablonenpuffereinträge sind ganzzahlige Werte im Bereich von 0 bis 2ⁿ – 1, wobei n die Bittiefe des Schablonenpuffers ist.</span><span class="sxs-lookup"><span data-stu-id="9bda2-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="9bda2-137">Diese Konstanten werden vom StencilCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="9bda2-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="9bda2-138">Konstanteninformationen</span><span class="sxs-lookup"><span data-stu-id="9bda2-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9bda2-139">Header</span><span class="sxs-lookup"><span data-stu-id="9bda2-139">Header</span></span>                   | <span data-ttu-id="9bda2-140">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="9bda2-140">d3d9caps.h</span></span> |
| <span data-ttu-id="9bda2-141">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="9bda2-141">Minimum operating system</span></span> | <span data-ttu-id="9bda2-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9bda2-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9bda2-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bda2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bda2-144">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9bda2-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



