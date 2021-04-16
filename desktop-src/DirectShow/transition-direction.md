---
description: Übergangs Richtung
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Übergangs Richtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553564"
---
# <a name="transition-direction"></a><span data-ttu-id="bbcc6-103">Übergangs Richtung</span><span class="sxs-lookup"><span data-stu-id="bbcc6-103">Transition Direction</span></span>

<span data-ttu-id="bbcc6-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="bbcc6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="bbcc6-105">Ein Übergang wechselt von Eingabe a zu Eingabe B und von time t ₀ zu t ₁.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="bbcc6-106">Daher kann die *Richtung* eines Übergangs eine von zwei Faktoren bedeuten:</span><span class="sxs-lookup"><span data-stu-id="bbcc6-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="bbcc6-107">Die Zuordnung von Zeitachsen Ebenen zu Eingaben.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="bbcc6-108">Der Fortschritt im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-108">The progression over time.</span></span>

<span data-ttu-id="bbcc6-109">Der erste ist die *Eingabe Richtung*, die zweite ist die Status *Richtung*.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="bbcc6-110">Beide Richtungen können gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-110">You can control both directions.</span></span>

-   <span data-ttu-id="bbcc6-111">Eingabe Richtung: Standardmäßig geht ein Übergang von der zusammengesetzten der Ebenen mit niedrigerer Priorität zur Ebene, die den Übergang enthält.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="bbcc6-112">Um diese Richtung umzukehren, nennen Sie die [**iamtimelinetrans:: setionwapinputs**](iamtimelinetrans-setswapinputs.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="bbcc6-113">Fortschritts Richtung: die meisten Übergänge unterstützen **eine Standardstatus** Eigenschaft, die angibt, welcher Prozentsatz des Übergangs in der Ausgabe zu einem bestimmten Zeitpunkt reflektiert wird.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="bbcc6-114">Standardmäßig geht der **Wert der Status-Eigenschaft während** der Übergangs Dauer von 0,0 auf 1,0.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="bbcc6-115">Um den Fortschritt umzukehren, legen Sie die Status **-Eigenschaft auf** Go von 1,0 auf 0,0 fest.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="bbcc6-116">Im folgenden Diagramm wird der Unterschied zwischen Eingabe Richtung und Fortschritt Richtung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="bbcc6-117">Es zeigt vier Abweichungen bei einem standardmäßigen [SMPTE](smpte-wipe-transition.md) -Umleitungs Übergang.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![Anweisungen zum Löschen](images/wipedirections.png)

<span data-ttu-id="bbcc6-119">Der Übergang befindet sich auf der Spur 1.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-119">The transition resides on track 1.</span></span> <span data-ttu-id="bbcc6-120">Standardmäßig wechselt die zurück Löschung von links nach rechts und von Track 0 zur Nachverfolgung 1.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="bbcc6-121">Das Austauschen von Eingaben bewirkt, dass die zurück Löschung von der Spur 1 zur Nachverfolgung von 0, aber von links nach rechts, ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="bbcc6-122">Wenn Sie den Fortschritt umkehren, wechselt der Übergang von rechts nach links.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="bbcc6-123">Sie können beides kombinieren, wie in der linken Abbildung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="bbcc6-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="bbcc6-124">Weitere Informationen zum Rendern von Übergängen durch des finden Sie [im Zeitachsen Modell](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="bbcc6-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbcc6-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbcc6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbcc6-126">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="bbcc6-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



