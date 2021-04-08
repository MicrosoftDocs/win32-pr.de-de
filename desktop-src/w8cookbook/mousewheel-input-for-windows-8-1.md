---
title: Mouswheel-Eingabe für Windows 8.1
description: Mouswheel-Eingabe für Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855811"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="dc250-103">Mouswheel-Eingabe für Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dc250-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="dc250-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="dc250-104">Platform</span></span>

<dl> <span data-ttu-id="dc250-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dc250-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="dc250-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="dc250-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="dc250-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc250-107">Description</span></span>

<span data-ttu-id="dc250-108">In Windows 8.1 werden mouserwheel-Ereignisse nicht mehr basierend auf dem Tastaturfokus wie in früheren Windows-Versionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dc250-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="dc250-109">Wenn in Windows 8.1 der Mauszeiger auf eine Store-App zeigt, wird Mausrad an diese APP übermittelt. aus Kompatibilitätsgründen wird Mausrad jedoch weiterhin basierend auf dem Tastaturfokus übermittelt, wenn der Mauszeiger auf eine Desktop-App zeigt.</span><span class="sxs-lookup"><span data-stu-id="dc250-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="dc250-110">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="dc250-110">Manifestations</span></span>

<span data-ttu-id="dc250-111">Wenn die Maus über Store-Apps bewegt wird, führt Mausrad einen Bildlauf für alle anwendbaren Inhalte durch, ohne dass der Benutzer auf die Store-App klicken muss.</span><span class="sxs-lookup"><span data-stu-id="dc250-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="dc250-112">Dies gilt auch für den Startbildschirm.</span><span class="sxs-lookup"><span data-stu-id="dc250-112">This also applies to the start screen.</span></span> <span data-ttu-id="dc250-113">Dadurch wird das Scrollen durch mouswheel zu einer einfacheren Interaktion in Windows 8.1 als in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dc250-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="dc250-114">Minderung</span><span class="sxs-lookup"><span data-stu-id="dc250-114">Mitigation</span></span>

<span data-ttu-id="dc250-115">Zum größten Teil sollte diese Änderung keine Auswirkungen auf vorhandene apps haben.</span><span class="sxs-lookup"><span data-stu-id="dc250-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="dc250-116">Wenn eine Store-App nur nach dem Registrieren eines Mausklicks auf Mausrad-Ereignisse lauscht, würde diese APP wahrscheinlich nicht auf Mausrad Antworten, bis der Benutzer Sie aktiv geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="dc250-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="dc250-117">Folglich besteht der wahrscheinlichste Nachteil darin, dass eine APP weiterhin genauso funktioniert wie in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dc250-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="dc250-118">Bei Desktop-Apps wird der APP mit dem Tastaturfokus nicht mehr ein Monopol über Mausrad-Eingaben erteilt, aber auch diese apps werden nicht in irgendeiner Weise unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc250-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="dc250-119">Es sind also keine kurzfristigen Maßnahmen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc250-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="dc250-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="dc250-120">Solution</span></span>

<span data-ttu-id="dc250-121">Entwickler von Store-Apps sollten mit dem Empfang von Mausrad-Ereignissen ohne ein gedrückter Mausklicks rechnen.</span><span class="sxs-lookup"><span data-stu-id="dc250-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="dc250-122">Sie sollten z. b. nur nach dem Registrieren eines Mausklicks auf Mausrad-Ereignisse lauschen.</span><span class="sxs-lookup"><span data-stu-id="dc250-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="dc250-123">Ebenso sollten Desktop Anwendungen nicht versuchen, Mausrad-Ereignisse zu erfassen (z. b. durch Festlegen eines Hooks auf niedriger Ebene), wenn Sie den Tastaturfokus haben.</span><span class="sxs-lookup"><span data-stu-id="dc250-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="dc250-124">Tests</span><span class="sxs-lookup"><span data-stu-id="dc250-124">Tests</span></span>

<span data-ttu-id="dc250-125">Store-App-Entwickler sollten sich auf Windows 8.1 testen, um zu überprüfen, ob alle scrollfunktionen funktionieren, wenn der Mauszeiger über die APP bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="dc250-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="dc250-126">Entwickler von Desktop-Apps sollten auf Windows 8.1 testen, um sicherzustellen, dass Sie keine Mausrad-Ereignisse erfassen (pro Leitfaden oben).</span><span class="sxs-lookup"><span data-stu-id="dc250-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 




