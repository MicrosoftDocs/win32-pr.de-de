---
title: Prädikat Register (HLSL vs-Referenz)
description: Dieses Vertex-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.
ms.assetid: 4b06e19a-78c7-4886-a0e2-225d419282e7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f558a5fee10d0403eeaacab9dc29ff3ea52b427c
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104038384"
---
# <a name="predicate-register-hlsl-vs-reference"></a><span data-ttu-id="5ff20-103">Prädikat Register (HLSL vs-Referenz)</span><span class="sxs-lookup"><span data-stu-id="5ff20-103">Predicate Register (HLSL VS reference)</span></span>

<span data-ttu-id="5ff20-104">Dieses Vertex-Shader-Ausgabe Register enthält einen booleschen pro-Kanal-Wert.</span><span class="sxs-lookup"><span data-stu-id="5ff20-104">This vertex shader output register contains a per-channel Boolean value.</span></span>

<span data-ttu-id="5ff20-105">Ein Prädikat Register wird von den folgenden Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ff20-105">A predicate register is supported by the following versions.</span></span>



| <span data-ttu-id="5ff20-106">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5ff20-106">Vertex shader versions</span></span> | <span data-ttu-id="5ff20-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="5ff20-107">1\_1</span></span> | <span data-ttu-id="5ff20-108">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ff20-108">2\_0</span></span> | <span data-ttu-id="5ff20-109">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5ff20-109">2\_sw</span></span> | <span data-ttu-id="5ff20-110">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5ff20-110">2\_x</span></span> | <span data-ttu-id="5ff20-111">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5ff20-111">3\_0</span></span> | <span data-ttu-id="5ff20-112">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5ff20-112">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="5ff20-113">Prädikat Register</span><span class="sxs-lookup"><span data-stu-id="5ff20-113">predicate register</span></span>     |      |      |       | <span data-ttu-id="5ff20-114">x</span><span class="sxs-lookup"><span data-stu-id="5ff20-114">x</span></span>    | <span data-ttu-id="5ff20-115">x</span><span class="sxs-lookup"><span data-stu-id="5ff20-115">x</span></span>    | <span data-ttu-id="5ff20-116">x</span><span class="sxs-lookup"><span data-stu-id="5ff20-116">x</span></span>     |



 

<span data-ttu-id="5ff20-117">Hier sind die Register Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ff20-117">Here are the register properties.</span></span>



| <span data-ttu-id="5ff20-118">Registriungstyp</span><span class="sxs-lookup"><span data-stu-id="5ff20-118">Register type</span></span> | <span data-ttu-id="5ff20-119">Anzahl</span><span class="sxs-lookup"><span data-stu-id="5ff20-119">Count</span></span> | <span data-ttu-id="5ff20-120">R/W</span><span class="sxs-lookup"><span data-stu-id="5ff20-120">R/W</span></span> | <span data-ttu-id="5ff20-121">\# Leseports</span><span class="sxs-lookup"><span data-stu-id="5ff20-121">\# Read ports</span></span> | <span data-ttu-id="5ff20-122">\# Lese-/inst-</span><span class="sxs-lookup"><span data-stu-id="5ff20-122">\# Reads/inst</span></span> | <span data-ttu-id="5ff20-123">Dimension</span><span class="sxs-lookup"><span data-stu-id="5ff20-123">Dimension</span></span> | <span data-ttu-id="5ff20-124">Reladdr</span><span class="sxs-lookup"><span data-stu-id="5ff20-124">RelAddr</span></span> | <span data-ttu-id="5ff20-125">der Arbeitszeittabelle</span><span class="sxs-lookup"><span data-stu-id="5ff20-125">Defaults</span></span> | <span data-ttu-id="5ff20-126">Erfordert DCL</span><span class="sxs-lookup"><span data-stu-id="5ff20-126">Requires DCL</span></span> |
|---------------|-------|-----|---------------|---------------|-----------|---------|----------|--------------|
| <span data-ttu-id="5ff20-127">Prädikat (p)</span><span class="sxs-lookup"><span data-stu-id="5ff20-127">Predicate(p)</span></span>  | <span data-ttu-id="5ff20-128">1</span><span class="sxs-lookup"><span data-stu-id="5ff20-128">1</span></span>     | <span data-ttu-id="5ff20-129">R/W</span><span class="sxs-lookup"><span data-stu-id="5ff20-129">R/W</span></span> | <span data-ttu-id="5ff20-130">1</span><span class="sxs-lookup"><span data-stu-id="5ff20-130">1</span></span>             | <span data-ttu-id="5ff20-131">1</span><span class="sxs-lookup"><span data-stu-id="5ff20-131">1</span></span>             | <span data-ttu-id="5ff20-132">4</span><span class="sxs-lookup"><span data-stu-id="5ff20-132">4</span></span>         | <span data-ttu-id="5ff20-133">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="5ff20-133">N/A</span></span>     | <span data-ttu-id="5ff20-134">Keine</span><span class="sxs-lookup"><span data-stu-id="5ff20-134">None</span></span>     | <span data-ttu-id="5ff20-135">N</span><span class="sxs-lookup"><span data-stu-id="5ff20-135">N</span></span>            |



 

<span data-ttu-id="5ff20-136">Das Prädikat Register kann mit [SETP \_ Comp-vs](setp-comp---vs.md)geändert werden. Es sind keine Standardwerte für dieses Register vorhanden. eine Anwendung muss das Register festlegen, bevor Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ff20-136">The predicate register can be modified with [setp\_comp - vs](setp-comp---vs.md). There are no default values for this register, an application needs to set the register before it is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ff20-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ff20-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff20-138">Vertex-Shader-Register</span><span class="sxs-lookup"><span data-stu-id="5ff20-138">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




