---
title: ps
description: Diese Anweisung gibt die shaderversionsnummer an und funktioniert für alle shaderversionen.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993191"
---
# <a name="ps"></a><span data-ttu-id="5dbb0-103">ps</span><span class="sxs-lookup"><span data-stu-id="5dbb0-103">ps</span></span>

<span data-ttu-id="5dbb0-104">Diese Anweisung gibt die shaderversionsnummer an und funktioniert für alle shaderversionen.</span><span class="sxs-lookup"><span data-stu-id="5dbb0-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dbb0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dbb0-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="5dbb0-106">Eingabeargumente</span><span class="sxs-lookup"><span data-stu-id="5dbb0-106">Input Arguments</span></span>

<span data-ttu-id="5dbb0-107">Eingabeargumente enthalten eine einzelne Hauptversionsnummer mit einer einzelnen unter Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="5dbb0-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="5dbb0-108">Die zulässigen Kombinationen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dbb0-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="5dbb0-109">Hauptversionen</span><span class="sxs-lookup"><span data-stu-id="5dbb0-109">Main versions</span></span> | <span data-ttu-id="5dbb0-110">Unter Versionen</span><span class="sxs-lookup"><span data-stu-id="5dbb0-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="5dbb0-111">1</span><span class="sxs-lookup"><span data-stu-id="5dbb0-111">1</span></span>             | <span data-ttu-id="5dbb0-112">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="5dbb0-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="5dbb0-113">2</span><span class="sxs-lookup"><span data-stu-id="5dbb0-113">2</span></span>             | <span data-ttu-id="5dbb0-114">0, x (erweitert), SW (Software)</span><span class="sxs-lookup"><span data-stu-id="5dbb0-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="5dbb0-115">3</span><span class="sxs-lookup"><span data-stu-id="5dbb0-115">3</span></span>             | <span data-ttu-id="5dbb0-116">0, SW (Software)</span><span class="sxs-lookup"><span data-stu-id="5dbb0-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="5dbb0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5dbb0-117">Remarks</span></span>



| <span data-ttu-id="5dbb0-118">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5dbb0-118">Pixel shader versions</span></span> | <span data-ttu-id="5dbb0-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="5dbb0-119">1\_1</span></span> | <span data-ttu-id="5dbb0-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="5dbb0-120">1\_2</span></span> | <span data-ttu-id="5dbb0-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5dbb0-121">1\_3</span></span> | <span data-ttu-id="5dbb0-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="5dbb0-122">1\_4</span></span> | <span data-ttu-id="5dbb0-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5dbb0-123">2\_0</span></span> | <span data-ttu-id="5dbb0-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-124">2\_x</span></span> | <span data-ttu-id="5dbb0-125">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5dbb0-125">2\_sw</span></span> | <span data-ttu-id="5dbb0-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5dbb0-126">3\_0</span></span> | <span data-ttu-id="5dbb0-127">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5dbb0-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5dbb0-128">ps</span><span class="sxs-lookup"><span data-stu-id="5dbb0-128">ps</span></span>                    | <span data-ttu-id="5dbb0-129">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-129">x</span></span>    | <span data-ttu-id="5dbb0-130">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-130">x</span></span>    | <span data-ttu-id="5dbb0-131">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-131">x</span></span>    | <span data-ttu-id="5dbb0-132">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-132">x</span></span>    | <span data-ttu-id="5dbb0-133">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-133">x</span></span>    | <span data-ttu-id="5dbb0-134">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-134">x</span></span>    | <span data-ttu-id="5dbb0-135">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-135">x</span></span>     | <span data-ttu-id="5dbb0-136">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-136">x</span></span>    | <span data-ttu-id="5dbb0-137">x</span><span class="sxs-lookup"><span data-stu-id="5dbb0-137">x</span></span>     |



 

<span data-ttu-id="5dbb0-138">Diese Anweisung muss die erste nicht-Kommentar Anweisung in einem Pixelshader sein.</span><span class="sxs-lookup"><span data-stu-id="5dbb0-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="5dbb0-139">Hardwarebeschleunigte Versionen der Software (Versionen ohne \_ SW in der Versionsnummer) können Scheitel Punkte mit Hardware-accelearation verarbeiten oder die Verarbeitung von Software Scheitel Punkten verwenden.</span><span class="sxs-lookup"><span data-stu-id="5dbb0-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="5dbb0-140">Softwareversionen (Versionen mit \_ SW in der Versionsnummer) verarbeiten Vertices nur mit Software.</span><span class="sxs-lookup"><span data-stu-id="5dbb0-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="5dbb0-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dbb0-141">Examples</span></span>

<span data-ttu-id="5dbb0-142">Dieses partielle Beispiel deklariert einen Pixel-Shader der Version 1 \_ .</span><span class="sxs-lookup"><span data-stu-id="5dbb0-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="5dbb0-143">In diesem partiellen Beispiel wird ein 1-Pixel-Shader der Version 1 deklariert \_ .</span><span class="sxs-lookup"><span data-stu-id="5dbb0-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="5dbb0-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5dbb0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dbb0-145">Pixelshaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="5dbb0-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




