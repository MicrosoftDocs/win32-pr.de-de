---
title: vs
description: Diese Anweisung gibt die Shader-Versionsnummer an. Diese Anweisung funktioniert für alle shaderversionen.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389588"
---
# <a name="vs"></a><span data-ttu-id="40445-104">vs</span><span class="sxs-lookup"><span data-stu-id="40445-104">vs</span></span>

<span data-ttu-id="40445-105">Diese Anweisung gibt die Shader-Versionsnummer an.</span><span class="sxs-lookup"><span data-stu-id="40445-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="40445-106">Diese Anweisung funktioniert für alle shaderversionen.</span><span class="sxs-lookup"><span data-stu-id="40445-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="40445-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40445-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="40445-108">Eingabeargumente</span><span class="sxs-lookup"><span data-stu-id="40445-108">Input Arguments</span></span>

<span data-ttu-id="40445-109">Eingabeargumente enthalten eine einzelne Hauptversionsnummer mit einer einzelnen unter Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="40445-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="40445-110">Die zulässigen Kombinationen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="40445-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="40445-111">Hauptversionen</span><span class="sxs-lookup"><span data-stu-id="40445-111">Main versions</span></span> | <span data-ttu-id="40445-112">Unter Versionen</span><span class="sxs-lookup"><span data-stu-id="40445-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="40445-113">1</span><span class="sxs-lookup"><span data-stu-id="40445-113">1</span></span>             | <span data-ttu-id="40445-114">1</span><span class="sxs-lookup"><span data-stu-id="40445-114">1</span></span>                              |
| <span data-ttu-id="40445-115">2</span><span class="sxs-lookup"><span data-stu-id="40445-115">2</span></span>             | <span data-ttu-id="40445-116">0, SW (Software), x (erweitert)</span><span class="sxs-lookup"><span data-stu-id="40445-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="40445-117">3</span><span class="sxs-lookup"><span data-stu-id="40445-117">3</span></span>             | <span data-ttu-id="40445-118">0, SW (Software)</span><span class="sxs-lookup"><span data-stu-id="40445-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="40445-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40445-119">Remarks</span></span>



| <span data-ttu-id="40445-120">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="40445-120">Vertex shader versions</span></span> | <span data-ttu-id="40445-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="40445-121">1\_1</span></span> | <span data-ttu-id="40445-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="40445-122">2\_0</span></span> | <span data-ttu-id="40445-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="40445-123">2\_x</span></span> | <span data-ttu-id="40445-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="40445-124">2\_sw</span></span> | <span data-ttu-id="40445-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="40445-125">3\_0</span></span> | <span data-ttu-id="40445-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="40445-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="40445-127">vs</span><span class="sxs-lookup"><span data-stu-id="40445-127">vs</span></span>                     | <span data-ttu-id="40445-128">x</span><span class="sxs-lookup"><span data-stu-id="40445-128">x</span></span>    | <span data-ttu-id="40445-129">x</span><span class="sxs-lookup"><span data-stu-id="40445-129">x</span></span>    | <span data-ttu-id="40445-130">x</span><span class="sxs-lookup"><span data-stu-id="40445-130">x</span></span>    | <span data-ttu-id="40445-131">x</span><span class="sxs-lookup"><span data-stu-id="40445-131">x</span></span>     | <span data-ttu-id="40445-132">x</span><span class="sxs-lookup"><span data-stu-id="40445-132">x</span></span>    | <span data-ttu-id="40445-133">x</span><span class="sxs-lookup"><span data-stu-id="40445-133">x</span></span>     |



 

<span data-ttu-id="40445-134">Diese Anweisung muss die erste Anweisung sein, die kein Kommentar in einem Scheitelpunkt-Shader ist.</span><span class="sxs-lookup"><span data-stu-id="40445-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="40445-135">Diese Anweisung wird in allen Scheitelpunkt-Shader-Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40445-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="40445-136">Hardwarebeschleunigte Versionen der Software (Versionen ohne \_ SW in der Versionsnummer) können Scheitel Punkte mit Hardware-accelearation verarbeiten oder die Verarbeitung von Software Scheitel Punkten verwenden.</span><span class="sxs-lookup"><span data-stu-id="40445-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="40445-137">Softwareversionen (Versionen mit \_ SW in der Versionsnummer) verarbeiten Vertices nur mit Software.</span><span class="sxs-lookup"><span data-stu-id="40445-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="40445-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40445-138">Examples</span></span>

<span data-ttu-id="40445-139">In diesem partiellen Beispiel wird ein \_ Vertex-Shader der Version 1 deklariert.</span><span class="sxs-lookup"><span data-stu-id="40445-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="40445-140">In diesem partiellen Beispiel wird ein Software-Vertex-Shader der Version 2 deklariert.</span><span class="sxs-lookup"><span data-stu-id="40445-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="40445-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40445-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40445-142">Vertex-shaderanweisungen</span><span class="sxs-lookup"><span data-stu-id="40445-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




