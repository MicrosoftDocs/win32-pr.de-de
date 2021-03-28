---
title: Konstantes boolesches Register (HLSL vs-Referenz)
description: Dieses Register ist eine Auflistung von Bits, die in statischen Fluss Steuerungs Anweisungen verwendet werden (z. b. if bool-vs-else-vs-endif-vs).
ms.assetid: bd02d03b-c228-481a-9c98-7442be4cdd07
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b32841f060a29fce2918daca8f8fd008529bef1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976752"
---
# <a name="constant-boolean-register-hlsl-vs-reference"></a><span data-ttu-id="771a4-103">Konstantes boolesches Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="771a4-103">Constant Boolean register (HLSL VS reference)</span></span>

<span data-ttu-id="771a4-104">Bei diesem Register handelt es sich um eine Auflistung von Bits, die in statischen Fluss Steuerungs Anweisungen verwendet werden (z. [b. bei "bool-vs](if-bool---vs.md)  -  [else-vs](else---vs.md)  -  [EndIf-vs](endif---vs.md)").</span><span class="sxs-lookup"><span data-stu-id="771a4-104">This register is a collection of bits used in static flow control instructions (for example, [if bool - vs](if-bool---vs.md) - [else - vs](else---vs.md) - [endif - vs](endif---vs.md)).</span></span> <span data-ttu-id="771a4-105">Es gibt 16 von Ihnen. Daher kann ein Shader 16 unabhängige Verzweigungs Bedingungen haben.</span><span class="sxs-lookup"><span data-stu-id="771a4-105">There are 16 of them, therefore, a shader can have 16 independent branch conditions.</span></span> <span data-ttu-id="771a4-106">Sie können mithilfe von [DEFB-vs](defb---vs.md) oder [**setvertexshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="771a4-106">They can be set using [defb - vs](defb---vs.md) or [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb).</span></span>

<span data-ttu-id="771a4-107">Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="771a4-107">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="771a4-108">Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="771a4-108">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="771a4-109">Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt.</span><span class="sxs-lookup"><span data-stu-id="771a4-109">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="771a4-110">Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren.</span><span class="sxs-lookup"><span data-stu-id="771a4-110">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="771a4-111">Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="771a4-111">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="771a4-112">Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="771a4-112">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="771a4-113">Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="771a4-113">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="771a4-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="771a4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="771a4-115">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="771a4-115">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 