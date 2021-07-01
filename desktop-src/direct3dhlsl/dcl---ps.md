---
title: dcl - (sm2, sm3 - ps asm)
description: Deklarieren Sie ein Pixel-Shader-Eingaberegister.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130099"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="d611a-103">dcl - (sm2, sm3 - ps asm)</span><span class="sxs-lookup"><span data-stu-id="d611a-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="d611a-104">Deklarieren Sie ein Pixel-Shader-Eingaberegister.</span><span class="sxs-lookup"><span data-stu-id="d611a-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="d611a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d611a-105">Syntax</span></span>

<span data-ttu-id="d611a-106">dcl \[ \_ pp \] dest \[ .mask\]</span><span class="sxs-lookup"><span data-stu-id="d611a-106">dcl\[\_pp\] dest\[.mask\]</span></span>



 

<span data-ttu-id="d611a-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="d611a-107">Where:</span></span>

-   <span data-ttu-id="d611a-108">\[\_pp \] ist eine optionale partielle Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="d611a-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="d611a-109">Weitere Informationen finden Sie unter [Partielle Genauigkeit.](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)</span><span class="sxs-lookup"><span data-stu-id="d611a-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="d611a-110">dest ist ein Zielregister.</span><span class="sxs-lookup"><span data-stu-id="d611a-110">dest is a destination register.</span></span> <span data-ttu-id="d611a-111">Dabei muss es sich entweder um ein [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) oder um ein [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) handelt.</span><span class="sxs-lookup"><span data-stu-id="d611a-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="d611a-112">\[.mask \] ist eine optionale Schreibmaske, die steuert, in welche Komponenten des Zielregisters geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d611a-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="d611a-113">Weitere Informationen finden Sie unter [Zielregister-Schreibmaske.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)</span><span class="sxs-lookup"><span data-stu-id="d611a-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d611a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d611a-114">Remarks</span></span>



| <span data-ttu-id="d611a-115">Pixelshaderversionen</span><span class="sxs-lookup"><span data-stu-id="d611a-115">Pixel shader versions</span></span> | <span data-ttu-id="d611a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="d611a-116">1\_1</span></span> | <span data-ttu-id="d611a-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="d611a-117">1\_2</span></span> | <span data-ttu-id="d611a-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="d611a-118">1\_3</span></span> | <span data-ttu-id="d611a-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="d611a-119">1\_4</span></span> | <span data-ttu-id="d611a-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d611a-120">2\_0</span></span> | <span data-ttu-id="d611a-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d611a-121">2\_x</span></span> | <span data-ttu-id="d611a-122">2 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d611a-122">2\_sw</span></span> | <span data-ttu-id="d611a-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d611a-123">3\_0</span></span> | <span data-ttu-id="d611a-124">3 \_ sw</span><span class="sxs-lookup"><span data-stu-id="d611a-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="d611a-125">Dcl</span><span class="sxs-lookup"><span data-stu-id="d611a-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="d611a-126">x</span><span class="sxs-lookup"><span data-stu-id="d611a-126">x</span></span>    | <span data-ttu-id="d611a-127">x</span><span class="sxs-lookup"><span data-stu-id="d611a-127">x</span></span>    | <span data-ttu-id="d611a-128">x</span><span class="sxs-lookup"><span data-stu-id="d611a-128">x</span></span>     | <span data-ttu-id="d611a-129">x</span><span class="sxs-lookup"><span data-stu-id="d611a-129">x</span></span>    | <span data-ttu-id="d611a-130">x</span><span class="sxs-lookup"><span data-stu-id="d611a-130">x</span></span>     |



 

<span data-ttu-id="d611a-131">Alle dcl-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d611a-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d611a-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d611a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d611a-133">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="d611a-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




