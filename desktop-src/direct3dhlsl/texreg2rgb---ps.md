---
title: texreg2rgb-PS
description: Interpretiert die roten, grünen und blauen (RGB) Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht. Das Ergebnis wird im Ziel Register gespeichert.
ms.assetid: 8ec44014-d796-407c-8fe0-036decaf2a3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8bcd2bbd7e57ba9dc692f34404a5610cdc517f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516496"
---
# <a name="texreg2rgb---ps"></a><span data-ttu-id="0f7f9-104">texreg2rgb-PS</span><span class="sxs-lookup"><span data-stu-id="0f7f9-104">texreg2rgb - ps</span></span>

<span data-ttu-id="0f7f9-105">Interpretiert die roten, grünen und blauen (RGB) Farbkomponenten des Quell Registers als Textur Adressdaten, um die Textur in der Phase zu testen, die der Ziel Registernummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-105">Interprets the red, green, and blue (RGB) color components of the source register as texture address data in order to sample the texture at the stage corresponding to the destination register number.</span></span> <span data-ttu-id="0f7f9-106">Das Ergebnis wird im Ziel Register gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-106">The result is stored in the destination register.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f7f9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f7f9-107">Syntax</span></span>



| <span data-ttu-id="0f7f9-108">texreg2rgb DST, src</span><span class="sxs-lookup"><span data-stu-id="0f7f9-108">texreg2rgb dst, src</span></span> |
|---------------------|



 

<span data-ttu-id="0f7f9-109">where</span><span class="sxs-lookup"><span data-stu-id="0f7f9-109">where</span></span>

-   <span data-ttu-id="0f7f9-110">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-110">dst is the destination register.</span></span>
-   <span data-ttu-id="0f7f9-111">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-111">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f7f9-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f7f9-112">Remarks</span></span>



| <span data-ttu-id="0f7f9-113">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="0f7f9-113">Pixel shader versions</span></span> | <span data-ttu-id="0f7f9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0f7f9-114">1\_1</span></span> | <span data-ttu-id="0f7f9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0f7f9-115">1\_2</span></span> | <span data-ttu-id="0f7f9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0f7f9-116">1\_3</span></span> | <span data-ttu-id="0f7f9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0f7f9-117">1\_4</span></span> | <span data-ttu-id="0f7f9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f7f9-118">2\_0</span></span> | <span data-ttu-id="0f7f9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0f7f9-119">2\_x</span></span> | <span data-ttu-id="0f7f9-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0f7f9-120">2\_sw</span></span> | <span data-ttu-id="0f7f9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f7f9-121">3\_0</span></span> | <span data-ttu-id="0f7f9-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0f7f9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0f7f9-123">texreg2rgb</span><span class="sxs-lookup"><span data-stu-id="0f7f9-123">texreg2rgb</span></span>            |      | <span data-ttu-id="0f7f9-124">x</span><span class="sxs-lookup"><span data-stu-id="0f7f9-124">x</span></span>    | <span data-ttu-id="0f7f9-125">x</span><span class="sxs-lookup"><span data-stu-id="0f7f9-125">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="0f7f9-126">Diese Anweisung ist für die Neuzuordnung von Farbräumen nützlich.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-126">This instruction is useful for color-space remapping operations.</span></span> <span data-ttu-id="0f7f9-127">Es unterstützt zweidimensionale (2D) und dreidimensionale (3D) Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-127">It supports two-dimensional (2D) and three-dimensional (3D) coordinates.</span></span> <span data-ttu-id="0f7f9-128">Sie kann wie [texreg2ar-PS](texreg2ar---ps.md) oder [texreg2gb-PS](texreg2gb---ps.md) verwendet werden, um 2D-Daten neu zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-128">It can be used just like the [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md) to remap 2D data.</span></span> <span data-ttu-id="0f7f9-129">Diese Anweisung unterstützt jedoch auch 3D-Daten, sodass Sie mit Cubemaps und 3D-volumetexturen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-129">However, this instruction also supports 3D data so it can be used with cube maps and 3D volume textures.</span></span>

<span data-ttu-id="0f7f9-130">Im folgenden finden Sie ein Beispiel für die Sequenz, auf die die Anweisung folgt.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-130">Here is an example of the sequence the instruction follows.</span></span>


```
 
tex t(n)
texreg2rgb t(m), t(n)     where m > n
```



<span data-ttu-id="0f7f9-131">Im folgenden finden Sie weitere Details dazu, wie die Neuzuordnung erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-131">Here is more detail about how the remapping is accomplished.</span></span>

<dl> <span data-ttu-id="0f7f9-132">Die erste Anweisung lädt die Textur Farbe (RGBA) in das Register TN.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-132">// The first instruction loads the texture color (RGBA) into register tn</span></span>  
<span data-ttu-id="0f7f9-133">tex TN</span><span class="sxs-lookup"><span data-stu-id="0f7f9-133">tex tn</span></span>  
<span data-ttu-id="0f7f9-134">Mit der zweiten Anweisung wird die Farbe neu zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0f7f9-134">// The second instruction remaps the color</span></span>  
<span data-ttu-id="0f7f9-135">t (m)<sub>RGBA</sub> = texturesample (Phase m)<sub>RGBA</sub> mit t (n)<sub>RGB</sub> als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="0f7f9-135">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using t(n)<sub>RGB</sub> as coordinates</span></span>
</dl>

## <a name="related-topics"></a><span data-ttu-id="0f7f9-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f7f9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f7f9-137">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="0f7f9-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




