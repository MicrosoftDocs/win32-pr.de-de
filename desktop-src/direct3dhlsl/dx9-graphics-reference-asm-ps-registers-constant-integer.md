---
title: Konstantes ganzzahliges Register (HLSL PS-Referenz)
description: Konstante ganzzahlige Register werden nur von Loop-PS und rep-PS verwendet.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976753"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a><span data-ttu-id="f06ba-103">Konstantes ganzzahliges Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="f06ba-103">Constant integer register (HLSL PS reference)</span></span>

<span data-ttu-id="f06ba-104">Konstante ganzzahlige Register werden nur von [Loop-PS](loop---ps.md) und [Rep-PS](rep---ps.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="f06ba-104">Constant integer registers are used only by [loop - ps](loop---ps.md) and [rep - ps](rep---ps.md).</span></span>

<span data-ttu-id="f06ba-105">Sie können mithilfe von " [defi-PS](defi---ps.md) " oder " [**setpixelshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f06ba-105">They can be set using [defi - ps](defi---ps.md) or [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).</span></span>

<span data-ttu-id="f06ba-106">Bei Verwendung als Argument für die [Loop-PS-](loop---ps.md) Anweisung:</span><span class="sxs-lookup"><span data-stu-id="f06ba-106">When used as an argument to the [loop - ps](loop---ps.md) instruction:</span></span>

-   <span data-ttu-id="f06ba-107">. x ist die Iterations Anzahl.</span><span class="sxs-lookup"><span data-stu-id="f06ba-107">.x is the iteration count.</span></span> <span data-ttu-id="f06ba-108">([Rep-PS](rep---ps.md) verwendet nur diese Komponente).</span><span class="sxs-lookup"><span data-stu-id="f06ba-108">([rep - ps](rep---ps.md) uses only this component).</span></span>
-   <span data-ttu-id="f06ba-109">. y ist der Anfangswert des Schleifen Zählers.</span><span class="sxs-lookup"><span data-stu-id="f06ba-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="f06ba-110">. z ist der Inkrement-Schritt für den Schleifen Zählers.</span><span class="sxs-lookup"><span data-stu-id="f06ba-110">.z is the increment step for the loop counter.</span></span>



| <span data-ttu-id="f06ba-111">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="f06ba-111">Pixel shader versions</span></span>     | <span data-ttu-id="f06ba-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="f06ba-112">1\_1</span></span> | <span data-ttu-id="f06ba-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="f06ba-113">1\_2</span></span> | <span data-ttu-id="f06ba-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f06ba-114">1\_3</span></span> | <span data-ttu-id="f06ba-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="f06ba-115">1\_4</span></span> | <span data-ttu-id="f06ba-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f06ba-116">2\_0</span></span> | <span data-ttu-id="f06ba-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f06ba-117">2\_sw</span></span> | <span data-ttu-id="f06ba-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f06ba-118">2\_x</span></span> | <span data-ttu-id="f06ba-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f06ba-119">3\_0</span></span> | <span data-ttu-id="f06ba-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f06ba-120">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="f06ba-121">Konstanter ganzzahliges Register</span><span class="sxs-lookup"><span data-stu-id="f06ba-121">Constant Integer Register</span></span> |      |      |      |      |      |       | <span data-ttu-id="f06ba-122">x</span><span class="sxs-lookup"><span data-stu-id="f06ba-122">x</span></span>    | <span data-ttu-id="f06ba-123">x</span><span class="sxs-lookup"><span data-stu-id="f06ba-123">x</span></span>    | <span data-ttu-id="f06ba-124">x</span><span class="sxs-lookup"><span data-stu-id="f06ba-124">x</span></span>     |



 

<span data-ttu-id="f06ba-125">Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="f06ba-125">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="f06ba-126">Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="f06ba-126">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="f06ba-127">Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f06ba-127">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="f06ba-128">Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren.</span><span class="sxs-lookup"><span data-stu-id="f06ba-128">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="f06ba-129">Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f06ba-129">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="f06ba-130">Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="f06ba-130">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="f06ba-131">Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f06ba-131">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f06ba-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f06ba-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f06ba-133">Register</span><span class="sxs-lookup"><span data-stu-id="f06ba-133">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 