---
title: texm3x2pad-PS
description: Führt die erste Zeilen Multiplikation einer zweizeiligen Matrix Multiplikation aus. Diese Anweisung muss entweder mit texm3x2tex-PS oder texm3x2depth-PS kombiniert werden. Weitere Informationen zur Verwendung von texmpad finden Sie in den folgenden Anweisungen.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857787"
---
# <a name="texm3x2pad---ps"></a><span data-ttu-id="9c28b-105">texm3x2pad-PS</span><span class="sxs-lookup"><span data-stu-id="9c28b-105">texm3x2pad - ps</span></span>

<span data-ttu-id="9c28b-106">Führt die erste Zeilen Multiplikation einer zweizeiligen Matrix Multiplikation aus.</span><span class="sxs-lookup"><span data-stu-id="9c28b-106">Performs the first row multiplication of a two-row matrix multiply.</span></span> <span data-ttu-id="9c28b-107">Diese Anweisung muss entweder mit [texm3x2tex-PS](texm3x2tex---ps.md) oder [texm3x2depth-PS](texm3x2depth---ps.md)kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="9c28b-107">This instruction must be combined with either [texm3x2tex - ps](texm3x2tex---ps.md) or [texm3x2depth - ps](texm3x2depth---ps.md).</span></span> <span data-ttu-id="9c28b-108">Weitere Informationen zur Verwendung von texmpad finden Sie in den folgenden Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="9c28b-108">Refer to either of these instructions for details on using texmpad.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c28b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c28b-109">Syntax</span></span>



| <span data-ttu-id="9c28b-110">tex3x2pad DST, src</span><span class="sxs-lookup"><span data-stu-id="9c28b-110">tex3x2pad dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="9c28b-111">where</span><span class="sxs-lookup"><span data-stu-id="9c28b-111">where</span></span>

-   <span data-ttu-id="9c28b-112">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="9c28b-112">dst is the destination register.</span></span>
-   <span data-ttu-id="9c28b-113">src ist ein Quell Register.</span><span class="sxs-lookup"><span data-stu-id="9c28b-113">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c28b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c28b-114">Remarks</span></span>



| <span data-ttu-id="9c28b-115">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="9c28b-115">Pixel shader versions</span></span> | <span data-ttu-id="9c28b-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="9c28b-116">1\_1</span></span> | <span data-ttu-id="9c28b-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="9c28b-117">1\_2</span></span> | <span data-ttu-id="9c28b-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9c28b-118">1\_3</span></span> | <span data-ttu-id="9c28b-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="9c28b-119">1\_4</span></span> | <span data-ttu-id="9c28b-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c28b-120">2\_0</span></span> | <span data-ttu-id="9c28b-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9c28b-121">2\_x</span></span> | <span data-ttu-id="9c28b-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c28b-122">2\_sw</span></span> | <span data-ttu-id="9c28b-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9c28b-123">3\_0</span></span> | <span data-ttu-id="9c28b-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9c28b-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9c28b-125">texm3x2pad</span><span class="sxs-lookup"><span data-stu-id="9c28b-125">texm3x2pad</span></span>            | <span data-ttu-id="9c28b-126">x</span><span class="sxs-lookup"><span data-stu-id="9c28b-126">x</span></span>    | <span data-ttu-id="9c28b-127">x</span><span class="sxs-lookup"><span data-stu-id="9c28b-127">x</span></span>    | <span data-ttu-id="9c28b-128">x</span><span class="sxs-lookup"><span data-stu-id="9c28b-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="9c28b-129">Diese Anweisung kann nicht allein verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c28b-129">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c28b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c28b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c28b-131">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="9c28b-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




