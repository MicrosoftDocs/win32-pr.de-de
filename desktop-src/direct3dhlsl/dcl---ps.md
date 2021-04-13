---
title: DCL-(SM2, SM3-PS ASM)
description: Deklarieren Sie ein Pixel-Shader-Eingabe Register.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389566"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="b6ea0-103">DCL-(SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="b6ea0-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="b6ea0-104">Deklarieren Sie ein Pixel-Shader-Eingabe Register.</span><span class="sxs-lookup"><span data-stu-id="b6ea0-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ea0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6ea0-105">Syntax</span></span>



|                           |
|---------------------------|
| <span data-ttu-id="b6ea0-106">DCL- \[ \_ PP \] \[ : dest. Mask\]</span><span class="sxs-lookup"><span data-stu-id="b6ea0-106">dcl\[\_pp\] dest\[.mask\]</span></span> |



 

<span data-ttu-id="b6ea0-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="b6ea0-107">Where:</span></span>

-   <span data-ttu-id="b6ea0-108">\[\_PP \] ist eine optionale partielle Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="b6ea0-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="b6ea0-109">Siehe [partielle Genauigkeit](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="b6ea0-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="b6ea0-110">dest ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="b6ea0-110">dest is a destination register.</span></span> <span data-ttu-id="b6ea0-111">Dabei muss es sich entweder um ein [Eingabe Farbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) oder um ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) handeln.</span><span class="sxs-lookup"><span data-stu-id="b6ea0-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="b6ea0-112">\[. mask \] ist eine optionale Schreib Maske, mit der gesteuert wird, auf welche Komponenten des Ziel Registers geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b6ea0-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="b6ea0-113">Siehe [Ziel Registrierung schreiben Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="b6ea0-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6ea0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b6ea0-114">Remarks</span></span>



| <span data-ttu-id="b6ea0-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="b6ea0-115">Pixel shader versions</span></span> | <span data-ttu-id="b6ea0-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="b6ea0-116">1\_1</span></span> | <span data-ttu-id="b6ea0-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="b6ea0-117">1\_2</span></span> | <span data-ttu-id="b6ea0-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b6ea0-118">1\_3</span></span> | <span data-ttu-id="b6ea0-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="b6ea0-119">1\_4</span></span> | <span data-ttu-id="b6ea0-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6ea0-120">2\_0</span></span> | <span data-ttu-id="b6ea0-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b6ea0-121">2\_x</span></span> | <span data-ttu-id="b6ea0-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b6ea0-122">2\_sw</span></span> | <span data-ttu-id="b6ea0-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b6ea0-123">3\_0</span></span> | <span data-ttu-id="b6ea0-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b6ea0-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b6ea0-125">DCL</span><span class="sxs-lookup"><span data-stu-id="b6ea0-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="b6ea0-126">x</span><span class="sxs-lookup"><span data-stu-id="b6ea0-126">x</span></span>    | <span data-ttu-id="b6ea0-127">x</span><span class="sxs-lookup"><span data-stu-id="b6ea0-127">x</span></span>    | <span data-ttu-id="b6ea0-128">x</span><span class="sxs-lookup"><span data-stu-id="b6ea0-128">x</span></span>     | <span data-ttu-id="b6ea0-129">x</span><span class="sxs-lookup"><span data-stu-id="b6ea0-129">x</span></span>    | <span data-ttu-id="b6ea0-130">x</span><span class="sxs-lookup"><span data-stu-id="b6ea0-130">x</span></span>     |



 

<span data-ttu-id="b6ea0-131">Alle DCL-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b6ea0-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6ea0-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6ea0-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6ea0-133">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="b6ea0-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




