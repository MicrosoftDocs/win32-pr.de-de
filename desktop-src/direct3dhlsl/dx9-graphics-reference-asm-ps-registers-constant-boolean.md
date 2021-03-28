---
title: Konstantes boolesches Register (HLSL PS-Referenz)
description: Dieses Register ist eine Auflistung von Bits, die in statischen Fluss Steuerungs Anweisungen verwendet werden (z. b. Wenn bool-PS-else-PS-endif-PS).
ms.assetid: fb4abe19-d0cf-48ac-866e-4be60cc86bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4868be7c22ce5a6a1881ad7db8acf0af65330c04
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729152"
---
# <a name="constant-boolean-register-hlsl-ps-reference"></a><span data-ttu-id="735f6-103">Konstantes boolesches Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="735f6-103">Constant Boolean register (HLSL PS reference)</span></span>

<span data-ttu-id="735f6-104">Dieses Register ist eine Auflistung von Bits, die in statischen Fluss Steuerungs Anweisungen verwendet werden (z. [b. Wenn bool-PS](if-bool---ps.md)  -  [else-PS](else---ps.md)  -  [EndIf-PS](endif---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="735f6-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - ps](if-bool---ps.md) - [else - ps](else---ps.md) - [endif - ps](endif---ps.md)).</span></span> <span data-ttu-id="735f6-105">Es gibt 16 von Ihnen. Daher kann ein Shader 16 unabhängige Verzweigungs Bedingungen haben.</span><span class="sxs-lookup"><span data-stu-id="735f6-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="735f6-106">Sie können mithilfe von [DEFB-PS](defb---ps.md) oder [**setpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="735f6-106">They can be set using [defb - ps](defb---ps.md) or [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb).</span></span>

<span data-ttu-id="735f6-107">Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="735f6-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="735f6-108">Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="735f6-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="735f6-109">Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt.</span><span class="sxs-lookup"><span data-stu-id="735f6-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="735f6-110">Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren.</span><span class="sxs-lookup"><span data-stu-id="735f6-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="735f6-111">Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="735f6-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="735f6-112">Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="735f6-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="735f6-113">Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="735f6-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>



| <span data-ttu-id="735f6-114">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="735f6-114">Pixel shader versions</span></span>     | <span data-ttu-id="735f6-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="735f6-115">1\_1</span></span> | <span data-ttu-id="735f6-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="735f6-116">1\_2</span></span> | <span data-ttu-id="735f6-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="735f6-117">1\_3</span></span> | <span data-ttu-id="735f6-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="735f6-118">1\_4</span></span> | <span data-ttu-id="735f6-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="735f6-119">2\_0</span></span> | <span data-ttu-id="735f6-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="735f6-120">2\_sw</span></span> | <span data-ttu-id="735f6-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="735f6-121">2\_x</span></span> | <span data-ttu-id="735f6-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="735f6-122">3\_0</span></span> | <span data-ttu-id="735f6-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="735f6-123">3\_sw</span></span> |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="735f6-124">Konstantes boolesches Register</span><span class="sxs-lookup"><span data-stu-id="735f6-124">Constant Boolean register</span></span> |      |      |      |      |      |       | <span data-ttu-id="735f6-125">x</span><span class="sxs-lookup"><span data-stu-id="735f6-125">x</span></span>    | <span data-ttu-id="735f6-126">x</span><span class="sxs-lookup"><span data-stu-id="735f6-126">x</span></span>    | <span data-ttu-id="735f6-127">x</span><span class="sxs-lookup"><span data-stu-id="735f6-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="735f6-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="735f6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="735f6-129">Register</span><span class="sxs-lookup"><span data-stu-id="735f6-129">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 