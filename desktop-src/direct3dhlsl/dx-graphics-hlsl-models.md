---
title: Shader-Modelle vs shaderprofile
description: Shader-Modelle vs shaderprofile
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856676"
---
# <a name="shader-models-vs-shader-profiles"></a><span data-ttu-id="93d73-103">Shader-Modelle vs shaderprofile</span><span class="sxs-lookup"><span data-stu-id="93d73-103">Shader Models vs Shader Profiles</span></span>

<span data-ttu-id="93d73-104">Die allgemeine Schattierungs Sprache für DirectX implementiert eine Reihe von shadermodellen.</span><span class="sxs-lookup"><span data-stu-id="93d73-104">The High Level Shading Language for DirectX implements a series of shader models.</span></span> <span data-ttu-id="93d73-105">Mit HLSL können Sie C-ähnliche programmierbare Shader für die Direct3D-Pipeline erstellen.</span><span class="sxs-lookup"><span data-stu-id="93d73-105">Using HLSL, you can create C-like programmable shaders for the Direct3D pipeline.</span></span> <span data-ttu-id="93d73-106">Jedes Shader-Modell baut auf den Untertiteln des Modells vor, wobei mehr Funktionen mit weniger Einschränkungen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="93d73-106">Each shader model builds on the capabilites of the model before it, implementing more functionality with fewer restrictions.</span></span>

<span data-ttu-id="93d73-107">Shadermodell 1 hat mit DirectX 8 begonnen und umfasst Assemblyebene und C-ähnliche Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="93d73-107">Shader model 1 started with DirectX 8 and included assembly level and C-like instructions.</span></span> <span data-ttu-id="93d73-108">Dieses Modell weist viele Einschränkungen auf, die durch eine frühe programmierbare shaderhardware verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="93d73-108">This model has many limitations caused by early programmable shader hardware.</span></span> <span data-ttu-id="93d73-109">Das Shadermodell 2 und 3 wurde in der Anzahl der Anweisungen stark erweitert, und Konstanten können verwenden.</span><span class="sxs-lookup"><span data-stu-id="93d73-109">Shader model 2 and 3 greatly expanded on the number of instructions, and constants shaders could use.</span></span> <span data-ttu-id="93d73-110">Sie sind viel leistungsfähiger als Shader-Modell 1, aber dennoch einige der vorhandenen Einschränkungen des ersten shadermodells.</span><span class="sxs-lookup"><span data-stu-id="93d73-110">They are much more powerful than shader model 1, but still carry some of the existing limitations of the first shader model.</span></span>

<span data-ttu-id="93d73-111">Ab Windows Vista ist Shader Model 4 eine komplette Umgestaltung.</span><span class="sxs-lookup"><span data-stu-id="93d73-111">Starting with Windows Vista, shader model 4 is a complete redesign.</span></span> <span data-ttu-id="93d73-112">Sie ermöglicht unbegrenzte Anweisungen und Konstanten (innerhalb von Hardware Einschränkungen Ihres Computers), verfügt über vorlagenbasierte Objekte, die die Textur Stichproben Bereinigung vereinfachen und effizienter sind und über die geringsten Einschränkungen jedes shadermodells verfügen.</span><span class="sxs-lookup"><span data-stu-id="93d73-112">It allows unlimited instructions and constants (within hardware constraints of your machine), has templated objects to make texture sampling cleaner and more efficient, and has the fewest restrictions of any shader model.</span></span> <span data-ttu-id="93d73-113">Dies erfordert jedoch die Windows-Treibermodell, die nur auf dem Betriebssystem Windows Vista (oder höher) verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="93d73-113">It does however require the Windows Driver Model which is only available on the Windows Vista (or later) operating system.</span></span>

## <a name="shader-profiles"></a><span data-ttu-id="93d73-114">Shaderprofile</span><span class="sxs-lookup"><span data-stu-id="93d73-114">Shader Profiles</span></span>

<span data-ttu-id="93d73-115">Ein Shader-Profil ist das Ziel für die Kompilierung eines Shaders. in dieser Tabelle werden die shaderprofile aufgelistet, die von den einzelnen Shader-Modellen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="93d73-115">A shader profile is the target for compiling a shader; this table lists the shader profiles that are supported by each shader model.</span></span>



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d73-116">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="93d73-116">Shader Model</span></span>                                       | <span data-ttu-id="93d73-117">Shaderprofile</span><span class="sxs-lookup"><span data-stu-id="93d73-117">Shader Profiles</span></span>                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="93d73-118">Shader-Modell 1</span><span class="sxs-lookup"><span data-stu-id="93d73-118">Shader Model 1</span></span>](dx-graphics-hlsl-sm1.md)         | <span data-ttu-id="93d73-119">vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="93d73-119">vs\_1\_1</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="93d73-120">Shadermodell 2</span><span class="sxs-lookup"><span data-stu-id="93d73-120">Shader Model 2</span></span>](dx-graphics-hlsl-sm2.md)         | <span data-ttu-id="93d73-121">PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 0, PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1, PS \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3, vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 0, vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1, vs \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3, lib \_ 4 \_ 0 \_ Ebene \_ 9 \_ 1, lib \_ 4 \_ 0 \_ Ebene \_ 9 \_ 3</span><span class="sxs-lookup"><span data-stu-id="93d73-121">ps\_2\_0, ps\_2\_x, vs\_2\_0, vs\_2\_x, ps\_4\_0\_level\_9\_0, ps\_4\_0\_level\_9\_1, ps\_4\_0\_level\_9\_3, vs\_4\_0\_level\_9\_0, vs\_4\_0\_level\_9\_1, vs\_4\_0\_level\_9\_3, lib\_4\_0\_level\_9\_1, lib\_4\_0\_level\_9\_3</span></span>                                                                      |
| [<span data-ttu-id="93d73-122">Shader-Modell 3</span><span class="sxs-lookup"><span data-stu-id="93d73-122">Shader Model 3</span></span>](dx-graphics-hlsl-sm3.md)         | <span data-ttu-id="93d73-123">PS \_ 3 \_ 0, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="93d73-123">ps\_3\_0, vs\_3\_0</span></span>                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="93d73-124">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="93d73-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)         | <span data-ttu-id="93d73-125">CS \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, CS \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="93d73-125">cs\_4\_0, gs\_4\_0, ps\_4\_0, vs\_4\_0, cs\_4\_1, gs\_4\_1, ps\_4\_1, vs\_4\_1, lib\_4\_0, lib\_4\_1</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="93d73-126">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="93d73-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="93d73-127">CS \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (obwohl GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 und vs \_ 4 \_ 1 im Shader-Modell 4,0 eingeführt wurden, fügt Shader Model 5 Unterstützung für diese shaderprofile für strukturierte Puffer und Byte Adress Puffer hinzu.)</span><span class="sxs-lookup"><span data-stu-id="93d73-127">cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0, lib\_5\_0 (Although gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0, and vs\_4\_1 were introduced in shader model 4.0, shader model 5 adds support to these shader profiles for structured buffers and byte address buffers.)</span></span><br/> |
| [<span data-ttu-id="93d73-128">Shader-Modell 6</span><span class="sxs-lookup"><span data-stu-id="93d73-128">Shader Model 6</span></span>](shader-model-6-0.md)             | <span data-ttu-id="93d73-129">CS \_ 6 0 \_ , DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0</span><span class="sxs-lookup"><span data-stu-id="93d73-129">cs\_6\_0, ds\_6\_0, gs\_6\_0, hs\_6\_0, ps\_6\_0, vs\_6\_0, lib\_6\_0</span></span>                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d73-130">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="93d73-130">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="93d73-131">Direct3D 9 hat die Shader-Modelle 1, 2 und 3 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-131">Direct3D 9 introduced shader models 1, 2, and 3.</span></span><br/> <span data-ttu-id="93d73-132">Direct3D 10 hat Shader Model 4 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-132">Direct3D 10 introduced shader model 4.</span></span><br/> <span data-ttu-id="93d73-133">Direct3D 10,1 hat das Shadermodell 4,1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-133">Direct3D 10.1 introduced shader model 4.1.</span></span><br/> |



 

## <a name="effect-profiles"></a><span data-ttu-id="93d73-134">Effekt profile</span><span class="sxs-lookup"><span data-stu-id="93d73-134">Effect Profiles</span></span>

<span data-ttu-id="93d73-135">Ein Effekt Profil ist das Ziel zum Kompilieren eines Effekts/Shader. in dieser Tabelle werden die Effekt Profile aufgelistet, die von den einzelnen Versionen von Direct3D unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="93d73-135">An effect profile is the target for compiling an effect/shader; this table lists the effect profiles that are supported by each version of Direct3D.</span></span>



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d73-136">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="93d73-136">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="93d73-137">Direct3D 9 hat die Auswirkung-Framework-profile FX \_ 1 \_ 0 und FX \_ 2 \_ 0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-137">Direct3D 9 introduced effect-framework profiles fx\_1\_0 and fx\_2\_0.</span></span><br/> <span data-ttu-id="93d73-138">Direct3D 10 hat das Effect-Framework-Profil FX \_ 4 \_ 0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-138">Direct3D 10 introduced effect-framework profile fx\_4\_0.</span></span><br/> <span data-ttu-id="93d73-139">Direct3D 10,1 hat das Effect-Framework-Profil FX \_ 4 \_ 1 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-139">Direct3D 10.1 introduced effect-framework profile fx\_4\_1.</span></span><br/> <span data-ttu-id="93d73-140">Direct3D 11 hat das Effect-Framework-Profil FX \_ 5 \_ 0 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="93d73-140">Direct3D 11 introduced effect-framework profile fx\_5\_0.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="93d73-141">Diese Legacy Effekt Profile sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="93d73-141">These legacy effects profiles are deprecated.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="93d73-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93d73-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93d73-143">Verweis für HLSL</span><span class="sxs-lookup"><span data-stu-id="93d73-143">Reference for HLSL</span></span>](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





