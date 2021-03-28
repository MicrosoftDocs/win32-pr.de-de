---
title: Bezeichnung (SM4-ASM)
description: Gibt den Anfang einer Unterroutine an.
ms.assetid: B966AE64-47CA-4A13-A26F-184D9FD26C26
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff4c2d73db5d776c75b6d6339cecb7748a9868d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719416"
---
# <a name="label-sm4---asm"></a><span data-ttu-id="d6de4-103">Bezeichnung (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d6de4-103">label (sm4 - asm)</span></span>

<span data-ttu-id="d6de4-104">Gibt den Anfang einer Unterroutine an.</span><span class="sxs-lookup"><span data-stu-id="d6de4-104">Indicates the beginning of a subroutine.</span></span>



| <span data-ttu-id="d6de4-105">Bezeichnung l\#</span><span class="sxs-lookup"><span data-stu-id="d6de4-105">label l\#</span></span> |
|-----------|



 



| <span data-ttu-id="d6de4-106">Element</span><span class="sxs-lookup"><span data-stu-id="d6de4-106">Item</span></span>                                                       | <span data-ttu-id="d6de4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6de4-107">Description</span></span>                         |
|------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="d6de4-108"><span id="l_"></span><span id="L_"></span>*int\#*</span><span class="sxs-lookup"><span data-stu-id="d6de4-108"><span id="l_"></span><span id="L_"></span>*l\#*</span></span><br/> | <span data-ttu-id="d6de4-109">\[in \] der Nummer der Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="d6de4-109">\[in\] The label number.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6de4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6de4-110">Remarks</span></span>

<span data-ttu-id="d6de4-111">Eine **Bezeichnung** kann nur direkt nach einer [**ret**](ret--sm4---asm-.md) -Anweisung angezeigt werden, die in keiner der Fluss Steuerungs Anweisungen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d6de4-111">A **label** can only appear directly after a [**ret**](ret--sm4---asm-.md) instruction which is not nested in any flow control statements.</span></span>

<span data-ttu-id="d6de4-112">Der Code vor der ersten **Bezeichnung** in einem Programm ist das Hauptprogramm.</span><span class="sxs-lookup"><span data-stu-id="d6de4-112">The code before the first **label** in a program is the main program.</span></span> <span data-ttu-id="d6de4-113">Alle Unterroutinen werden am Ende des Programms angezeigt, das durch Bezeichnungs Anweisungen **angegeben wird.**</span><span class="sxs-lookup"><span data-stu-id="d6de4-113">All subroutines appear at the end of the program, indicated by **label** statements.</span></span>

<span data-ttu-id="d6de4-114">Das folgende Beispiel zeigt die Verwendung dieser Anweisung.</span><span class="sxs-lookup"><span data-stu-id="d6de4-114">The following example shows how to use this instruction.</span></span>

``` syntax
 
               ...
                call l3
                ...
                ret
                label l3
                    ...
                    if_nz r0.x
                        ret
                    endif
                    ...
                ret
```

<span data-ttu-id="d6de4-115">Diese Anweisung gilt für die folgenden Shader-Phasen:</span><span class="sxs-lookup"><span data-stu-id="d6de4-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d6de4-116">Vertexshader</span><span class="sxs-lookup"><span data-stu-id="d6de4-116">Vertex Shader</span></span> | <span data-ttu-id="d6de4-117">Geometrie-Shader</span><span class="sxs-lookup"><span data-stu-id="d6de4-117">Geometry Shader</span></span> | <span data-ttu-id="d6de4-118">Pixelshader</span><span class="sxs-lookup"><span data-stu-id="d6de4-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d6de4-119">x</span><span class="sxs-lookup"><span data-stu-id="d6de4-119">x</span></span>             | <span data-ttu-id="d6de4-120">x</span><span class="sxs-lookup"><span data-stu-id="d6de4-120">x</span></span>               | <span data-ttu-id="d6de4-121">x</span><span class="sxs-lookup"><span data-stu-id="d6de4-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d6de4-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="d6de4-122">Minimum Shader Model</span></span>

<span data-ttu-id="d6de4-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d6de4-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d6de4-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="d6de4-124">Shader Model</span></span>                                              | <span data-ttu-id="d6de4-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6de4-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d6de4-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="d6de4-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d6de4-127">ja</span><span class="sxs-lookup"><span data-stu-id="d6de4-127">yes</span></span>       |
| [<span data-ttu-id="d6de4-128">Shadermodell 4,1</span><span class="sxs-lookup"><span data-stu-id="d6de4-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d6de4-129">ja</span><span class="sxs-lookup"><span data-stu-id="d6de4-129">yes</span></span>       |
| [<span data-ttu-id="d6de4-130">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="d6de4-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d6de4-131">ja</span><span class="sxs-lookup"><span data-stu-id="d6de4-131">yes</span></span>       |
| [<span data-ttu-id="d6de4-132">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6de4-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d6de4-133">nein</span><span class="sxs-lookup"><span data-stu-id="d6de4-133">no</span></span>        |
| [<span data-ttu-id="d6de4-134">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6de4-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d6de4-135">nein</span><span class="sxs-lookup"><span data-stu-id="d6de4-135">no</span></span>        |
| [<span data-ttu-id="d6de4-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6de4-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d6de4-137">nein</span><span class="sxs-lookup"><span data-stu-id="d6de4-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d6de4-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d6de4-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6de4-139">Shader Model 4-Assembly (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d6de4-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





