---
title: Temporäres Register (HLSL PS-Referenz)
description: Temporäre Register der Pixel-Shader-Eingabe werden verwendet, um Zwischenergebnisse zu speichern.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857831"
---
# <a name="temporary-register-hlsl-ps-reference"></a><span data-ttu-id="5b80c-103">Temporäres Register (HLSL PS-Referenz)</span><span class="sxs-lookup"><span data-stu-id="5b80c-103">Temporary register (HLSL PS reference)</span></span>

<span data-ttu-id="5b80c-104">Temporäre Register der Pixel-Shader-Eingabe werden verwendet, um Zwischenergebnisse zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5b80c-104">Pixel shader input temporary registers are used to hold intermediate results.</span></span>

<span data-ttu-id="5b80c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b80c-105">Syntax</span></span>


```
no declaration is required
```





| <span data-ttu-id="5b80c-106">Pixel-Shader-Versionen</span><span class="sxs-lookup"><span data-stu-id="5b80c-106">Pixel shader versions</span></span> | <span data-ttu-id="5b80c-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="5b80c-107">1\_1</span></span> | <span data-ttu-id="5b80c-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="5b80c-108">1\_2</span></span> | <span data-ttu-id="5b80c-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5b80c-109">1\_3</span></span> | <span data-ttu-id="5b80c-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="5b80c-110">1\_4</span></span> | <span data-ttu-id="5b80c-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b80c-111">2\_0</span></span> | <span data-ttu-id="5b80c-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b80c-112">2\_sw</span></span> | <span data-ttu-id="5b80c-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5b80c-113">2\_x</span></span> | <span data-ttu-id="5b80c-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5b80c-114">3\_0</span></span> | <span data-ttu-id="5b80c-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5b80c-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| <span data-ttu-id="5b80c-116">Temporäres Register</span><span class="sxs-lookup"><span data-stu-id="5b80c-116">Temporary Register</span></span>    |      |      |      |      | <span data-ttu-id="5b80c-117">x</span><span class="sxs-lookup"><span data-stu-id="5b80c-117">x</span></span>    | <span data-ttu-id="5b80c-118">x</span><span class="sxs-lookup"><span data-stu-id="5b80c-118">x</span></span>     | <span data-ttu-id="5b80c-119">x</span><span class="sxs-lookup"><span data-stu-id="5b80c-119">x</span></span>    | <span data-ttu-id="5b80c-120">x</span><span class="sxs-lookup"><span data-stu-id="5b80c-120">x</span></span>    | <span data-ttu-id="5b80c-121">x</span><span class="sxs-lookup"><span data-stu-id="5b80c-121">x</span></span>     |



 

-   <span data-ttu-id="5b80c-122">Es gibt 12 Pixel-Shader-temporäre Register: R0 bis R11.</span><span class="sxs-lookup"><span data-stu-id="5b80c-122">There are 12 pixel-shader temporary registers: r0 to r11.</span></span>
-   <span data-ttu-id="5b80c-123">Diese Register werden zum Speichern von Zwischenergebnissen während Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5b80c-123">These registers are used for storing intermediate results during computations.</span></span>
-   <span data-ttu-id="5b80c-124">Wenn für ein temporäres Register Komponenten verwendet werden, die nicht im vorherigen Code definiert sind, tritt bei der shadervalidierung ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="5b80c-124">If a temporary register uses components that are not defined in previous code, shader validation will fail.</span></span>
-   <span data-ttu-id="5b80c-125">Dabei handelt es sich um mindestens eine Gleit Komma Genauigkeit.</span><span class="sxs-lookup"><span data-stu-id="5b80c-125">These are at least floating-point precision.</span></span>
-   <span data-ttu-id="5b80c-126">In einer einzelnen Anweisung können maximal drei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b80c-126">A maximum of three can be used in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b80c-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b80c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b80c-128">Register</span><span class="sxs-lookup"><span data-stu-id="5b80c-128">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




