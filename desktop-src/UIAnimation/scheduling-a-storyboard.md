---
title: Planen eines Storyboards
description: Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.
ms.assetid: f3c8fe34-8bca-4421-a390-9e0ba9af27b4
keywords:
- Storyboards Windows-Animation, Planung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3feae253804d20711c9bbd8ed50895f43272a3f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036403"
---
# <a name="schedule-a-storyboard"></a><span data-ttu-id="a5f85-104">Planen eines Storyboards</span><span class="sxs-lookup"><span data-stu-id="a5f85-104">Schedule a Storyboard</span></span>

<span data-ttu-id="a5f85-105">Nachdem ein Storyboard erstellt wurde, wird es vom Animations-Manager geplant.</span><span class="sxs-lookup"><span data-stu-id="a5f85-105">After a storyboard is created, it is scheduled by the animation manager.</span></span>

## <a name="overview"></a><span data-ttu-id="a5f85-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="a5f85-106">Overview</span></span>

<span data-ttu-id="a5f85-107">Standardmäßig wird jedes Storyboard sofort nach der Planung gestartet.</span><span class="sxs-lookup"><span data-stu-id="a5f85-107">By default, each storyboard starts immediately when it is scheduled.</span></span> <span data-ttu-id="a5f85-108">Dies bedeutet, dass beim Starten einer oder mehrerer Variablen durch ein Storyboard möglicherweise alle anderen Storyboards, die dieselben Variablen animieren, unterbrochen werden.</span><span class="sxs-lookup"><span data-stu-id="a5f85-108">This means that when a storyboard starts to animate one or more variables, it may interrupt any other storyboards animating those same variables.</span></span> <span data-ttu-id="a5f85-109">Allerdings kann eine Anwendung andere Verhalten angeben, indem die relative Priorität zwischen Storyboards festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a5f85-109">However, an application may specify other behaviors by determining the relative priority between storyboards.</span></span>

<span data-ttu-id="a5f85-110">Nachdem ein Storyboard geplant wurde, kann es nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a5f85-110">After a storyboard has been scheduled, it can no longer be altered.</span></span> <span data-ttu-id="a5f85-111">Nachdem ein Storyboard aus dem Zeitplan entfernt wurde, kann es jedoch wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a5f85-111">However, after a storyboard has been removed from the schedule, it can be scheduled for play again.</span></span> <span data-ttu-id="a5f85-112">Entwickler sollten bei der erneuten Verwendung von Storyboards Vorsicht walten lassen, da dies nur dann der Fall sein sollte, wenn es nicht möglich ist, dass das gleiche Storyboard aufgrund einer Benutzeraktion in die Warteschlange eingereiht werden muss, wenn Sie bereits im Zeitplan vorhanden ist oder in die Warteschlange eingereiht wurde.</span><span class="sxs-lookup"><span data-stu-id="a5f85-112">Developers should exercise caution when re-using storyboards, as this should only be done where there is no chance that the same storyboard might need to be queued due to a user action when it is already playing or queued in the schedule.</span></span>

## <a name="example-code"></a><span data-ttu-id="a5f85-113">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="a5f85-113">Example Code</span></span>

<span data-ttu-id="a5f85-114">Der folgende Beispielcode stammt aus der Datei "MainWindow. cpp" in den Windows-Animations Beispielen [Anwendungs gesteuerte Animation](application-driven-animation-sample.md) und [Timer-gesteuerte Animation](timer-driven-animation-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a5f85-114">The following example code is taken from MainWindow.cpp in the Windows Animation samples [Application-Driven Animation](application-driven-animation-sample.md) and [Timer-Driven Animation](timer-driven-animation-sample.md).</span></span> <span data-ttu-id="a5f85-115">Er verwendet die [**iuianimationstoryboard:: Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) -Methode, um das Storyboard zu planen.</span><span class="sxs-lookup"><span data-stu-id="a5f85-115">It uses the [**IUIAnimationStoryboard::Schedule**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule) method to schedule the storyboard.</span></span> <span data-ttu-id="a5f85-116">Diese Methode erfordert die aktuelle Zeit als Parameter.</span><span class="sxs-lookup"><span data-stu-id="a5f85-116">This method requires the current time as a parameter.</span></span>


```
// Get the current time and schedule the storyboard for play

UI_ANIMATION_SECONDS secondsNow;
hr = m_pAnimationTimer->GetTime(
    &secondsNow
    );
if (SUCCEEDED(hr))
{
    hr = pStoryboard->Schedule(
        secondsNow
    );
}
```



## <a name="previous-step"></a><span data-ttu-id="a5f85-117">Vorheriger Schritt</span><span class="sxs-lookup"><span data-stu-id="a5f85-117">Previous Step</span></span>

<span data-ttu-id="a5f85-118">Bevor Sie mit diesem Schritt beginnen, sollten Sie diesen Schritt abgeschlossen haben: [Erstellen eines Storyboards und hinzufügen](updating---timer-driven-animation.md)von Übergängen.</span><span class="sxs-lookup"><span data-stu-id="a5f85-118">Before starting this step, you should have completed this step: [Create a Storyboard and Add Transitions](updating---timer-driven-animation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f85-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5f85-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f85-120">**Iuianimationstoryboard:: Schedule**</span><span class="sxs-lookup"><span data-stu-id="a5f85-120">**IUIAnimationStoryboard::Schedule**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-schedule)
</dt> <dt>

[<span data-ttu-id="a5f85-121">**Iuianimationtimer:: getTime**</span><span class="sxs-lookup"><span data-stu-id="a5f85-121">**IUIAnimationTimer::GetTime**</span></span>](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtimer-gettime)
</dt> <dt>

[<span data-ttu-id="a5f85-122">Übersicht über Storyboards</span><span class="sxs-lookup"><span data-stu-id="a5f85-122">Storyboard Overview</span></span>](storyboard-construction.md)
</dt> </dl>

 

 




