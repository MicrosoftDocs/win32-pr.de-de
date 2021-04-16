---
description: Eine Funktion ist der Baustein für einen Shader, der in der Sprache auf hoher Ebene erstellt wird. Wenn Sie Shader lieber in einer Sprache im C-Stil schreiben möchten, anstatt Sie in der Assemblysprache zu verwenden, sollten Sie Funktionen schreiben.
ms.assetid: vs|directx_sdk|~\functions.htm
title: Effekt Funktions Syntax (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21e239359877813e64acea8b5f404a6ade59c992
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520907"
---
# <a name="effect-function-syntax-direct3d-9"></a><span data-ttu-id="3b6c3-104">Effekt Funktions Syntax (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3b6c3-104">Effect Function Syntax (Direct3D 9)</span></span>

<span data-ttu-id="3b6c3-105">Eine Funktion ist der Baustein für einen Shader, der in der Sprache auf hoher Ebene erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-105">A function is the building block for a shader created in the high-level language.</span></span> <span data-ttu-id="3b6c3-106">Wenn Sie Shader lieber in einer Sprache im C-Stil schreiben möchten, anstatt Sie in der Assemblysprache zu verwenden, sollten Sie Funktionen schreiben.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-106">If you prefer to write shaders in a C-style language instead of in assembly language, you will want to write functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3b6c3-107">Syntax</span></span>


```
type id ( [ parameters ] )  
    { body }
```



<span data-ttu-id="3b6c3-108">Funktionen ändern die Parameterwerte nicht in einem Effekt.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-108">Functions do not change parameter values in an effect.</span></span>

-   <span data-ttu-id="3b6c3-109">Type: ein beliebiger gültiger [Verweis für den HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) -Typ.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-109">type - Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span>
-   <span data-ttu-id="3b6c3-110">ID: ein eindeutiger Name.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-110">id - A unique name.</span></span>
-   <span data-ttu-id="3b6c3-111">Parameter-Funktionsparameter.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-111">parameters - Function parameters.</span></span>
-   <span data-ttu-id="3b6c3-112">Body: der Hauptteil der Funktion.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-112">body - The body of the function.</span></span>

<span data-ttu-id="3b6c3-113">Funktionen werden aus der Sprache auf hoher Ebene erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b6c3-113">Functions are built from the high-level language.</span></span> <span data-ttu-id="3b6c3-114">Weitere Informationen finden Sie unter [Referenz für HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3b6c3-114">See [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b6c3-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b6c3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b6c3-116">Effekt Format</span><span class="sxs-lookup"><span data-stu-id="3b6c3-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
