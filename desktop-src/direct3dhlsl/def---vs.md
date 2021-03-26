---
title: DEF-vs
description: Definiert Scheitelpunkt-Shader-Konstanten.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209344"
---
# <a name="def---vs"></a><span data-ttu-id="4e8e3-103">DEF-vs</span><span class="sxs-lookup"><span data-stu-id="4e8e3-103">def - vs</span></span>

<span data-ttu-id="4e8e3-104">Definiert Scheitelpunkt-Shader-Konstanten.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e8e3-105">Syntax</span></span>



| <span data-ttu-id="4e8e3-106">DEF DST, float1, float2, float3, float4</span><span class="sxs-lookup"><span data-stu-id="4e8e3-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="4e8e3-107">where</span><span class="sxs-lookup"><span data-stu-id="4e8e3-107">where</span></span>

-   <span data-ttu-id="4e8e3-108">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-108">dst is the destination register.</span></span>
-   <span data-ttu-id="4e8e3-109">float1, float2, float3, float4 sind vier Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e8e3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e8e3-110">Remarks</span></span>



| <span data-ttu-id="4e8e3-111">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="4e8e3-111">Vertex shader versions</span></span> | <span data-ttu-id="4e8e3-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="4e8e3-112">1\_1</span></span> | <span data-ttu-id="4e8e3-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e8e3-113">2\_0</span></span> | <span data-ttu-id="4e8e3-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-114">2\_x</span></span> | <span data-ttu-id="4e8e3-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4e8e3-115">2\_sw</span></span> | <span data-ttu-id="4e8e3-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4e8e3-116">3\_0</span></span> | <span data-ttu-id="4e8e3-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4e8e3-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4e8e3-118">def</span><span class="sxs-lookup"><span data-stu-id="4e8e3-118">def</span></span>                    | <span data-ttu-id="4e8e3-119">x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-119">x</span></span>    | <span data-ttu-id="4e8e3-120">x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-120">x</span></span>    | <span data-ttu-id="4e8e3-121">x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-121">x</span></span>    | <span data-ttu-id="4e8e3-122">x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-122">x</span></span>     | <span data-ttu-id="4e8e3-123">x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-123">x</span></span>    | <span data-ttu-id="4e8e3-124">x</span><span class="sxs-lookup"><span data-stu-id="4e8e3-124">x</span></span>     |



 

<span data-ttu-id="4e8e3-125">Die DEF-Anweisung definiert eine shaderkonstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="4e8e3-126">Diese werden als unmittelbare Konstanten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-126">These are called immediate constants.</span></span> <span data-ttu-id="4e8e3-127">Unmittelbare Konstanten haben Vorrang vor Konstanten, die von den API-Methoden setvertexshaderconstantf festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="4e8e3-128">Es gibt zwei Möglichkeiten, eine Konstante in einem Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="4e8e3-129">Verwenden Sie DEF-vs, um die Konstante direkt in einem Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="4e8e3-130">DEF-vs können nur Gleit Komma Konstanten definieren.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="4e8e3-131">Verwenden Sie die API-Methoden, um eine Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="4e8e3-132">Verwenden Sie [**setvertexshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) , um eine Gleit Komma Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4e8e3-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e8e3-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e8e3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e8e3-134">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="4e8e3-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="4e8e3-135">Defi-vs</span><span class="sxs-lookup"><span data-stu-id="4e8e3-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="4e8e3-136">DEFB-vs</span><span class="sxs-lookup"><span data-stu-id="4e8e3-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 