---
title: DEF-PS
description: Definiert Pixel-Shader-Gleit Komma Konstanten.
ms.assetid: 679b3074-73f3-48de-8c7a-f43bff76b25a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b4f035df97de2645983862dd68aa7ec80fc22d4b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039548"
---
# <a name="def---ps"></a><span data-ttu-id="fcb3b-103">DEF-PS</span><span class="sxs-lookup"><span data-stu-id="fcb3b-103">def - ps</span></span>

<span data-ttu-id="fcb3b-104">Definiert Pixel-Shader-Gleit Komma Konstanten.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-104">Defines pixel shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb3b-105">Syntax</span></span>



| <span data-ttu-id="fcb3b-106">DEF DST, fVvalue1, fValue2, fValue3, fValue4</span><span class="sxs-lookup"><span data-stu-id="fcb3b-106">def dst, fVvalue1, fValue2, fValue3, fValue4</span></span> |
|----------------------------------------------|



 

<span data-ttu-id="fcb3b-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="fcb3b-107">Where:</span></span>

-   <span data-ttu-id="fcb3b-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-108">dst is the destination register.</span></span>
-   <span data-ttu-id="fcb3b-109">fValue1 to fValue4 sind Gleit Komma Werte.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-109">fValue1 to fValue4 are floating-point values..</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb3b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcb3b-110">Remarks</span></span>



| <span data-ttu-id="fcb3b-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="fcb3b-111">Pixel shader versions</span></span> | <span data-ttu-id="fcb3b-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="fcb3b-112">1\_1</span></span> | <span data-ttu-id="fcb3b-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="fcb3b-113">1\_2</span></span> | <span data-ttu-id="fcb3b-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fcb3b-114">1\_3</span></span> | <span data-ttu-id="fcb3b-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="fcb3b-115">1\_4</span></span> | <span data-ttu-id="fcb3b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fcb3b-116">2\_0</span></span> | <span data-ttu-id="fcb3b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-117">2\_x</span></span> | <span data-ttu-id="fcb3b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fcb3b-118">2\_sw</span></span> | <span data-ttu-id="fcb3b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fcb3b-119">3\_0</span></span> | <span data-ttu-id="fcb3b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fcb3b-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fcb3b-121">def</span><span class="sxs-lookup"><span data-stu-id="fcb3b-121">def</span></span>                   | <span data-ttu-id="fcb3b-122">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-122">x</span></span>    | <span data-ttu-id="fcb3b-123">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-123">x</span></span>    | <span data-ttu-id="fcb3b-124">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-124">x</span></span>    | <span data-ttu-id="fcb3b-125">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-125">x</span></span>    | <span data-ttu-id="fcb3b-126">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-126">x</span></span>    | <span data-ttu-id="fcb3b-127">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-127">x</span></span>    | <span data-ttu-id="fcb3b-128">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-128">x</span></span>     | <span data-ttu-id="fcb3b-129">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-129">x</span></span>    | <span data-ttu-id="fcb3b-130">x</span><span class="sxs-lookup"><span data-stu-id="fcb3b-130">x</span></span>     |



 

<span data-ttu-id="fcb3b-131">Es gibt zwei Möglichkeiten, eine Gleit Komma Konstante in einem Pixelshader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-131">There are two ways to set a floating-point constant in a pixel shader.</span></span>

1.  <span data-ttu-id="fcb3b-132">Verwenden Sie def, um die Konstante direkt in einem Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-132">Use def to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="fcb3b-133">Verwenden Sie die-API, um eine Konstante mit [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-133">Use the API to set a constant with [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="fcb3b-134">DEF definiert eine shaderkonstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-134">def defines a shader constant whose value is loaded any time a shader is set to a device.</span></span> <span data-ttu-id="fcb3b-135">Diese werden als unmittelbare Konstanten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-135">These are called immediate constants.</span></span> <span data-ttu-id="fcb3b-136">Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-136">Immediate constants take precedence over constants set by the API method.</span></span>

-   <span data-ttu-id="fcb3b-137">Muss vor der ersten arithmetischen oder Adressierungs Anweisung im Shader angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-137">Must appear before the first arithmetic or addressing instruction in shader.</span></span>
-   <span data-ttu-id="fcb3b-138">Kann mit [DCL-(SM2, SM3-PS ASM)-](dcl---ps.md) Anweisungen gemischt werden (bei denen es sich um den anderen Typ der Anweisung handelt, die sich am Anfang eines Shaders befindet).</span><span class="sxs-lookup"><span data-stu-id="fcb3b-138">Can be intermixed with [dcl - (sm2, sm3 - ps asm)](dcl---ps.md) instructions (which are the other type of instruction that resides at the beginning of a shader).</span></span>
-   <span data-ttu-id="fcb3b-139">das DST-Register muss ein [konstantes Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)sein.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-139">dst register must be a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>
-   <span data-ttu-id="fcb3b-140">Die Schreib Maske muss voll (Standard) sein.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-140">Write mask must be full (default).</span></span>
-   <span data-ttu-id="fcb3b-141">Wenn ein [konstantes Register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) mehrmals in einem Shader definiert ist, wird das letzte beibehalten.</span><span class="sxs-lookup"><span data-stu-id="fcb3b-141">If a [constant register](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) is defined multiple times in a shader, the last one persists.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fcb3b-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fcb3b-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fcb3b-143">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="fcb3b-143">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 