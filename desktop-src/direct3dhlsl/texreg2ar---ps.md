---
title: texreg2ar-PS
description: Interpretiert die Alpha-und roten Farbkomponenten des Quell Registers als Textur Adressdaten (u, v), um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht. Das Ergebnis wird im Ziel Register gespeichert.
ms.assetid: b31a2ee4-f9b9-4aee-b3be-7ccc5b8c6f3e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93418e7e9e87178cd64c2d7238b5227de0990378
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473453"
---
# <a name="texreg2ar---ps"></a><span data-ttu-id="b95df-104">texreg2ar-PS</span><span class="sxs-lookup"><span data-stu-id="b95df-104">texreg2ar - ps</span></span>

<span data-ttu-id="b95df-105">Interpretiert die Alpha-und roten Farbkomponenten des Quell Registers als Textur Adressdaten (u, v), um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="b95df-105">Interprets the alpha and red color components of the source register as texture address data (u,v) to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="b95df-106">Das Ergebnis wird im Ziel Register gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b95df-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="b95df-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b95df-107">Syntax</span></span>



| <span data-ttu-id="b95df-108">texreg2ar DST, src</span><span class="sxs-lookup"><span data-stu-id="b95df-108">texreg2ar dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="b95df-109">where</span><span class="sxs-lookup"><span data-stu-id="b95df-109">where</span></span>

-   <span data-ttu-id="b95df-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="b95df-110">dst is the destination register.</span></span>
-   <span data-ttu-id="b95df-111">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="b95df-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b95df-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b95df-112">Remarks</span></span>



| <span data-ttu-id="b95df-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b95df-113">Pixel shader versions</span></span> | <span data-ttu-id="b95df-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b95df-114">1\_1</span></span> | <span data-ttu-id="b95df-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b95df-115">1\_2</span></span> | <span data-ttu-id="b95df-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b95df-116">1\_3</span></span> | <span data-ttu-id="b95df-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b95df-117">1\_4</span></span> | <span data-ttu-id="b95df-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b95df-118">2\_0</span></span> | <span data-ttu-id="b95df-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b95df-119">2\_x</span></span> | <span data-ttu-id="b95df-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b95df-120">2\_sw</span></span> | <span data-ttu-id="b95df-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b95df-121">3\_0</span></span> | <span data-ttu-id="b95df-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b95df-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b95df-123">texreg2ar</span><span class="sxs-lookup"><span data-stu-id="b95df-123">texreg2ar</span></span>             | <span data-ttu-id="b95df-124">x</span><span class="sxs-lookup"><span data-stu-id="b95df-124">x</span></span>    | <span data-ttu-id="b95df-125">x</span><span class="sxs-lookup"><span data-stu-id="b95df-125">x</span></span>    | <span data-ttu-id="b95df-126">x</span><span class="sxs-lookup"><span data-stu-id="b95df-126">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="b95df-127">Diese Anweisung ist für die Neuzuordnung von Farbräumen nützlich.</span><span class="sxs-lookup"><span data-stu-id="b95df-127">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="b95df-128">Im folgenden finden Sie ein Beispiel für die Reihenfolge der Anweisung:</span><span class="sxs-lookup"><span data-stu-id="b95df-128">Here is an example of the sequence the instruction follows:</span></span>

<dl> <span data-ttu-id="b95df-129">tex t (n)</span><span class="sxs-lookup"><span data-stu-id="b95df-129">tex t(n)</span></span>  
<span data-ttu-id="b95df-130">texreg2ar t (m), t (n), wobei m > n</span><span class="sxs-lookup"><span data-stu-id="b95df-130">texreg2ar t(m), t(n) where m > n</span></span>  
<span data-ttu-id="b95df-131">Die erste Anweisung lädt die Textur Farbe (RGBA).</span><span class="sxs-lookup"><span data-stu-id="b95df-131">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="b95df-132">in Register TN</span><span class="sxs-lookup"><span data-stu-id="b95df-132">// into register tn</span></span>  
<span data-ttu-id="b95df-133">tex TN</span><span class="sxs-lookup"><span data-stu-id="b95df-133">tex tn</span></span>  
<span data-ttu-id="b95df-134">Mit der zweiten Anweisung wird die Farbe neu zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="b95df-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="b95df-135">t (m)<sub>RGBA</sub> = texturesample (Phase m)<sub>RGBA</sub> mit t (n)<sub>AR</sub> als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="b95df-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>AR</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="b95df-136">\_bx2 kann nicht für das src-Register für texreg2ar [-oder texreg2gb-PS-](texreg2gb---ps.md) Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b95df-136">\_bx2 cannot be used on the src register for texreg2ar or [texreg2gb - ps](texreg2gb---ps.md) instructions.</span></span>

<span data-ttu-id="b95df-137">Für diese Anweisung muss das Quell Register nicht signierte Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="b95df-137">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="b95df-138">Die Verwendung von signierten oder gemischten Daten im Quell Register führt zu undefinierten Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="b95df-138">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="b95df-139">Weitere Informationen finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="b95df-139">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b95df-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b95df-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b95df-141">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b95df-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 