---
title: DSY-PS
description: Berechnen Sie die Änderungs Rate in der y-Richtung des Renderziels.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389514"
---
# <a name="dsy---ps"></a><span data-ttu-id="15eea-103">DSY-PS</span><span class="sxs-lookup"><span data-stu-id="15eea-103">dsy - ps</span></span>

<span data-ttu-id="15eea-104">Berechnen Sie die Änderungs Rate in der y-Richtung des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="15eea-104">Compute the rate of change in the render target's y-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="15eea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="15eea-105">Syntax</span></span>



| <span data-ttu-id="15eea-106">DSY DST, src</span><span class="sxs-lookup"><span data-stu-id="15eea-106">dsy dst, src</span></span> |
|--------------|



 

<span data-ttu-id="15eea-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="15eea-107">Where:</span></span>

-   <span data-ttu-id="15eea-108">DST ist ein Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="15eea-108">dst is a destination register.</span></span>
-   <span data-ttu-id="15eea-109">src ist ein Eingabe Quellen Register.</span><span class="sxs-lookup"><span data-stu-id="15eea-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="15eea-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15eea-110">Remarks</span></span>



| <span data-ttu-id="15eea-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="15eea-111">Pixel shader versions</span></span> | <span data-ttu-id="15eea-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="15eea-112">1\_1</span></span> | <span data-ttu-id="15eea-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="15eea-113">1\_2</span></span> | <span data-ttu-id="15eea-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="15eea-114">1\_3</span></span> | <span data-ttu-id="15eea-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="15eea-115">1\_4</span></span> | <span data-ttu-id="15eea-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15eea-116">2\_0</span></span> | <span data-ttu-id="15eea-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="15eea-117">2\_x</span></span> | <span data-ttu-id="15eea-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="15eea-118">2\_sw</span></span> | <span data-ttu-id="15eea-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="15eea-119">3\_0</span></span> | <span data-ttu-id="15eea-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="15eea-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="15eea-121">DSY</span><span class="sxs-lookup"><span data-stu-id="15eea-121">dsy</span></span>                   |      |      |      |      |      | <span data-ttu-id="15eea-122">x</span><span class="sxs-lookup"><span data-stu-id="15eea-122">x</span></span>    | <span data-ttu-id="15eea-123">x</span><span class="sxs-lookup"><span data-stu-id="15eea-123">x</span></span>     | <span data-ttu-id="15eea-124">x</span><span class="sxs-lookup"><span data-stu-id="15eea-124">x</span></span>    | <span data-ttu-id="15eea-125">x</span><span class="sxs-lookup"><span data-stu-id="15eea-125">x</span></span>     |



 

<span data-ttu-id="15eea-126">Die vom Quell Register berechnete Änderungs Rate ist ein Näherungswert für den Inhalt des gleichen Registers in angrenzenden Pixeln, auf denen der Pixelshader in einem Sperr Schritt mit dem aktuellen Pixel ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15eea-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="15eea-127">Die Anweisungen [DSX](dsx---ps.md) und DSY berechnen das Ergebnis, indem Sie sich den aktuellen Inhalt des Quell Registers (pro Komponente) für die verschiedenen Pixel im lokalen Bereich ansehen, der im Sperr Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15eea-127">The [dsx](dsx---ps.md) And dsy instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="15eea-128">Die exakte Formel für die Berechnung des Farbverlaufs variiert abhängig von der Hardware, sollte jedoch mit der Art und Weise konsistent sein, wie die Hardware die gleichen Vorgänge im Rahmen der Detail Berechnung durchführt, um die Textur Stichproben zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="15eea-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15eea-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15eea-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15eea-130">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="15eea-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="15eea-131">texldd-PS</span><span class="sxs-lookup"><span data-stu-id="15eea-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




