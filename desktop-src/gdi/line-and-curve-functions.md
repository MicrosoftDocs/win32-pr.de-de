---
description: Die folgenden Funktionen werden bei Linien und Kurven verwendet.
ms.assetid: 90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b
title: Linien-und Kurven Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7bf04160e8b9cc0a5c2fb28378bce82a1c7650a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993943"
---
# <a name="line-and-curve-functions"></a><span data-ttu-id="c342c-103">Linien-und Kurven Funktionen</span><span class="sxs-lookup"><span data-stu-id="c342c-103">Line and Curve Functions</span></span>

<span data-ttu-id="c342c-104">Die folgenden Funktionen werden bei Linien und Kurven verwendet.</span><span class="sxs-lookup"><span data-stu-id="c342c-104">The following functions are used with lines and curves.</span></span>



| <span data-ttu-id="c342c-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="c342c-105">Function</span></span>                                   | <span data-ttu-id="c342c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c342c-106">Description</span></span>                                                                                                   |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c342c-107">**Anglearc**</span><span class="sxs-lookup"><span data-stu-id="c342c-107">**AngleArc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)               | <span data-ttu-id="c342c-108">Zeichnet ein Liniensegment und einen Bogen.</span><span class="sxs-lookup"><span data-stu-id="c342c-108">Draws a line segment and an arc.</span></span>                                                                              |
| [<span data-ttu-id="c342c-109">**Arc**</span><span class="sxs-lookup"><span data-stu-id="c342c-109">**Arc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arc)                         | <span data-ttu-id="c342c-110">Zeichnet einen elliptischen Bogen.</span><span class="sxs-lookup"><span data-stu-id="c342c-110">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="c342c-111">**ArcTo**</span><span class="sxs-lookup"><span data-stu-id="c342c-111">**ArcTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-arcto)                     | <span data-ttu-id="c342c-112">Zeichnet einen elliptischen Bogen.</span><span class="sxs-lookup"><span data-stu-id="c342c-112">Draws an elliptical arc.</span></span>                                                                                      |
| [<span data-ttu-id="c342c-113">**Getarcdirection**</span><span class="sxs-lookup"><span data-stu-id="c342c-113">**GetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getarcdirection) | <span data-ttu-id="c342c-114">Ruft die aktuelle Bogen Richtung für den angegebenen Gerätekontext ab.</span><span class="sxs-lookup"><span data-stu-id="c342c-114">Retrieves the current arc direction for the specified device context.</span></span>                                         |
| [<span data-ttu-id="c342c-115">**LineDDA**</span><span class="sxs-lookup"><span data-stu-id="c342c-115">**LineDDA**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-linedda)                 | <span data-ttu-id="c342c-116">Bestimmt, welche Pixel für eine Linie hervorgehoben werden sollen, die durch die angegebenen Start-und Endpunkte definiert ist.</span><span class="sxs-lookup"><span data-stu-id="c342c-116">Determines which pixels should be highlighted for a line defined by the specified starting and ending points.</span></span> |
| [<span data-ttu-id="c342c-117">**Lineddaproc**</span><span class="sxs-lookup"><span data-stu-id="c342c-117">**LineDDAProc**</span></span>](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)         | <span data-ttu-id="c342c-118">Eine von der Anwendung definierte Rückruffunktion, die mit der LineDDA-Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c342c-118">An application-defined callback function used with the LineDDA function.</span></span>                                      |
| [<span data-ttu-id="c342c-119">**LineTo**</span><span class="sxs-lookup"><span data-stu-id="c342c-119">**LineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-lineto)                   | <span data-ttu-id="c342c-120">Zeichnet eine Linie von der aktuellen Position bis zum angegebenen Punkt, aber nicht einschließlich.</span><span class="sxs-lookup"><span data-stu-id="c342c-120">Draws a line from the current position up to, but not including, the specified point.</span></span>                         |
| [<span data-ttu-id="c342c-121">**"Muvezu Ex"**</span><span class="sxs-lookup"><span data-stu-id="c342c-121">**MoveToEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)               | <span data-ttu-id="c342c-122">Aktualisiert die aktuelle Position auf den angegebenen Punkt und gibt optional die vorherige Position zurück.</span><span class="sxs-lookup"><span data-stu-id="c342c-122">Updates the current position to the specified point and optionally returns the previous position.</span></span>             |
| [<span data-ttu-id="c342c-123">**Polybezier**</span><span class="sxs-lookup"><span data-stu-id="c342c-123">**PolyBezier**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)           | <span data-ttu-id="c342c-124">Zeichnet eine oder mehrere Bézier-Kurven.</span><span class="sxs-lookup"><span data-stu-id="c342c-124">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="c342c-125">**PolyBezierTo**</span><span class="sxs-lookup"><span data-stu-id="c342c-125">**PolyBezierTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)       | <span data-ttu-id="c342c-126">Zeichnet eine oder mehrere Bézier-Kurven.</span><span class="sxs-lookup"><span data-stu-id="c342c-126">Draws one or more Bézier curves.</span></span>                                                                              |
| [<span data-ttu-id="c342c-127">**Polydraw**</span><span class="sxs-lookup"><span data-stu-id="c342c-127">**PolyDraw**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)               | <span data-ttu-id="c342c-128">Zeichnet eine Reihe von Liniensegmenten und Bézier-Kurven.</span><span class="sxs-lookup"><span data-stu-id="c342c-128">Draws a set of line segments and Bézier curves.</span></span>                                                               |
| [<span data-ttu-id="c342c-129">**Polylinie**</span><span class="sxs-lookup"><span data-stu-id="c342c-129">**Polyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polyline)               | <span data-ttu-id="c342c-130">Zeichnet eine Reihe von Liniensegmenten, indem die Punkte im angegebenen Array verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="c342c-130">Draws a series of line segments by connecting the points in the specified array.</span></span>                              |
| [<span data-ttu-id="c342c-131">**PolyLineTo**</span><span class="sxs-lookup"><span data-stu-id="c342c-131">**PolylineTo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)           | <span data-ttu-id="c342c-132">Zeichnet eine oder mehrere gerade Linien.</span><span class="sxs-lookup"><span data-stu-id="c342c-132">Draws one or more straight lines.</span></span>                                                                             |
| [<span data-ttu-id="c342c-133">**Polypolyline**</span><span class="sxs-lookup"><span data-stu-id="c342c-133">**PolyPolyline**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)       | <span data-ttu-id="c342c-134">Zeichnet mehrere Reihe verbundener Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="c342c-134">Draws multiple series of connected line segments.</span></span>                                                             |
| [<span data-ttu-id="c342c-135">**"Tartarcdirection"**</span><span class="sxs-lookup"><span data-stu-id="c342c-135">**SetArcDirection**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) | <span data-ttu-id="c342c-136">Legt die Zeichnungs Richtung fest, die für Bogen-und Rechteck Funktionen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c342c-136">Sets the drawing direction to be used for arc and rectangle functions.</span></span>                                        |



 

 

 



