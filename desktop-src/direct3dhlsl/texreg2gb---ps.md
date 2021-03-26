---
title: texreg2gb-PS
description: Interpretiert die grünen und blauen Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht.
ms.assetid: 81d3fb3e-ef53-4d25-b65d-c4c9fea0c74c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d6c428ee5a532919916f0a714db7f81a1c75c12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976689"
---
# <a name="texreg2gb---ps"></a><span data-ttu-id="58070-103">texreg2gb-PS</span><span class="sxs-lookup"><span data-stu-id="58070-103">texreg2gb - ps</span></span>

<span data-ttu-id="58070-104">Interpretiert die grünen und blauen Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="58070-104">Interprets the green and blue color components of the source register as texture address data to sample the texture at the stage corresponding to the destination register number.</span></span>

## <a name="syntax"></a><span data-ttu-id="58070-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="58070-105">Syntax</span></span>



| <span data-ttu-id="58070-106">texreg2gb DST, src</span><span class="sxs-lookup"><span data-stu-id="58070-106">texreg2gb dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="58070-107">where</span><span class="sxs-lookup"><span data-stu-id="58070-107">where</span></span>

-   <span data-ttu-id="58070-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="58070-108">dst is the destination register.</span></span>
-   <span data-ttu-id="58070-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="58070-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="58070-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="58070-110">Remarks</span></span>



| <span data-ttu-id="58070-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="58070-111">Pixel shader versions</span></span> | <span data-ttu-id="58070-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="58070-112">1\_1</span></span> | <span data-ttu-id="58070-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="58070-113">1\_2</span></span> | <span data-ttu-id="58070-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="58070-114">1\_3</span></span> | <span data-ttu-id="58070-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="58070-115">1\_4</span></span> | <span data-ttu-id="58070-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58070-116">2\_0</span></span> | <span data-ttu-id="58070-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="58070-117">2\_x</span></span> | <span data-ttu-id="58070-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="58070-118">2\_sw</span></span> | <span data-ttu-id="58070-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="58070-119">3\_0</span></span> | <span data-ttu-id="58070-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="58070-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="58070-121">texreg2gb</span><span class="sxs-lookup"><span data-stu-id="58070-121">texreg2gb</span></span>             |      | <span data-ttu-id="58070-122">x</span><span class="sxs-lookup"><span data-stu-id="58070-122">x</span></span>    | <span data-ttu-id="58070-123">x</span><span class="sxs-lookup"><span data-stu-id="58070-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="58070-124">Diese Anweisung ist für die Neuzuordnung von Farbräumen nützlich.</span><span class="sxs-lookup"><span data-stu-id="58070-124">This instruction is useful for color-space remapping operations.</span></span>

<span data-ttu-id="58070-125">Im folgenden finden Sie ein Beispiel für die Sequenz, auf die die Anweisung folgt.</span><span class="sxs-lookup"><span data-stu-id="58070-125">Here is an example of the sequence the instruction follows.</span></span>

<dl> <span data-ttu-id="58070-126">tex t (n)</span><span class="sxs-lookup"><span data-stu-id="58070-126">tex t(n)</span></span>  
<span data-ttu-id="58070-127">texreg2gb t (m), t (n), wobei m > n</span><span class="sxs-lookup"><span data-stu-id="58070-127">texreg2gb t(m), t(n) where m > n</span></span>  
<span data-ttu-id="58070-128">Die erste Anweisung lädt die Textur Farbe (RGBA).</span><span class="sxs-lookup"><span data-stu-id="58070-128">// The first instruction loads the texture color (RGBA)</span></span>  
<span data-ttu-id="58070-129">in Register TN</span><span class="sxs-lookup"><span data-stu-id="58070-129">// into register tn</span></span>  
<span data-ttu-id="58070-130">tex TN</span><span class="sxs-lookup"><span data-stu-id="58070-130">tex tn</span></span>  
<span data-ttu-id="58070-131">Mit der zweiten Anweisung wird die Farbe neu zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="58070-131">// The second instruction remaps the color</span></span>  
<span data-ttu-id="58070-132">t (m)<sub>RGBA</sub> = texturesample (Stufe m)<sub>RGBA</sub> mit t (n)<sub>GB</sub> als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="58070-132">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>GB</sub> as coordinates</span></span>
</dl>

<span data-ttu-id="58070-133">\_bx2 kann nicht für das src-Register für [texreg2ar-PS-](texreg2ar---ps.md) oder texreg2gb-Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58070-133">\_bx2 cannot be used on the src register for [texreg2ar - ps](texreg2ar---ps.md) or texreg2gb instructions.</span></span>

<span data-ttu-id="58070-134">Für diese Anweisung muss das Quell Register nicht signierte Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="58070-134">For this instruction, the source register must use unsigned data.</span></span> <span data-ttu-id="58070-135">Die Verwendung von signierten oder gemischten Daten im Quell Register führt zu undefinierten Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="58070-135">Use of signed or mixed data in the source register will produce undefined results.</span></span> <span data-ttu-id="58070-136">Weitere Informationen finden Sie unter [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span><span class="sxs-lookup"><span data-stu-id="58070-136">For more information, see [D3DFORMAT](/windows/desktop/direct3d9/d3dformat).</span></span>

## <a name="related-topics"></a><span data-ttu-id="58070-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58070-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58070-138">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="58070-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 