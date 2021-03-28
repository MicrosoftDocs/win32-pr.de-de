---
title: Defi-PS
description: Definiert einen ganzzahligen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.
ms.assetid: c51982a1-45b4-48db-a49a-93165d61efd3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3552d5cfe322dd384e1c6bd219e35af19b469a56
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102078"
---
# <a name="defi---ps"></a><span data-ttu-id="c035c-103">Defi-PS</span><span class="sxs-lookup"><span data-stu-id="c035c-103">defi - ps</span></span>

<span data-ttu-id="c035c-104">Definiert einen ganzzahligen Konstanten Wert, der jedes Mal geladen werden muss, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c035c-104">Defines an integer constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c035c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c035c-105">Syntax</span></span>



| <span data-ttu-id="c035c-106">Defi DST, integerValue</span><span class="sxs-lookup"><span data-stu-id="c035c-106">defi dst, integerValue</span></span> |
|------------------------|



 

-   <span data-ttu-id="c035c-107">DST ist das Ziel Register.</span><span class="sxs-lookup"><span data-stu-id="c035c-107">dst is the destination register.</span></span>
-   <span data-ttu-id="c035c-108">integerValue ist ein konstanter ganzzahliger Wert.</span><span class="sxs-lookup"><span data-stu-id="c035c-108">integerValue is a constant integer value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c035c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c035c-109">Remarks</span></span>



| <span data-ttu-id="c035c-110">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="c035c-110">Pixel shader versions</span></span> | <span data-ttu-id="c035c-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="c035c-111">1\_1</span></span> | <span data-ttu-id="c035c-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="c035c-112">1\_2</span></span> | <span data-ttu-id="c035c-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c035c-113">1\_3</span></span> | <span data-ttu-id="c035c-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="c035c-114">1\_4</span></span> | <span data-ttu-id="c035c-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c035c-115">2\_0</span></span> | <span data-ttu-id="c035c-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c035c-116">2\_x</span></span> | <span data-ttu-id="c035c-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c035c-117">2\_sw</span></span> | <span data-ttu-id="c035c-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c035c-118">3\_0</span></span> | <span data-ttu-id="c035c-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c035c-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c035c-120">verteidigen</span><span class="sxs-lookup"><span data-stu-id="c035c-120">defi</span></span>                  |      |      |      |      |      | <span data-ttu-id="c035c-121">x</span><span class="sxs-lookup"><span data-stu-id="c035c-121">x</span></span>    | <span data-ttu-id="c035c-122">x</span><span class="sxs-lookup"><span data-stu-id="c035c-122">x</span></span>     | <span data-ttu-id="c035c-123">x</span><span class="sxs-lookup"><span data-stu-id="c035c-123">x</span></span>    | <span data-ttu-id="c035c-124">x</span><span class="sxs-lookup"><span data-stu-id="c035c-124">x</span></span>     |



 

<span data-ttu-id="c035c-125">Die defi-Anweisung definiert eine shaderkonstante, deren Wert immer dann geladen wird, wenn ein Shader auf ein Gerät festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c035c-125">The defi instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="c035c-126">Diese werden als unmittelbare Konstanten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c035c-126">These are called immediate constants.</span></span> <span data-ttu-id="c035c-127">Unmittelbare Konstanten haben Vorrang vor Konstanten, die von der API-Methode setpixelshaderconstantb festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c035c-127">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="c035c-128">Es gibt zwei Möglichkeiten, eine Konstante in einem Shader festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c035c-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="c035c-129">Verwenden Sie defi, um die Konstante direkt in einem Shader zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c035c-129">Use defi to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="c035c-130">Verwenden Sie die API-Methoden, um eine Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c035c-130">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="c035c-131">Verwenden Sie [**setpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) , um eine boolesche Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c035c-131">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>
    -   <span data-ttu-id="c035c-132">Verwenden Sie [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) , um eine Gleit Komma Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c035c-132">Use [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf) to set a floating-point constant.</span></span>
    -   <span data-ttu-id="c035c-133">Verwenden Sie [**setpixelshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) , um eine ganzzahlige Konstante festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c035c-133">Use [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti) to set an integer constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c035c-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c035c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c035c-135">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="c035c-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 