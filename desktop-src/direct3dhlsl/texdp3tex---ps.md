---
title: texdp3tex-PS
description: Führt ein 3-Komponenten-Punktprodukt aus und verwendet das Ergebnis, um eine 1D-Textur Suche durchzuführen.
ms.assetid: vs|directx_sdk|~\texdp3tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dfe74dd0a73bc47cd2855d35b239e80a1b5153c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104992975"
---
# <a name="texdp3tex---ps"></a><span data-ttu-id="bc1c0-103">texdp3tex-PS</span><span class="sxs-lookup"><span data-stu-id="bc1c0-103">texdp3tex - ps</span></span>

<span data-ttu-id="bc1c0-104">Führt ein 3-Komponenten-Punktprodukt aus und verwendet das Ergebnis, um eine 1D-Textur Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-104">Performs a three-component dot product and uses the result to do a 1D texture lookup.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc1c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc1c0-105">Syntax</span></span>



| <span data-ttu-id="bc1c0-106">texdp3tex DST, src</span><span class="sxs-lookup"><span data-stu-id="bc1c0-106">texdp3tex dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="bc1c0-107">where</span><span class="sxs-lookup"><span data-stu-id="bc1c0-107">where</span></span>

-   <span data-ttu-id="bc1c0-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-108">dst is the destination register.</span></span>
-   <span data-ttu-id="bc1c0-109">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc1c0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc1c0-110">Remarks</span></span>



| <span data-ttu-id="bc1c0-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="bc1c0-111">Pixel shader versions</span></span> | <span data-ttu-id="bc1c0-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="bc1c0-112">1\_1</span></span> | <span data-ttu-id="bc1c0-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="bc1c0-113">1\_2</span></span> | <span data-ttu-id="bc1c0-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="bc1c0-114">1\_3</span></span> | <span data-ttu-id="bc1c0-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="bc1c0-115">1\_4</span></span> | <span data-ttu-id="bc1c0-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc1c0-116">2\_0</span></span> | <span data-ttu-id="bc1c0-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bc1c0-117">2\_x</span></span> | <span data-ttu-id="bc1c0-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bc1c0-118">2\_sw</span></span> | <span data-ttu-id="bc1c0-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bc1c0-119">3\_0</span></span> | <span data-ttu-id="bc1c0-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bc1c0-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="bc1c0-121">texdp3tex</span><span class="sxs-lookup"><span data-stu-id="bc1c0-121">texdp3tex</span></span>             |      | <span data-ttu-id="bc1c0-122">x</span><span class="sxs-lookup"><span data-stu-id="bc1c0-122">x</span></span>    | <span data-ttu-id="bc1c0-123">x</span><span class="sxs-lookup"><span data-stu-id="bc1c0-123">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="bc1c0-124">Textur Register müssen die folgende Sequenz verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-124">Texture registers must use the following sequence.</span></span>


```
 
tex       t(n)        // Define tn as a standard 3-vector (tn must be 
                      // defined in some way before texdp3tex uses it)
texdp3tex t(m), t(n)  // where m > n                 
                      // Perform a three-component dot product between t(n) and 
                      // the texture coordinate set m. Use the scalar result to
                      // do a 1D texture lookup at texturestage m and place
                      // the result in t(m)
```



<span data-ttu-id="bc1c0-125">Hier finden Sie weitere Details dazu, wie das Punktprodukt und die Textur Suche durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-125">Here is more detail about how the dot product and texture lookup are done.</span></span>

<span data-ttu-id="bc1c0-126">Die texdp3tex-Anweisung führt ein 3-Komponenten-Punktprodukt aus.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-126">The texdp3tex instruction performs a three-component dot product.</span></span>

<span data-ttu-id="bc1c0-127">u ' = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub></span><span class="sxs-lookup"><span data-stu-id="bc1c0-127">u' = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub></span></span>

<span data-ttu-id="bc1c0-128">Das Ergebnis wird verwendet, um eine Stichprobe der Textur in Textur Phase m Durchführen einer 1D-Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="bc1c0-128">The result is used to sample the texture at texture stage m by performing a 1D lookup.</span></span>

<span data-ttu-id="bc1c0-129">t (m)<sub>RGBA</sub> = texturesample (Phase m)<sub>RGBA</sub> mit (u ', 0, 0) als Koordinaten</span><span class="sxs-lookup"><span data-stu-id="bc1c0-129">t(m)<sub>RGBA</sub> = TextureSample(stage m)<sub>RGBA</sub> using (u',0,0) as coordinates</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc1c0-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc1c0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc1c0-131">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="bc1c0-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




