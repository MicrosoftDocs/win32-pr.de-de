---
title: Desktopfenster-Manager
description: Das in Windows Vista eingeführte Feature "Desktop Komposition" hat grundlegend geändert, wie Anwendungen auf dem Bildschirm Pixel anzeigen.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Desktopfenster-Manager (DWM), Informationen zu
- Dwm (Desktopfenster-Manager), Informationen zu
- Desktopfenster-Manager (DWM), Komposition
- Dwm (Desktopfenster-Manager), Komposition
- Desktop Komposition
- Komposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711190"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="3cdbc-109">Desktopfenster-Manager</span><span class="sxs-lookup"><span data-stu-id="3cdbc-109">Desktop Window Manager</span></span>

<span data-ttu-id="3cdbc-110">Das in Windows Vista eingeführte Feature "Desktop Komposition" hat grundlegend geändert, wie Anwendungen auf dem Bildschirm Pixel anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="3cdbc-111">Wenn die Desktop Komposition aktiviert ist, werden einzelne Fenster nicht mehr direkt auf den Bildschirm oder das primäre Anzeigegerät gezeichnet, wie dies in früheren Versionen von Windows der Fall war.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="3cdbc-112">Stattdessen wird die Zeichenfolge in den Videospeicher, der in einem Desktop Bild gerendert und auf der Anzeige angezeigt wird, zu den Bildschirm Oberflächen umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="3cdbc-113">Die Desktop Komposition wird vom Desktopfenster-Manager (DWM) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="3cdbc-114">Durch die Desktop Komposition ermöglicht DWM visuelle Effekte auf dem Desktop sowie verschiedene Funktionen wie z. b. Glasfenster Rahmen, 3-D-Fenster Übergangs Animationen, Windows Flip-und Windows Flip3D-Unterstützung und Unterstützung für hohe Auflösung.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="3cdbc-115">Der Desktopfenster-Manager wird als Windows-Dienst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="3cdbc-116">Sie kann über das System Steuerungselement "Verwaltung" unter "Dienste" als Desktopfenster-Manager Sitzungs-Manager aktiviert und deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="3cdbc-117">Viele der DWM-Features können über die DWM-APIs gesteuert oder von einer Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="3cdbc-118">In der folgenden Dokumentation werden die Features und Anforderungen der DWM-APIs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3cdbc-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="3cdbc-119">DWM-Übersichten</span><span class="sxs-lookup"><span data-stu-id="3cdbc-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="3cdbc-120">DWM-Beispiel Code</span><span class="sxs-lookup"><span data-stu-id="3cdbc-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="3cdbc-121">DWM-Referenz</span><span class="sxs-lookup"><span data-stu-id="3cdbc-121">DWM Reference</span></span>](reference.md)

 

 




