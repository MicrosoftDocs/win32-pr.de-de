---
title: Die Funktionalität der Desktop-App ist beeinträchtigt, wenn Sie nicht im Fenstermodus ausgeführt wird.
description: In Windows 10 sind Windows-apps nicht mehr standardmäßig voll Bild fähig – stattdessen sind Sie Fenster und Vorgänge wie das minimieren, wiederherstellen, maximieren und Ändern der Größe (und jeder andere Vorgang, den Sie immer in einem anderen klassischen Windows-Anwendungsfenster ausführen konnten) sind jetzt möglich.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388591"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="77819-103">Die Funktionalität der Desktop-App ist beeinträchtigt, wenn Sie nicht im Fenstermodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77819-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="77819-104">In Windows 10 sind Windows-apps nicht mehr standardmäßig voll Bild fähig – stattdessen sind Sie Fenster und Vorgänge wie das minimieren, wiederherstellen, maximieren und Ändern der Größe (und jeder andere Vorgang, den Sie immer in einem anderen klassischen Windows-Anwendungsfenster ausführen konnten) sind jetzt möglich.</span><span class="sxs-lookup"><span data-stu-id="77819-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="77819-105">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="77819-105">Manifestations</span></span>

<span data-ttu-id="77819-106">Die auffälligste Änderung ist nun, dass Sie Größe beliebig groß machen können, die nicht nur die Größe des Bildschirms bzw. der Höhe des Bildschirms ist.</span><span class="sxs-lookup"><span data-stu-id="77819-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="77819-107">Ein Benutzer kann die Größe des App-Fensters kontinuierlich anpassen (bis zur minimalen Fenstergröße der APP).</span><span class="sxs-lookup"><span data-stu-id="77819-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="77819-108">Dies unterscheidet sich von Windows 8,0 oder Windows 8.1, bei dem das Ändern der Größe eines Fensters eine diskrete Aktion war (die Benutzer haben eine Miniaturansicht des Fensters geändert, wodurch sich die Größe des Fensters geändert hat, nachdem der Benutzer die Aktion committet hat).</span><span class="sxs-lookup"><span data-stu-id="77819-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="77819-109">Heutzutage ist es eine kontinuierliche Größenänderung, wenn der Benutzer das Fenster in der unteren Ecke (oder an einer anderen Rahmen Position) zieht, und die APP erhält Größen Änderungs Nachrichten in einer Zeile und nicht in einer Größenänderung.</span><span class="sxs-lookup"><span data-stu-id="77819-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="77819-110">Gegenmaßnahmen</span><span class="sxs-lookup"><span data-stu-id="77819-110">Mitigations</span></span>

<span data-ttu-id="77819-111">So mindern Sie dieses Problem für Windows 8,0-und 8,1-apps:</span><span class="sxs-lookup"><span data-stu-id="77819-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="77819-112">Wenn die erwartete Funktion innerhalb der APP-Funktionalität beschädigt ist, besteht die Benutzer Entschärfung darin, die app in den Vollbildmodus zu versetzen (mithilfe der Schaltfläche "Vollbild wechseln" in der oberen rechten Ecke der Titelleiste).</span><span class="sxs-lookup"><span data-stu-id="77819-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="77819-113">Wenn die APP-Start Anleitung davon betroffen ist, dass Sie nicht erwartungsgemäß geöffnet ist, sollte der Benutzer dennoch in der Lage sein, in den Tablet-Modus zu wechseln, um zu erzwingen, dass die APP im Vollbildmodus ohne Benutzereingriff gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="77819-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="77819-114">Die beste Möglichkeit, dies zu handhaben, besteht darin, die APP so zu ändern, dass Sie die Größe der Größen und Höhen von nicht überwachten Größen (d. h. nicht über eine hart codierte Tabelle mit Höhe/Breite verfügt und diese nur erwartet oder hart codierte Verhältnisse erwartet).</span><span class="sxs-lookup"><span data-stu-id="77819-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="77819-115">App-Entwickler sollten davon ausgehen, dass bei der Größenänderung der App eine andere Nachricht zum Ändern der Größe direkt nach dem übermitteln der aktuellen Größenänderung auftreten kann – wenn die APP während der Größenänderung Animationen startet, kann die APP möglicherweise eine andere Nachricht zum Ändern der Größe erhalten (daher ist es wichtig sicherzustellen, dass diese Art von Situation nicht zum Absturz der APP führt).</span><span class="sxs-lookup"><span data-stu-id="77819-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




