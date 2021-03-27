---
title: DEFB-PS
description: Definiert einen booleschen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729176"
---
# <a name="defb---ps"></a><span data-ttu-id="e0bad-103">DEFB-PS</span><span class="sxs-lookup"><span data-stu-id="e0bad-103">defb - ps</span></span>

<span data-ttu-id="e0bad-104">Definiert einen booleschen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0bad-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0bad-105">Syntax</span></span>



| <span data-ttu-id="e0bad-106">DEFB dest, BooleanValue</span><span class="sxs-lookup"><span data-stu-id="e0bad-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="e0bad-107">where</span><span class="sxs-lookup"><span data-stu-id="e0bad-107">where</span></span>

-   <span data-ttu-id="e0bad-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="e0bad-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e0bad-109">BooleanValue ist ein einzelner boolescher Wert, entweder true oder false.</span><span class="sxs-lookup"><span data-stu-id="e0bad-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0bad-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0bad-110">Remarks</span></span>



| <span data-ttu-id="e0bad-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="e0bad-111">Pixel shader versions</span></span> | <span data-ttu-id="e0bad-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e0bad-112">1\_1</span></span> | <span data-ttu-id="e0bad-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="e0bad-113">1\_2</span></span> | <span data-ttu-id="e0bad-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="e0bad-114">1\_3</span></span> | <span data-ttu-id="e0bad-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="e0bad-115">1\_4</span></span> | <span data-ttu-id="e0bad-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0bad-116">2\_0</span></span> | <span data-ttu-id="e0bad-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e0bad-117">2\_x</span></span> | <span data-ttu-id="e0bad-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e0bad-118">2\_sw</span></span> | <span data-ttu-id="e0bad-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e0bad-119">3\_0</span></span> | <span data-ttu-id="e0bad-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e0bad-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="e0bad-121">DEFB</span><span class="sxs-lookup"><span data-stu-id="e0bad-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="e0bad-122">x</span><span class="sxs-lookup"><span data-stu-id="e0bad-122">x</span></span>    | <span data-ttu-id="e0bad-123">x</span><span class="sxs-lookup"><span data-stu-id="e0bad-123">x</span></span>     | <span data-ttu-id="e0bad-124">x</span><span class="sxs-lookup"><span data-stu-id="e0bad-124">x</span></span>    | <span data-ttu-id="e0bad-125">x</span><span class="sxs-lookup"><span data-stu-id="e0bad-125">x</span></span>     |



 

<span data-ttu-id="e0bad-126">Die DEFB-Anweisung definiert eine boolesche Shader-Konstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e0bad-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="e0bad-127">Diese werden als unmittelbare Konstanten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e0bad-127">These are called immediate constants.</span></span> <span data-ttu-id="e0bad-128">Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setpixelshaderconstantb festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e0bad-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="e0bad-129">Es gibt zwei Möglichkeiten, eine BooleanConstant in einem Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e0bad-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="e0bad-130">Verwenden Sie DEFB, um die Konstante direkt in einem Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e0bad-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="e0bad-131">Verwenden Sie die API-Methoden, um eine Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e0bad-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="e0bad-132">Verwenden Sie [**setpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) , um eine boolesche Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e0bad-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0bad-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0bad-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0bad-134">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="e0bad-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="e0bad-135">DEF-PS</span><span class="sxs-lookup"><span data-stu-id="e0bad-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="e0bad-136">Defi-PS</span><span class="sxs-lookup"><span data-stu-id="e0bad-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 