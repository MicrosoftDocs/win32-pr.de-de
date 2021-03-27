---
title: Konstantes float-Register (HLSL PS-Referenz)
description: Pixel-Shader-Eingabe Register für eine 4D-Gleit Komma Konstante.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05bb382b745d172ea4b81f9920154e7c79a58c2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390753"
---
# <a name="constant-float-register-hlsl-ps-reference"></a><span data-ttu-id="f0fa1-103">Konstantes float-Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="f0fa1-103">Constant float register (HLSL PS reference)</span></span>

<span data-ttu-id="f0fa1-104">Pixel-Shader-Eingabe Register für eine 4D-Gleit Komma Konstante.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-104">Pixel shader input register for a 4D floating-point constant.</span></span>

<span data-ttu-id="f0fa1-105">Sie können mithilfe von [DEF-PS](def---ps.md) oder [**setpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-105">They can be set using [def - ps](def---ps.md) or [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).</span></span>

<span data-ttu-id="f0fa1-106">Das Verhalten der shaderkonstanten wurde zwischen Direct3D 8 und Direct3D 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-106">The behavior of shader constants has changed between Direct3D 8 and Direct3D 9.</span></span>

-   <span data-ttu-id="f0fa1-107">Bei Direct3D 9 weisen Konstanten, die mit defx festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-107">For Direct3D 9, constants set with defx assign values to the shader constant space.</span></span> <span data-ttu-id="f0fa1-108">Die Lebensdauer einer mit defx deklarierten Konstante ist nur auf die Ausführung dieses Shaders beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-108">The lifetime of a constant declared with defx is confined to the execution of that shader only.</span></span> <span data-ttu-id="f0fa1-109">Umgekehrt werden Konstanten, die mithilfe der APIs setxxxshaderconstantx festgelegt wurden, Konstanten im globalen Raum initialisieren.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-109">Conversely, constants set using the APIs SetXXXShaderConstantX initialize constants in global space.</span></span> <span data-ttu-id="f0fa1-110">Konstanten im globalen Raum werden erst in den lokalen Bereich (sichtbar für den Shader) kopiert, bis setxxxshaderconstants aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-110">Constants in global space are not copied to local space (visible to the shader) until SetxxxShaderConstants is called.</span></span>
-   <span data-ttu-id="f0fa1-111">Bei Direct3D 8 weisen Konstanten, die mit defx oder den APIs festgelegt sind, dem Shader-konstantenbereich Werte zu.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-111">For Direct3D 8, constants set with defx or the APIs both assign values to the shader constant space.</span></span> <span data-ttu-id="f0fa1-112">Jedes Mal, wenn der Shader ausgeführt wird, werden die Konstanten vom aktuellen Shader verwendet, unabhängig von dem Verfahren, mit dem Sie festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-112">Each time the shader is executed, the constants are used by the current shader regardless of the technique used to set them.</span></span>

## <a name="examples"></a><span data-ttu-id="f0fa1-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0fa1-113">Examples</span></span>

<span data-ttu-id="f0fa1-114">Im folgenden finden Sie ein Beispiel für das Deklarieren von zwei Gleit Komma Konstanten innerhalb eines Shaders.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-114">Here is an example declaring two floating-point constants within a shader.</span></span>


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



<span data-ttu-id="f0fa1-115">Diese Konstanten werden jedes Mal geladen, wenn [**setpixelshader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-115">These constants are loaded every time [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) is called.</span></span>

<span data-ttu-id="f0fa1-116">Wenn Sie Konstante Werte mit der API festlegen, ist keine Shader-Deklaration erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f0fa1-116">If you are setting constant values with the API, there is no shader declaration required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0fa1-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0fa1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0fa1-118">Register</span><span class="sxs-lookup"><span data-stu-id="f0fa1-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 