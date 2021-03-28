---
title: DSX-PS
description: Berechnen Sie die Änderungs Rate in der x-Richtung des Renderziels.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948327"
---
# <a name="dsx---ps"></a><span data-ttu-id="04eca-103">DSX-PS</span><span class="sxs-lookup"><span data-stu-id="04eca-103">dsx - ps</span></span>

<span data-ttu-id="04eca-104">Berechnen Sie die Änderungs Rate in der x-Richtung des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="04eca-104">Compute the rate of change in the render target's x-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="04eca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04eca-105">Syntax</span></span>



| <span data-ttu-id="04eca-106">DSX DST, src</span><span class="sxs-lookup"><span data-stu-id="04eca-106">dsx dst, src</span></span> |
|--------------|



 

<span data-ttu-id="04eca-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="04eca-107">Where:</span></span>

-   <span data-ttu-id="04eca-108">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="04eca-108">dst is a destination register.</span></span>
-   <span data-ttu-id="04eca-109">src ist ein Eingabe Quellen Register.</span><span class="sxs-lookup"><span data-stu-id="04eca-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="04eca-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04eca-110">Remarks</span></span>



| <span data-ttu-id="04eca-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="04eca-111">Pixel shader versions</span></span> | <span data-ttu-id="04eca-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="04eca-112">1\_1</span></span> | <span data-ttu-id="04eca-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="04eca-113">1\_2</span></span> | <span data-ttu-id="04eca-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="04eca-114">1\_3</span></span> | <span data-ttu-id="04eca-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="04eca-115">1\_4</span></span> | <span data-ttu-id="04eca-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04eca-116">2\_0</span></span> | <span data-ttu-id="04eca-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="04eca-117">2\_x</span></span> | <span data-ttu-id="04eca-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="04eca-118">2\_sw</span></span> | <span data-ttu-id="04eca-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="04eca-119">3\_0</span></span> | <span data-ttu-id="04eca-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="04eca-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="04eca-121">DSX</span><span class="sxs-lookup"><span data-stu-id="04eca-121">dsx</span></span>                   |      |      |      |      |      | <span data-ttu-id="04eca-122">x</span><span class="sxs-lookup"><span data-stu-id="04eca-122">x</span></span>    | <span data-ttu-id="04eca-123">x</span><span class="sxs-lookup"><span data-stu-id="04eca-123">x</span></span>     | <span data-ttu-id="04eca-124">x</span><span class="sxs-lookup"><span data-stu-id="04eca-124">x</span></span>    | <span data-ttu-id="04eca-125">x</span><span class="sxs-lookup"><span data-stu-id="04eca-125">x</span></span>     |



 

<span data-ttu-id="04eca-126">Die vom Quell Register berechnete Änderungs Rate ist ein Näherungswert für den Inhalt des gleichen Registers in angrenzenden Pixeln, auf denen der Pixelshader in einem Sperr Schritt mit dem aktuellen Pixel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04eca-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="04eca-127">Die Anweisungen DSX und [DSY](dsy---ps.md) berechnen das Ergebnis, indem Sie sich den aktuellen Inhalt des Quell Registers (pro Komponente) für die verschiedenen Pixel im lokalen Bereich ansehen, der im Sperr Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04eca-127">The dsx And [dsy](dsy---ps.md) instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="04eca-128">Die exakte Formel für die Berechnung des Farbverlaufs variiert abhängig von der Hardware, sollte jedoch mit der Art und Weise konsistent sein, wie die Hardware die gleichen Vorgänge im Rahmen der Detail Berechnung durchführt, um die Textur Stichproben zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="04eca-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04eca-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04eca-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04eca-130">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="04eca-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="04eca-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="04eca-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




