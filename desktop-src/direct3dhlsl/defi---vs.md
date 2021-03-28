---
title: Defi-vs
description: Definiert einen ganzzahligen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: d6067a7d-58fb-4553-a42f-192c29bf78b7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 897a544cc9974b8ffa727f2d39219cfeab82d52a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517006"
---
# <a name="defi---vs"></a><span data-ttu-id="16f8b-103">Defi-vs</span><span class="sxs-lookup"><span data-stu-id="16f8b-103">defi - vs</span></span>

<span data-ttu-id="16f8b-104">Definiert einen ganzzahligen Konstanten Wert, der immer dann geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="16f8b-104">Defines an integer constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f8b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="16f8b-105">Syntax</span></span>



| <span data-ttu-id="16f8b-106">Defi DST, integerValue0, integerValue1, integerValue2, integerValue3</span><span class="sxs-lookup"><span data-stu-id="16f8b-106">defi dst, integerValue0, integerValue1, integerValue2, integerValue3</span></span> |
|----------------------------------------------------------------------|



 

-   <span data-ttu-id="16f8b-107">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="16f8b-107">dst is the destination register.</span></span>
-   <span data-ttu-id="16f8b-108">integerValue \# ist ein konstanter ganzzahliger Wert.</span><span class="sxs-lookup"><span data-stu-id="16f8b-108">integerValue\# is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16f8b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16f8b-109">Remarks</span></span>



| <span data-ttu-id="16f8b-110">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="16f8b-110">Vertex shader versions</span></span> | <span data-ttu-id="16f8b-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="16f8b-111">1\_1</span></span> | <span data-ttu-id="16f8b-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16f8b-112">2\_0</span></span> | <span data-ttu-id="16f8b-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16f8b-113">2\_x</span></span> | <span data-ttu-id="16f8b-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16f8b-114">2\_sw</span></span> | <span data-ttu-id="16f8b-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16f8b-115">3\_0</span></span> | <span data-ttu-id="16f8b-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16f8b-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="16f8b-117">verteidigen</span><span class="sxs-lookup"><span data-stu-id="16f8b-117">defi</span></span>                   |      | <span data-ttu-id="16f8b-118">x</span><span class="sxs-lookup"><span data-stu-id="16f8b-118">x</span></span>    | <span data-ttu-id="16f8b-119">x</span><span class="sxs-lookup"><span data-stu-id="16f8b-119">x</span></span>    | <span data-ttu-id="16f8b-120">x</span><span class="sxs-lookup"><span data-stu-id="16f8b-120">x</span></span>     | <span data-ttu-id="16f8b-121">x</span><span class="sxs-lookup"><span data-stu-id="16f8b-121">x</span></span>    | <span data-ttu-id="16f8b-122">x</span><span class="sxs-lookup"><span data-stu-id="16f8b-122">x</span></span>     |



 

<span data-ttu-id="16f8b-123">Die defi-Anweisung definiert eine ganzzahlige Shader-Konstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="16f8b-123">The defi instruction defines an integer shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="16f8b-124">Diese werden als unmittelbare Konstanten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="16f8b-124">These are called immediate constants.</span></span> <span data-ttu-id="16f8b-125">Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setvertexshaderconstanti festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="16f8b-125">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantI.</span></span>

<span data-ttu-id="16f8b-126">Es gibt zwei Möglichkeiten, eine ganzzahlige Konstante in einem Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="16f8b-126">There are two ways to set an integer constant in a shader.</span></span>

1.  <span data-ttu-id="16f8b-127">Verwenden Sie defi, um den ganzzahligen Konstanten Vektor direkt in einem Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="16f8b-127">Use defi to define the integer constant vector directly inside a shader.</span></span>
2.  <span data-ttu-id="16f8b-128">Verwenden Sie die API-Methoden, um eine Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="16f8b-128">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="16f8b-129">Verwenden Sie [**setvertexshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) , um eine ganzzahlige Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="16f8b-129">Use [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="16f8b-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16f8b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16f8b-131">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="16f8b-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="16f8b-132">DEF-vs</span><span class="sxs-lookup"><span data-stu-id="16f8b-132">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="16f8b-133">DEFB-vs</span><span class="sxs-lookup"><span data-stu-id="16f8b-133">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 