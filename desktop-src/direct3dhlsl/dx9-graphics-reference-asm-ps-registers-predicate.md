---
title: Prädikat Register (HLSL PS-Referenz)
description: Dieses Pixel-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.
ms.assetid: dc5bff90-4efa-4390-b744-dd1e894ff540
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54c0706b110e04548c836bed8ae794f8da73747e
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719530"
---
# <a name="predicate-register-hlsl-ps-reference"></a><span data-ttu-id="6ae3c-103">Prädikat Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="6ae3c-103">Predicate register (HLSL PS reference)</span></span>

<span data-ttu-id="6ae3c-104">Dieses Pixel-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.</span><span class="sxs-lookup"><span data-stu-id="6ae3c-104">This pixel shader output register contains a per-channel boolean value.</span></span>

<span data-ttu-id="6ae3c-105">Ein Prädikat Register wird von folgenden Versionen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6ae3c-105">A predicate register is supported by the following versions:</span></span>



| <span data-ttu-id="6ae3c-106">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="6ae3c-106">Pixel shader versions</span></span> | <span data-ttu-id="6ae3c-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="6ae3c-107">1\_1</span></span> | <span data-ttu-id="6ae3c-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="6ae3c-108">1\_2</span></span> | <span data-ttu-id="6ae3c-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6ae3c-109">1\_3</span></span> | <span data-ttu-id="6ae3c-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="6ae3c-110">1\_4</span></span> | <span data-ttu-id="6ae3c-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ae3c-111">2\_0</span></span> | <span data-ttu-id="6ae3c-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ae3c-112">2\_sw</span></span> | <span data-ttu-id="6ae3c-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6ae3c-113">2\_x</span></span> | <span data-ttu-id="6ae3c-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6ae3c-114">3\_0</span></span> | <span data-ttu-id="6ae3c-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6ae3c-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="6ae3c-116">Prädikat Register</span><span class="sxs-lookup"><span data-stu-id="6ae3c-116">predicate register</span></span>    |      |      |      |      |      |       | <span data-ttu-id="6ae3c-117">x</span><span class="sxs-lookup"><span data-stu-id="6ae3c-117">x</span></span>    | <span data-ttu-id="6ae3c-118">x</span><span class="sxs-lookup"><span data-stu-id="6ae3c-118">x</span></span>    | <span data-ttu-id="6ae3c-119">x</span><span class="sxs-lookup"><span data-stu-id="6ae3c-119">x</span></span>     |



 

<span data-ttu-id="6ae3c-120">Hier sind die Register Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="6ae3c-120">Here are the register properties.</span></span>



| <span data-ttu-id="6ae3c-121">Registriungstyp</span><span class="sxs-lookup"><span data-stu-id="6ae3c-121">Register type</span></span> | <span data-ttu-id="6ae3c-122">Anzahl</span><span class="sxs-lookup"><span data-stu-id="6ae3c-122">Count</span></span> | <span data-ttu-id="6ae3c-123">R/W</span><span class="sxs-lookup"><span data-stu-id="6ae3c-123">R/W</span></span> | <span data-ttu-id="6ae3c-124">\# Leseports</span><span class="sxs-lookup"><span data-stu-id="6ae3c-124">\# Read ports</span></span> | <span data-ttu-id="6ae3c-125">\# Lese-/inst-</span><span class="sxs-lookup"><span data-stu-id="6ae3c-125">\# Reads/inst</span></span> | <span data-ttu-id="6ae3c-126">Dimension</span><span class="sxs-lookup"><span data-stu-id="6ae3c-126">Dimension</span></span> | <span data-ttu-id="6ae3c-127">Reladdr</span><span class="sxs-lookup"><span data-stu-id="6ae3c-127">RelAddr</span></span> | <span data-ttu-id="6ae3c-128">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="6ae3c-128">Defaults</span></span> | <span data-ttu-id="6ae3c-129">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="6ae3c-129">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="6ae3c-130">Prädikat (p)</span><span class="sxs-lookup"><span data-stu-id="6ae3c-130">Predicate(p)</span></span>  | <span data-ttu-id="6ae3c-131">1</span><span class="sxs-lookup"><span data-stu-id="6ae3c-131">1</span></span>     | <span data-ttu-id="6ae3c-132">R/W</span><span class="sxs-lookup"><span data-stu-id="6ae3c-132">R/W</span></span> | <span data-ttu-id="6ae3c-133">1</span><span class="sxs-lookup"><span data-stu-id="6ae3c-133">1</span></span>             | <span data-ttu-id="6ae3c-134">1</span><span class="sxs-lookup"><span data-stu-id="6ae3c-134">1</span></span>             | <span data-ttu-id="6ae3c-135">4</span><span class="sxs-lookup"><span data-stu-id="6ae3c-135">4</span></span>         | <span data-ttu-id="6ae3c-136">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="6ae3c-136">N/A</span></span>     | <span data-ttu-id="6ae3c-137">Keine</span><span class="sxs-lookup"><span data-stu-id="6ae3c-137">None</span></span>     | <span data-ttu-id="6ae3c-138">N</span><span class="sxs-lookup"><span data-stu-id="6ae3c-138">N</span></span>            |



 

<span data-ttu-id="6ae3c-139">Das Prädikat Register kann mit [SETP \_ Comp-PS](setp-comp---ps.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6ae3c-139">The predicate register can be modified with [setp\_comp - ps](setp-comp---ps.md).</span></span> <span data-ttu-id="6ae3c-140">Es sind keine Standardwerte für dieses Register vorhanden. eine Anwendung muss das Register festlegen, bevor Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ae3c-140">There are no default values for this register; an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ae3c-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6ae3c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ae3c-142">Register</span><span class="sxs-lookup"><span data-stu-id="6ae3c-142">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




