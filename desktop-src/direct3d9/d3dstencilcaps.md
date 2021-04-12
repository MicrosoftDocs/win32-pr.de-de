---
description: Funktionsfunktionsflags der Treiber Schablone.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392970"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="e1e7e-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="e1e7e-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="e1e7e-104">Funktionsfunktionsflags der Treiber Schablone.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-104">Driver stencil capability flags.</span></span>



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1e7e-105">\#definieren</span><span class="sxs-lookup"><span data-stu-id="e1e7e-105">\#define</span></span>                 | <span data-ttu-id="e1e7e-106">Wert</span><span class="sxs-lookup"><span data-stu-id="e1e7e-106">Value</span></span>       | <span data-ttu-id="e1e7e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1e7e-107">Description</span></span>                                                                                           |
| <span data-ttu-id="e1e7e-108">D3DSTENCILCAPS \_ beibehalten</span><span class="sxs-lookup"><span data-stu-id="e1e7e-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="e1e7e-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="e1e7e-109">0x00000001L</span></span> | <span data-ttu-id="e1e7e-110">Aktualisieren Sie den Eintrag nicht im Schablonen Puffer.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="e1e7e-111">Dies ist der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-111">This is the default value.</span></span>                             |
| <span data-ttu-id="e1e7e-112">D3DSTENCILCAPS \_ 0</span><span class="sxs-lookup"><span data-stu-id="e1e7e-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="e1e7e-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="e1e7e-113">0x00000002L</span></span> | <span data-ttu-id="e1e7e-114">Legen Sie den Schablone-Puffer Eintrag auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="e1e7e-115">D3DSTENCILCAPS \_ ersetzen</span><span class="sxs-lookup"><span data-stu-id="e1e7e-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="e1e7e-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="e1e7e-116">0x00000004L</span></span> | <span data-ttu-id="e1e7e-117">Ersetzen Sie den Stencil-Buffer-Eintrag durch den Verweis Wert.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="e1e7e-118">D3DSTENCILCAPS \_ incrsat</span><span class="sxs-lookup"><span data-stu-id="e1e7e-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="e1e7e-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="e1e7e-119">0x00000008L</span></span> | <span data-ttu-id="e1e7e-120">Erhöhen Sie den Schablone-Puffer Eintrag, und legen Sie auf den maximalen Wert an.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="e1e7e-121">D3DSTENCILCAPS \_ decrsat</span><span class="sxs-lookup"><span data-stu-id="e1e7e-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="e1e7e-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="e1e7e-122">0x00000010L</span></span> | <span data-ttu-id="e1e7e-123">Dekrement der Schablone-Puffer Eintrag, der auf 0 (null) gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="e1e7e-124">D3DSTENCILCAPS \_ umkehren</span><span class="sxs-lookup"><span data-stu-id="e1e7e-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="e1e7e-125">0x00000020l</span><span class="sxs-lookup"><span data-stu-id="e1e7e-125">0x00000020L</span></span> | <span data-ttu-id="e1e7e-126">Umkehren Sie die Bits im Schablone-Puffer Eintrag.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="e1e7e-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="e1e7e-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="e1e7e-128">0x00000040l</span><span class="sxs-lookup"><span data-stu-id="e1e7e-128">0x00000040L</span></span> | <span data-ttu-id="e1e7e-129">Erhöhen Sie den Schablonen Puffer Eintrag, wobei der Wert auf 0 (null) umwickelt wird, wenn der neue Wert den maximalen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="e1e7e-130">D3DSTENCILCAPS- \_ decr</span><span class="sxs-lookup"><span data-stu-id="e1e7e-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="e1e7e-131">0x00000080l</span><span class="sxs-lookup"><span data-stu-id="e1e7e-131">0x00000080L</span></span> | <span data-ttu-id="e1e7e-132">Verringert den Schablonen Puffer Eintrag und umwickelt ihn in den maximalen Wert, wenn der neue Wert kleiner als 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="e1e7e-133">D3DSTENCILCAPS \_ twoseitigem</span><span class="sxs-lookup"><span data-stu-id="e1e7e-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="e1e7e-134">0x00000100l</span><span class="sxs-lookup"><span data-stu-id="e1e7e-134">0x00000100L</span></span> | <span data-ttu-id="e1e7e-135">Das Gerät unterstützt zweiseitige Schablonen.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="e1e7e-136">Schablone-Puffer Einträge sind ganzzahlige Werte im Bereich von 0 bis 2 ⁿ-1, wobei n die Bittiefe des Schablonen Puffers ist.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="e1e7e-137">Diese Konstanten werden vom Schablone-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)verwendet.</span><span class="sxs-lookup"><span data-stu-id="e1e7e-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="e1e7e-138">Konstante Informationen</span><span class="sxs-lookup"><span data-stu-id="e1e7e-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e1e7e-139">Header</span><span class="sxs-lookup"><span data-stu-id="e1e7e-139">Header</span></span>                   | <span data-ttu-id="e1e7e-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="e1e7e-140">d3d9caps.h</span></span> |
| <span data-ttu-id="e1e7e-141">Mindestens Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="e1e7e-141">Minimum operating system</span></span> | <span data-ttu-id="e1e7e-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e1e7e-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e1e7e-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1e7e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1e7e-144">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e1e7e-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



