---
title: Vertex-Shader-Quell Registrierungs Modifiers
description: Quellmodifiziererer können angewendet werden, um die aus einem Quell Register gelesenen Daten zu ändern, bevor die Daten von der Anweisung verwendet werden.
ms.assetid: 516ff7ca-0071-44ac-a246-612a9faa7e7b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c663741da50620e03cfde9f13d67a0c0063453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388519"
---
# <a name="vertex-shader-source-register-modifiers"></a><span data-ttu-id="53fb5-103">Vertex-Shader-Quell Registrierungs Modifiers</span><span class="sxs-lookup"><span data-stu-id="53fb5-103">Vertex Shader Source Register Modifiers</span></span>

<span data-ttu-id="53fb5-104">Quellmodifiziererer können angewendet werden, um die aus einem Quell Register gelesenen Daten zu ändern, bevor die Daten von der Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53fb5-104">Source modifiers can be applied to modify the data read from a source register before the data is used by the instruction.</span></span>

## <a name="negate"></a><span data-ttu-id="53fb5-105">Negate</span><span class="sxs-lookup"><span data-stu-id="53fb5-105">Negate</span></span>

<span data-ttu-id="53fb5-106">Negieren Sie den Inhalt des Quell Registers.</span><span class="sxs-lookup"><span data-stu-id="53fb5-106">Negate the contents of the source register.</span></span>



| <span data-ttu-id="53fb5-107">Komponentenmodifizierer</span><span class="sxs-lookup"><span data-stu-id="53fb5-107">Component modifier</span></span> | <span data-ttu-id="53fb5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53fb5-108">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="53fb5-109">\- r</span><span class="sxs-lookup"><span data-stu-id="53fb5-109">\- r</span></span>               | <span data-ttu-id="53fb5-110">Quell Negation</span><span class="sxs-lookup"><span data-stu-id="53fb5-110">Source negation</span></span> |



 

<span data-ttu-id="53fb5-111">Der Negation-Modifizierer kann nicht für das zweite Quell Register dieser Anweisungen verwendet werden: [m3x2-vs](m3x2---vs.md), [M3x3-vs](m3x3---vs.md), [M3x4-vs](m3x4---vs.md), [m4x3-vs](m4x3---vs.md), [M4x4-vs](m4x4---vs.md).</span><span class="sxs-lookup"><span data-stu-id="53fb5-111">The negate modifier cannot be used on second source register of these instructions: [m3x2 - vs](m3x2---vs.md), [m3x3 - vs](m3x3---vs.md), [m3x4 - vs](m3x4---vs.md), [m4x3 - vs](m4x3---vs.md), [m4x4 - vs](m4x4---vs.md).</span></span>



| <span data-ttu-id="53fb5-112">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="53fb5-112">Vertex shader versions</span></span> | <span data-ttu-id="53fb5-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="53fb5-113">1\_1</span></span> | <span data-ttu-id="53fb5-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53fb5-114">2\_0</span></span> | <span data-ttu-id="53fb5-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53fb5-115">2\_x</span></span> | <span data-ttu-id="53fb5-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53fb5-116">2\_sw</span></span> | <span data-ttu-id="53fb5-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53fb5-117">3\_0</span></span> | <span data-ttu-id="53fb5-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53fb5-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| \-                     | <span data-ttu-id="53fb5-119">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-119">x</span></span>    | <span data-ttu-id="53fb5-120">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-120">x</span></span>    | <span data-ttu-id="53fb5-121">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-121">x</span></span>    | <span data-ttu-id="53fb5-122">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-122">x</span></span>     | <span data-ttu-id="53fb5-123">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-123">x</span></span>    | <span data-ttu-id="53fb5-124">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-124">x</span></span>     |



 

## <a name="absolute-value"></a><span data-ttu-id="53fb5-125">Absoluter Wert</span><span class="sxs-lookup"><span data-stu-id="53fb5-125">Absolute Value</span></span>

<span data-ttu-id="53fb5-126">Nehmen Sie den absoluten Wert des Register.</span><span class="sxs-lookup"><span data-stu-id="53fb5-126">Take the absolute value of the register.</span></span>



| <span data-ttu-id="53fb5-127">Vertex-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="53fb5-127">Vertex shader versions</span></span> | <span data-ttu-id="53fb5-128">1\_1</span><span class="sxs-lookup"><span data-stu-id="53fb5-128">1\_1</span></span> | <span data-ttu-id="53fb5-129">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53fb5-129">2\_0</span></span> | <span data-ttu-id="53fb5-130">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="53fb5-130">2\_x</span></span> | <span data-ttu-id="53fb5-131">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53fb5-131">2\_sw</span></span> | <span data-ttu-id="53fb5-132">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="53fb5-132">3\_0</span></span> | <span data-ttu-id="53fb5-133">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="53fb5-133">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="53fb5-134">abs</span><span class="sxs-lookup"><span data-stu-id="53fb5-134">abs</span></span>                    |      |      |      |       | <span data-ttu-id="53fb5-135">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-135">x</span></span>    | <span data-ttu-id="53fb5-136">x</span><span class="sxs-lookup"><span data-stu-id="53fb5-136">x</span></span>     |



 

<span data-ttu-id="53fb5-137">Wenn ein Shader der Version 3 aus mindestens einem konstanten float-Register (c \# ) liest, muss einer der folgenden Werte zutreffen.</span><span class="sxs-lookup"><span data-stu-id="53fb5-137">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="53fb5-138">Alle Konstanten Gleit Komma Register müssen den ABS-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="53fb5-138">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="53fb5-139">Keines der Konstanten Gleit Komma Register kann den ABS-Modifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="53fb5-139">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53fb5-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="53fb5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53fb5-141">Vertex-Shader-registermodifiziererer</span><span class="sxs-lookup"><span data-stu-id="53fb5-141">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




