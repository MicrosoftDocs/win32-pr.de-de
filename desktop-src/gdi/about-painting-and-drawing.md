---
description: Fast alle Anwendungen verwenden den Bildschirm, um die Daten anzuzeigen, die Sie bearbeiten.
ms.assetid: 97d606a0-11d3-49c3-b045-8397f4bcfa54
title: Informationen zum Zeichnen und zeichnen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb8ffa5b5c842dcd12d57967f2c20de0391824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993862"
---
# <a name="about-painting-and-drawing"></a><span data-ttu-id="59cb7-103">Informationen zum Zeichnen und zeichnen</span><span class="sxs-lookup"><span data-stu-id="59cb7-103">About Painting and Drawing</span></span>

<span data-ttu-id="59cb7-104">Fast alle Anwendungen verwenden den Bildschirm, um die Daten anzuzeigen, die Sie bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="59cb7-104">Nearly all applications use the screen to display the data they manipulate.</span></span> <span data-ttu-id="59cb7-105">Eine Anwendung zeichnet Bilder, zeichnet Abbildungen und schreibt Text, sodass der Benutzerdaten anzeigen kann, während er erstellt, bearbeitet und gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="59cb7-105">An application paints images, draws figures, and writes text so that the user can view data as it is created, edited, and printed.</span></span> <span data-ttu-id="59cb7-106">Microsoft Windows bietet umfassende Unterstützung für das Zeichnen und zeichnen, aber aufgrund der Art der Multitasking-Betriebssysteme müssen Anwendungen beim Zugriff auf den Bildschirm miteinander zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="59cb7-106">Microsoft Windows provides rich support for painting and drawing, but, because of the nature of multitasking operating systems, applications must cooperate with one another when accessing the screen.</span></span>

<span data-ttu-id="59cb7-107">Damit alle Anwendungen reibungslos und kooperativ funktionieren, verwaltet das System alle Ausgaben auf dem Bildschirm.</span><span class="sxs-lookup"><span data-stu-id="59cb7-107">To keep all applications functioning smoothly and cooperatively, the system manages all output to the screen.</span></span> <span data-ttu-id="59cb7-108">Anwendungen verwenden Windows als das primäre Ausgabegerät anstelle des Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="59cb7-108">Applications use windows as their primary output device rather than the screen itself.</span></span> <span data-ttu-id="59cb7-109">Die System Bereitstellung zeigt Geräte Kontexte an, die den Fenstern eindeutig entsprechen.</span><span class="sxs-lookup"><span data-stu-id="59cb7-109">The system supplies display device contexts that uniquely correspond to the windows.</span></span> <span data-ttu-id="59cb7-110">Anwendungen verwenden Anzeigegeräte Kontexte, um die Ausgabe an die angegebenen Fenster weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="59cb7-110">Applications use display device contexts to direct their output to the specified windows.</span></span> <span data-ttu-id="59cb7-111">Das Zeichnen in einem Fenster (Weiterleiten der Ausgabe) hindert eine Anwendung daran, die Ausgabe anderer Anwendungen zu beeinträchtigen, und ermöglicht es, Anwendungen untereinander zu koexistieren, während die Grafikfunktionen des Systems weiterhin vollständig genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="59cb7-111">Drawing in a window (directing output to it) prevents an application from interfering with the output of other applications and allows applications to coexist with one another while still taking full advantage of the graphics capabilities of the system.</span></span>

-   [<span data-ttu-id="59cb7-112">Wann in einem Fenster gezeichnet werden soll</span><span class="sxs-lookup"><span data-stu-id="59cb7-112">When to Draw in a Window</span></span>](when-to-draw-in-a-window.md)
-   [<span data-ttu-id="59cb7-113">Die WM-Zeichnungs \_ Meldung</span><span class="sxs-lookup"><span data-stu-id="59cb7-113">The WM\_PAINT Message</span></span>](the-wm-paint-message.md)
-   [<span data-ttu-id="59cb7-114">Zeichnen ohne die WM-Zeichnungs \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="59cb7-114">Drawing Without the WM\_PAINT Message</span></span>](drawing-without-the-wm-paint-message.md)
-   [<span data-ttu-id="59cb7-115">Fenster Koordinaten System</span><span class="sxs-lookup"><span data-stu-id="59cb7-115">Window Coordinate System</span></span>](window-coordinate-system.md)
-   [<span data-ttu-id="59cb7-116">Fensterbereiche</span><span class="sxs-lookup"><span data-stu-id="59cb7-116">Window Regions</span></span>](window-regions.md)
-   [<span data-ttu-id="59cb7-117">Fenster Hintergrund</span><span class="sxs-lookup"><span data-stu-id="59cb7-117">Window Background</span></span>](window-background.md)
-   [<span data-ttu-id="59cb7-118">Minimierte Fenster</span><span class="sxs-lookup"><span data-stu-id="59cb7-118">Minimized Windows</span></span>](minimized-windows.md)
-   [<span data-ttu-id="59cb7-119">Fenstergröße geändert</span><span class="sxs-lookup"><span data-stu-id="59cb7-119">Resized Windows</span></span>](resized-windows.md)
-   [<span data-ttu-id="59cb7-120">Nicht-Client Bereich</span><span class="sxs-lookup"><span data-stu-id="59cb7-120">Nonclient Area</span></span>](nonclient-area.md)
-   [<span data-ttu-id="59cb7-121">Aktualisierungs Bereich des untergeordneten Fensters</span><span class="sxs-lookup"><span data-stu-id="59cb7-121">Child Window Update Region</span></span>](child-window-update-region.md)
-   [<span data-ttu-id="59cb7-122">Geräte anzeigen</span><span class="sxs-lookup"><span data-stu-id="59cb7-122">Display Devices</span></span>](display-devices.md)
-   [<span data-ttu-id="59cb7-123">Fenster Update Sperre</span><span class="sxs-lookup"><span data-stu-id="59cb7-123">Window Update Lock</span></span>](window-update-lock.md)
-   [<span data-ttu-id="59cb7-124">Akkumuliertes Rechteck</span><span class="sxs-lookup"><span data-stu-id="59cb7-124">Accumulated Bounding Rectangle</span></span>](accumulated-bounding-rectangle.md)

 

 



