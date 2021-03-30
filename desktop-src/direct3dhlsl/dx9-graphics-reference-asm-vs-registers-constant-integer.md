---
title: Konstantes ganzzahliges Register (HLSL vs-Referenz)
description: Konstante ganzzahlige Register werden nur von Loop-vs und rep-vs verwendet.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976776"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a><span data-ttu-id="875d0-103">Konstantes ganzzahliges Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="875d0-103">Constant Integer Register (HLSL VS reference)</span></span>

<span data-ttu-id="875d0-104">Konstante ganzzahlige Register werden nur von [Loop-vs](loop---vs.md) und [Rep-vs](rep---vs.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="875d0-104">Constant integer registers are used only by [loop - vs](loop---vs.md) and [rep - vs](rep---vs.md).</span></span>

<span data-ttu-id="875d0-105">Sie können mithilfe von " [defi-vs](defi---vs.md) " oder " [**setvertexshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="875d0-105">They can be set using [defi - vs](defi---vs.md) or [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).</span></span>

<span data-ttu-id="875d0-106">Bei Verwendung als Argument für die [Loop-vs-](loop---vs.md) Anweisung:</span><span class="sxs-lookup"><span data-stu-id="875d0-106">When used as an argument to the [loop - vs](loop---vs.md) instruction:</span></span>

-   <span data-ttu-id="875d0-107">. x ist die Iterations Anzahl.</span><span class="sxs-lookup"><span data-stu-id="875d0-107">.x is the iteration count.</span></span> <span data-ttu-id="875d0-108">([Rep-vs](rep---vs.md) verwendet nur diese Komponente).</span><span class="sxs-lookup"><span data-stu-id="875d0-108">([rep - vs](rep---vs.md) uses only this component).</span></span>
-   <span data-ttu-id="875d0-109">. y ist der Anfangswert des Schleifen Zählers.</span><span class="sxs-lookup"><span data-stu-id="875d0-109">.y is the initial value for the loop counter.</span></span>
-   <span data-ttu-id="875d0-110">. z ist der Inkrement-Schritt für den Schleifen Zählers.</span><span class="sxs-lookup"><span data-stu-id="875d0-110">.z is the increment step for the loop counter.</span></span>

<span data-ttu-id="875d0-111">Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="875d0-111">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="875d0-112">Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="875d0-112">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="875d0-113">Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt.</span><span class="sxs-lookup"><span data-stu-id="875d0-113">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="875d0-114">Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren.</span><span class="sxs-lookup"><span data-stu-id="875d0-114">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="875d0-115">Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="875d0-115">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="875d0-116">Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="875d0-116">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="875d0-117">Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="875d0-117">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="875d0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="875d0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="875d0-119">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="875d0-119">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 