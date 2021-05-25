---
description: Treiberschablonenfunktionsflags.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343055"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="a551a-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="a551a-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="a551a-104">Treiberschablonenfunktionsflags.</span><span class="sxs-lookup"><span data-stu-id="a551a-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="a551a-105">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="a551a-105">\#define</span></span>                 | <span data-ttu-id="a551a-106">Wert</span><span class="sxs-lookup"><span data-stu-id="a551a-106">Value</span></span>       | <span data-ttu-id="a551a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a551a-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a551a-108">D3DSTENCILCAPS \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="a551a-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="a551a-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="a551a-109">0x00000001L</span></span> | <span data-ttu-id="a551a-110">Aktualisieren Sie den Eintrag im Schablonenpuffer nicht.</span><span class="sxs-lookup"><span data-stu-id="a551a-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="a551a-111">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="a551a-111">This is the default value.</span></span>                             |
| <span data-ttu-id="a551a-112">D3DSTENCILCAPS \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="a551a-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="a551a-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="a551a-113">0x00000002L</span></span> | <span data-ttu-id="a551a-114">Legen Sie den Eintrag stencil-buffer auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="a551a-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="a551a-115">D3DSTENCILCAPS \_ REPLACE</span><span class="sxs-lookup"><span data-stu-id="a551a-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="a551a-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="a551a-116">0x00000004L</span></span> | <span data-ttu-id="a551a-117">Ersetzen Sie den Eintrag stencil-buffer durch den Verweiswert.</span><span class="sxs-lookup"><span data-stu-id="a551a-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="a551a-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="a551a-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="a551a-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="a551a-119">0x00000008L</span></span> | <span data-ttu-id="a551a-120">Erhöhen Sie den Eintrag für den Schablonenpuffer, und legen Sie dabei den Maximalwert fest.</span><span class="sxs-lookup"><span data-stu-id="a551a-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="a551a-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="a551a-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="a551a-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="a551a-122">0x00000010L</span></span> | <span data-ttu-id="a551a-123">Dekrementieren Sie den Schablonenpuffereintrag, indem Sie auf 0 (null) klammern.</span><span class="sxs-lookup"><span data-stu-id="a551a-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="a551a-124">D3DSTENCILCAPS \_ INVERT</span><span class="sxs-lookup"><span data-stu-id="a551a-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="a551a-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="a551a-125">0x00000020L</span></span> | <span data-ttu-id="a551a-126">Umkehren der Bits im Schablonenpuffereintrag.</span><span class="sxs-lookup"><span data-stu-id="a551a-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="a551a-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="a551a-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="a551a-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="a551a-128">0x00000040L</span></span> | <span data-ttu-id="a551a-129">Inkrementiert den Schablonenpuffereintrag und wird auf 0 (null) gesetzt, wenn der neue Wert den Maximalwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="a551a-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="a551a-130">D3DSTENCILCAPS \_ DECR</span><span class="sxs-lookup"><span data-stu-id="a551a-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="a551a-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="a551a-131">0x00000080L</span></span> | <span data-ttu-id="a551a-132">Dekrementierung des Schablonenpuffereintrags und Umschließen bis zum höchstwert, wenn der neue Wert kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="a551a-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="a551a-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="a551a-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="a551a-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="a551a-134">0x00000100L</span></span> | <span data-ttu-id="a551a-135">Das Gerät unterstützt die zweiseitige Schablone.</span><span class="sxs-lookup"><span data-stu-id="a551a-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="a551a-136">Schablonenpuffereinträge sind ganzzahlige Werte im Bereich von 0 bis 2ⁿ - 1, wobei n die Bittiefe des Schablonenpuffers ist.</span><span class="sxs-lookup"><span data-stu-id="a551a-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="a551a-137">Diese Konstanten werden vom StencilCaps-Member von [**D3DCAPS9 verwendet.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="a551a-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="a551a-138">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="a551a-138">Constant Information</span></span>



| <span data-ttu-id="a551a-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a551a-139">Requirement</span></span>                         | <span data-ttu-id="a551a-140">Wert</span><span class="sxs-lookup"><span data-stu-id="a551a-140">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="a551a-141">Header</span><span class="sxs-lookup"><span data-stu-id="a551a-141">Header</span></span>                   | <span data-ttu-id="a551a-142">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="a551a-142">d3d9caps.h</span></span> |
| <span data-ttu-id="a551a-143">Mindestbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="a551a-143">Minimum operating system</span></span> | <span data-ttu-id="a551a-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="a551a-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a551a-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a551a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a551a-146">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a551a-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



