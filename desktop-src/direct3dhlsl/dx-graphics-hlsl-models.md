---
title: Shadermodelle im Vergleich zu Shaderprofilen
description: Shadermodelle im Vergleich zu Shaderprofilen
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 963e68d5875c3ee512e7e0d6ee7c243db72f4400
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119615"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="846d4-103">Shadermodelle im Vergleich zu Shaderprofilen</span><span class="sxs-lookup"><span data-stu-id="846d4-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="846d4-104">Die Schattierungssprache auf hoher Ebene für DirectX implementiert eine Reihe von Shadermodellen.</span><span class="sxs-lookup"><span data-stu-id="846d4-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="846d4-105">Mit HLSL können Sie C-ähnliche programmierbare Shader für die Direct3D-Pipeline erstellen.</span><span class="sxs-lookup"><span data-stu-id="846d4-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="846d4-106">Jedes Shadermodell baut auf den Funktionen des Modells auf, bevor es verfügbar ist, und implementiert mehr Funktionalität mit weniger Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="846d4-106">Each shader model builds on the capabilities of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="846d4-107">Shadermodell 1 wurde mit DirectX 8 gestartet und enthielt Assemblyebene und C-ähnliche Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="846d4-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="846d4-108">Dieses Modell weist viele Einschränkungen auf, die durch frühe programmierbare Shaderhardware verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="846d4-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="846d4-109">Shadermodell 2 und 3 wurden aufgrund der Anzahl von Anweisungen stark erweitert, und Konstanten-Shader könnten verwenden.</span><span class="sxs-lookup"><span data-stu-id="846d4-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="846d4-110">Sie sind viel leistungsstärker als Shadermodell 1, haben aber trotzdem einige der bestehenden Einschränkungen des ersten Shadermodells.</span><span class="sxs-lookup"><span data-stu-id="846d4-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="846d4-111">Ab Windows Vista ist Shadermodell 4 ein vollständiges Design.</span><span class="sxs-lookup"><span data-stu-id="846d4-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="846d4-112">Sie ermöglicht unbegrenzte Anweisungen und Konstanten (innerhalb der Hardwareeinschränkungen Ihres Computers), verfügt über Vorlagenobjekte, um die Textursampling übersichtlicher und effizienter zu gestalten, und weist die geringsten Einschränkungen für jedes Shadermodell auf.</span><span class="sxs-lookup"><span data-stu-id="846d4-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="846d4-113">Es ist jedoch die Windows-Treibermodell erforderlich, die nur unter dem Betriebssystem Windows Vista (oder höher) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="846d4-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="846d4-114">Shaderprofile</span><span class="sxs-lookup"><span data-stu-id="846d4-114">Shader Profiles</span></span>

<span data-ttu-id="846d4-115">Ein Shaderprofil ist das Ziel zum Kompilieren eines Shaders. In dieser Tabelle sind die Shaderprofile aufgeführt, die von den einzelnen Shadermodellen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="846d4-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



| <span data-ttu-id="846d4-116">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="846d4-116">Shader model</span></span>                                                   | <span data-ttu-id="846d4-117">Shaderprofile</span><span class="sxs-lookup"><span data-stu-id="846d4-117">Shader profiles</span></span>                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="846d4-118">Shadermodell 1</span><span class="sxs-lookup"><span data-stu-id="846d4-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="846d4-119">Vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="846d4-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="846d4-120">Shadermodell 2</span><span class="sxs-lookup"><span data-stu-id="846d4-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="846d4-121">ps \_ 2 \_ 0, ps \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 \_ level \_ 9 \_ 0, ps \_ 4 \_ 0 level \_ \_ 9 \_ 1, ps \_ 4 \_ 0 level \_ \_ 9 \_ 3, vs \_ 4 \_ 0 level \_ \_ 9 \_ 0, vs \_ 4 \_ 0 level \_ \_ 9 \_ 1, vs \_ 4 \_ 0 level \_ \_ 9 \_ 3, lib \_ 4 \_ 0 level \_ \_ 9 \_ 1, lib \_ 4 \_ 0 level \_ \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="846d4-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="846d4-122">Shadermodell 3</span><span class="sxs-lookup"><span data-stu-id="846d4-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="846d4-123">ps \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="846d4-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="846d4-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="846d4-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="846d4-125">cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="846d4-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="846d4-126">Shadermodell 5</span><span class="sxs-lookup"><span data-stu-id="846d4-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="846d4-127">cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (obwohl gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps \_ 4 \_ 1, vs \_ 4 \_ 0 und vs \_ 4 \_ 1 im Shadermodell 4.0 eingeführt wurden, fügt Shadermodell 5 diesen Shaderprofilen Unterstützung für strukturierte Puffer und Byteadresspuffer hinzu.)</span><span class="sxs-lookup"><span data-stu-id="846d4-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="846d4-128">Shadermodell 6</span><span class="sxs-lookup"><span data-stu-id="846d4-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="846d4-129">cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="846d4-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |

<span data-ttu-id="846d4-130">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="846d4-130">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="846d4-131">Mit Direct3D 9 wurden die Shadermodelle 1, 2 und 3 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span>
- <span data-ttu-id="846d4-132">Direct3D 10 hat Shadermodell 4 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-132">Direct3D 10 introduced shader model 4.</span></span>
- <span data-ttu-id="846d4-133">Mit Direct3D 10.1 wurde das Shadermodell 4.1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-133">Direct3D 10.1 introduced shader model 4.1.</span></span>



 

## <a name="effect-profiles"></a><span data-ttu-id="846d4-134">Effektprofile</span><span class="sxs-lookup"><span data-stu-id="846d4-134">Effect Profiles</span></span>

<span data-ttu-id="846d4-135">Ein Effektprofil ist das Ziel zum Kompilieren eines Effekts/Shaders. In dieser Tabelle sind die Effektprofile aufgeführt, die von jeder Version von Direct3D unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="846d4-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>

<span data-ttu-id="846d4-136">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="846d4-136">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="846d4-137">Direct3D 9 hat effect-framework profiles fx \_ 1 \_ 0 und fx \_ 2 \_ 0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span>
- <span data-ttu-id="846d4-138">Direct3D 10 hat effect-framework profile fx \_ 4 \_ 0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span>
- <span data-ttu-id="846d4-139">Direct3D 10.1 hat effect-framework profile fx \_ 4 \_ 1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span>
- <span data-ttu-id="846d4-140">Direct3D 11 hat effect-framework profile fx \_ 5 \_ 0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="846d4-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span>

> [!Note]  
> <span data-ttu-id="846d4-141">Diese Legacyeffektprofile sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="846d4-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="846d4-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="846d4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="846d4-143">Referenz für HLSL</span><span class="sxs-lookup"><span data-stu-id="846d4-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





