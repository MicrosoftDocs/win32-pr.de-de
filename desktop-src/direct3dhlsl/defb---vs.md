---
title: DEFB-vs
description: Definiert einen booleschen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948766"
---
# <a name="defb---vs"></a><span data-ttu-id="ec48e-103">DEFB-vs</span><span class="sxs-lookup"><span data-stu-id="ec48e-103">defb - vs</span></span>

<span data-ttu-id="ec48e-104">Definiert einen booleschen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec48e-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec48e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec48e-105">Syntax</span></span>



| <span data-ttu-id="ec48e-106">DEFB dest, BooleanValue</span><span class="sxs-lookup"><span data-stu-id="ec48e-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="ec48e-107">where</span><span class="sxs-lookup"><span data-stu-id="ec48e-107">where</span></span>

-   <span data-ttu-id="ec48e-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="ec48e-108">dst is the destination register.</span></span>
-   <span data-ttu-id="ec48e-109">BooleanValue ist ein boolescher Wert, entweder true oder false.</span><span class="sxs-lookup"><span data-stu-id="ec48e-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec48e-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec48e-110">Remarks</span></span>



| <span data-ttu-id="ec48e-111">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="ec48e-111">Vertex shader versions</span></span> | <span data-ttu-id="ec48e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="ec48e-112">1\_1</span></span> | <span data-ttu-id="ec48e-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec48e-113">2\_0</span></span> | <span data-ttu-id="ec48e-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ec48e-114">2\_x</span></span> | <span data-ttu-id="ec48e-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ec48e-115">2\_sw</span></span> | <span data-ttu-id="ec48e-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ec48e-116">3\_0</span></span> | <span data-ttu-id="ec48e-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ec48e-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ec48e-118">DEFB</span><span class="sxs-lookup"><span data-stu-id="ec48e-118">defb</span></span>                   |      | <span data-ttu-id="ec48e-119">x</span><span class="sxs-lookup"><span data-stu-id="ec48e-119">x</span></span>    | <span data-ttu-id="ec48e-120">x</span><span class="sxs-lookup"><span data-stu-id="ec48e-120">x</span></span>    | <span data-ttu-id="ec48e-121">x</span><span class="sxs-lookup"><span data-stu-id="ec48e-121">x</span></span>     | <span data-ttu-id="ec48e-122">x</span><span class="sxs-lookup"><span data-stu-id="ec48e-122">x</span></span>    | <span data-ttu-id="ec48e-123">x</span><span class="sxs-lookup"><span data-stu-id="ec48e-123">x</span></span>     |



 

<span data-ttu-id="ec48e-124">Die DEFB-vs-Anweisung definiert eine boolesche Shader-Konstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ec48e-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="ec48e-125">Diese werden als unmittelbare Konstanten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ec48e-125">These are called immediate constants.</span></span> <span data-ttu-id="ec48e-126">Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setvertexshaderconstantb festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ec48e-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="ec48e-127">Es gibt zwei Möglichkeiten, eine boolesche Konstante in einem Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ec48e-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="ec48e-128">Verwenden Sie DEFB-vs, um die Konstante direkt in einem Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ec48e-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="ec48e-129">Verwenden Sie die API-Methoden, um eine Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ec48e-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="ec48e-130">Verwenden Sie [**setvertexshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) , um eine boolesche Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ec48e-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec48e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ec48e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec48e-132">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="ec48e-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="ec48e-133">DEF-vs</span><span class="sxs-lookup"><span data-stu-id="ec48e-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="ec48e-134">Defi-vs</span><span class="sxs-lookup"><span data-stu-id="ec48e-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 