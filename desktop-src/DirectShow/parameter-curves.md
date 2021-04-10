---
description: Parameter Kurven
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Parameter Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125017"
---
# <a name="parameter-curves"></a><span data-ttu-id="56847-103">Parameter Kurven</span><span class="sxs-lookup"><span data-stu-id="56847-103">Parameter Curves</span></span>

<span data-ttu-id="56847-104">Medien Parameter können im Laufe der Zeit eine Kurve verfolgen.</span><span class="sxs-lookup"><span data-stu-id="56847-104">Media parameters are able to follow a curve over time.</span></span> <span data-ttu-id="56847-105">Jede Kurve wird durch eine mathematische Formel und zwei Endpunkte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="56847-105">Each curve is described by a mathematical formula and two end-points.</span></span> <span data-ttu-id="56847-106">Jeder Endpunkt wird durch eine Verweis Zeit und den Wert der Kurve zu diesem Zeitpunkt definiert.</span><span class="sxs-lookup"><span data-stu-id="56847-106">Each end-point is defined by a reference time and the value of the curve at that time.</span></span> <span data-ttu-id="56847-107">Die Formel wird verwendet, um Zwischenwerte zwischen den Punkten zu berechnen, und bestimmt die Form der Kurve.</span><span class="sxs-lookup"><span data-stu-id="56847-107">The formula is used to calculate intermediate values between the points, and determines the shape of the curve.</span></span> <span data-ttu-id="56847-108">Mögliche Kurven:</span><span class="sxs-lookup"><span data-stu-id="56847-108">The possible curves are:</span></span>

-   <span data-ttu-id="56847-109">Gelenks</span><span class="sxs-lookup"><span data-stu-id="56847-109">Jump</span></span>
-   <span data-ttu-id="56847-110">Linear</span><span class="sxs-lookup"><span data-stu-id="56847-110">Linear</span></span>
-   <span data-ttu-id="56847-111">Square</span><span class="sxs-lookup"><span data-stu-id="56847-111">Square</span></span>
-   <span data-ttu-id="56847-112">Umgekehrtes Quadrat</span><span class="sxs-lookup"><span data-stu-id="56847-112">Inverse square</span></span>
-   <span data-ttu-id="56847-113">Ston</span><span class="sxs-lookup"><span data-stu-id="56847-113">Sine</span></span>

<span data-ttu-id="56847-114">"Jump" bedeutet, dass Sie direkt zum Endwert springen.</span><span class="sxs-lookup"><span data-stu-id="56847-114">"Jump" means jump directly to the end value.</span></span> <span data-ttu-id="56847-115">Die anderen Kurven werden im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56847-115">The other curves are shown in the following diagram.</span></span>

![Parameter Kurven](images/param-curves01.png)

<span data-ttu-id="56847-117">Die Kurven funktionieren mathematisch wie folgt.</span><span class="sxs-lookup"><span data-stu-id="56847-117">Mathematically, the curves work as follows.</span></span> <span data-ttu-id="56847-118">Angenommen, eine Kurve beginnt bei Time *t*₀ mit dem Wert *v*₀ und endet mit Time *t*₁ mit dem Wert *v*₁.</span><span class="sxs-lookup"><span data-stu-id="56847-118">Suppose that a curve begins at time *t*₀ with a value of *v*₀, and ends at time *t*₁ with a value of *v*₁.</span></span> <span data-ttu-id="56847-119">Die beiden Punkte, die die Kurve definieren, sind (*t*₀, *v*₀) und (*t*₁, *v*₁).</span><span class="sxs-lookup"><span data-stu-id="56847-119">The two points that define the curve are (*t*₀, *v*₀) and (*t*₁, *v*₁).</span></span>

-   <span data-ttu-id="56847-120">Legen Sie die Gesamtdauer der Kurve ( *t*₁ –*t*₀) ab.</span><span class="sxs-lookup"><span data-stu-id="56847-120">Let Δ *t* be the total duration of the curve, *t*₁–*t*₀.</span></span>
-   <span data-ttu-id="56847-121">*Lassen Sie* das Intervall zwischen den Anfangs-und Endwerten *v*₁ –*v*₀.</span><span class="sxs-lookup"><span data-stu-id="56847-121">Let Δ *v* be the interval between the starting and ending values, *v*₁–*v*₀.</span></span>
-   <span data-ttu-id="56847-122">Zu einem beliebigen Zeitpunkt *t* , d. ₀. *t*<= *t*  <=  *t*₁, lassen Sie *t*' = t –*t*₀.</span><span class="sxs-lookup"><span data-stu-id="56847-122">At any time *t* such that *t*₀ <= *t* <= *t*₁, let Δ *t*' = *t*–*t*₀.</span></span>

![Parameter Berechnung](images/param-curves02.png)

<span data-ttu-id="56847-124">Der Wert des-Parameters zum Zeitpunkt *t* ist:</span><span class="sxs-lookup"><span data-stu-id="56847-124">The value of the parameter at time *t* is:</span></span>

<span data-ttu-id="56847-125">*v* = f (,*t*"/-*t* ) Version v \*   +  *v*₀</span><span class="sxs-lookup"><span data-stu-id="56847-125">*v* = f( Δ *t*' / Δ *t* ) \* Δ *v* + *v*₀</span></span>

<span data-ttu-id="56847-126">Dabei ist f (x) eine Funktion, die durch den Kurven-Typ bestimmt wird:</span><span class="sxs-lookup"><span data-stu-id="56847-126">where f(x) is a function determined by the curve type:</span></span>

-   <span data-ttu-id="56847-127">Linear: y = x</span><span class="sxs-lookup"><span data-stu-id="56847-127">Linear: y = x</span></span>
-   <span data-ttu-id="56847-128">Quadrat: y = x ^ 2</span><span class="sxs-lookup"><span data-stu-id="56847-128">Square: y = x^2</span></span>
-   <span data-ttu-id="56847-129">Umgekehrtes Quadrat: y = sqrt (x)</span><span class="sxs-lookup"><span data-stu-id="56847-129">Inverse square: y = sqrt(x)</span></span>
-   <span data-ttu-id="56847-130">Sinus: y = \[ Sin (-x – μ/2) + 1 \] /2</span><span class="sxs-lookup"><span data-stu-id="56847-130">Sine: y = \[ sin(πx – π/2) + 1 \] / 2</span></span>

<span data-ttu-id="56847-131">Beachten Sie,*dass "<-t"* lautet, sodass der Begriff "-*t"/*"*t* " zwischen 0 und *1 liegt.*</span><span class="sxs-lookup"><span data-stu-id="56847-131">Observe that Δ *t*' < Δ *t*, so the term Δ *t*'/Δ *t* ranges from 0 to 1.</span></span> <span data-ttu-id="56847-132">Daher liegt f (x) auch zwischen 0 und 1, und *v* liegt immer zwischen *v*₀ und *v*₁.</span><span class="sxs-lookup"><span data-stu-id="56847-132">Therefore, f(x) also ranges from 0 to 1, and *v* always falls between *v*₀ and *v*₁.</span></span> <span data-ttu-id="56847-133">Dies gilt unabhängig davon, ob *v*₀ < *v*₁ oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="56847-133">This is true whether *v*₀ < *v*₁ or vice versa.</span></span> <span data-ttu-id="56847-134">Das heißt, die Kurve wird durch das Rechteck (*t*₀, *v*₀, *t*₁, *v*₁) begrenzt.</span><span class="sxs-lookup"><span data-stu-id="56847-134">In other words, the curve is bounded by the rectangle (*t*₀, *v*₀, *t*₁, *v*₁).</span></span>

<span data-ttu-id="56847-135">Bei der Sinuskurve reicht der Wert von ("– x)/2" von "–./2" zu "-/2". Dies bedeutet, dass sich der Wert von "Sin (-x – μ/2)" von "– 1 bis 1" erstreckt.</span><span class="sxs-lookup"><span data-stu-id="56847-135">For the sine curve, the value of (πx – π/2) ranges from –π/2 to π/2, which means that sin(πx – π/2) ranges from –1 to 1.</span></span> <span data-ttu-id="56847-136">Das Ergebnis wird dann normalisiert, sodass f (x) in den Bereich (0 – 1) fällt.</span><span class="sxs-lookup"><span data-stu-id="56847-136">The result is then normalized so that f(x) falls into the range (0–1).</span></span>

## <a name="related-topics"></a><span data-ttu-id="56847-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56847-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56847-138">Medien Parameter</span><span class="sxs-lookup"><span data-stu-id="56847-138">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



