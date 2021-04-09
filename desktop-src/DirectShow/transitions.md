---
description: Transitions
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868263"
---
# <a name="transitions"></a><span data-ttu-id="7045a-103">Transitions</span><span class="sxs-lookup"><span data-stu-id="7045a-103">Transitions</span></span>

<span data-ttu-id="7045a-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="7045a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="7045a-105">Mithilfe eines visuellen Effekts, wie z. b. ein ausblenden oder ein Zurücksetzen, kann ein Übergang von einer Videospur zu einer anderen durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="7045a-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="7045a-106">Die folgende Abbildung zeigt eine Zeitachse mit einem Übergang:</span><span class="sxs-lookup"><span data-stu-id="7045a-106">The following illustration shows a timeline with a transition:</span></span>

![Zeitachse mit Übergang](images/timeline3.png)

<span data-ttu-id="7045a-108">Das Übergangs Objekt befindet sich auf der Spur 1 und stellt einen Übergang von der Spur 0 zur Nachverfolgung 1 dar.</span><span class="sxs-lookup"><span data-stu-id="7045a-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="7045a-109">Zu Beginn des Übergangs ist das gerenderte Video vollständig von Track 0 (Quelle A).</span><span class="sxs-lookup"><span data-stu-id="7045a-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="7045a-110">Am Ende ist das Video vollständig von Track 1 (Quelle C).</span><span class="sxs-lookup"><span data-stu-id="7045a-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="7045a-111">Dazwischen geht die Ausgabe von Quelle A in Quelle C über. Beispielsweise wird bei einem Fade-Übergang eine Quelle progressiv zum anderen.</span><span class="sxs-lookup"><span data-stu-id="7045a-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="7045a-112">Die endgültige Ausgabe wird am Ende der Abbildung schematisiert.</span><span class="sxs-lookup"><span data-stu-id="7045a-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="7045a-113">Übergänge können sich nicht innerhalb desselben Titels zeitlich überlappen, Sie können jedoch überlappende Übergänge erstellen, indem Sie das Kompositions Objekt verwenden, wie unter [Komposition und Layering](composition-and-layering.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7045a-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="7045a-114">Ein Übergang weist eine Richtung auf.</span><span class="sxs-lookup"><span data-stu-id="7045a-114">A transition has a direction.</span></span> <span data-ttu-id="7045a-115">Standardmäßig beginnt Sie mit dem Titel mit niedrigerer Priorität (Quelle A im vorherigen Beispiel) und endet mit der Spur mit höherer Priorität (Quelle C).</span><span class="sxs-lookup"><span data-stu-id="7045a-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="7045a-116">Zwischen und besteht das Video aus einer Mischung aus den beiden Quellen.</span><span class="sxs-lookup"><span data-stu-id="7045a-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="7045a-117">Sie können jedoch das Gegenteil Verhalten angeben, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7045a-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![ntrack mit zwei Übergängen](images/fade.png)

<span data-ttu-id="7045a-119">An dieser Stelle wird der erste Übergang von der Spur 0 verblasst Nachverfolgung 1. Dies ist das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="7045a-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="7045a-120">Der zweite Übergang wird von der Nachverfolgung 1 zurück zur Nachverfolgung 0.</span><span class="sxs-lookup"><span data-stu-id="7045a-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="7045a-121">Beachten Sie, dass sich beide Übergänge auf Track 1 befinden.</span><span class="sxs-lookup"><span data-stu-id="7045a-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7045a-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7045a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7045a-123">Einführung in DirectShow-Bearbeitungs Dienste</span><span class="sxs-lookup"><span data-stu-id="7045a-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="7045a-124">Übergänge und Effekte</span><span class="sxs-lookup"><span data-stu-id="7045a-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="7045a-125">Arbeiten mit Effekten und Übergängen</span><span class="sxs-lookup"><span data-stu-id="7045a-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



