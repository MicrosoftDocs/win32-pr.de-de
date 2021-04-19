---
title: Komponenten
description: Komponenten
ms.assetid: 9fbd957d-ee6b-475f-8a04-51effa206ad5
keywords:
- OpenGL unter Windows, Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1294745938e245deda8296f2ce4d1df386b9f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341468"
---
# <a name="components"></a><span data-ttu-id="0343f-104">Komponenten</span><span class="sxs-lookup"><span data-stu-id="0343f-104">Components</span></span>

<span data-ttu-id="0343f-105">Die Microsoft-Implementierung von OpenGL in Windows umfasst die folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="0343f-105">Microsoft's implementation of OpenGL in Windows includes the following components:</span></span>

-   <span data-ttu-id="0343f-106">Der vollständige Satz der aktuellen OpenGL-Befehle</span><span class="sxs-lookup"><span data-stu-id="0343f-106">The full set of current OpenGL commands</span></span>

    <span data-ttu-id="0343f-107">OpenGL enthält eine Bibliothek mit Kernfunktionen für 3D-Grafik Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="0343f-107">OpenGL contains a library of core functions for 3-D graphics operations.</span></span> <span data-ttu-id="0343f-108">Diese grundlegenden Funktionen werden verwendet, um Objektform Beschreibung, Matrix Transformation, Beleuchtung, Färbung, Textur, Clipping, Bitmaps, Nebel und Antialiasing zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="0343f-108">These basic functions are used to manage object shape description, matrix transformation, lighting, coloring, texture, clipping, bitmaps, fog, and antialiasing.</span></span> <span data-ttu-id="0343f-109">Die Namen für diese Kernfunktionen haben das Präfix "GL".</span><span class="sxs-lookup"><span data-stu-id="0343f-109">The names for these core functions have a "gl" prefix.</span></span>

    <span data-ttu-id="0343f-110">Viele der OpenGL-Befehle verfügen über mehrere Varianten, die sich von der Anzahl und dem Typ ihrer Parameter unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="0343f-110">Many of the OpenGL commands have several variants, which differ in the number and type of their parameters.</span></span> <span data-ttu-id="0343f-111">Wenn alle Varianten gezählt werden, sind mehr als 300 OpenGL-Befehle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0343f-111">Counting all the variants, there are more than 300 OpenGL commands.</span></span>

-   <span data-ttu-id="0343f-112">The OpenGL Utility (GLU) Library</span><span class="sxs-lookup"><span data-stu-id="0343f-112">The OpenGL Utility (GLU) library</span></span>

    <span data-ttu-id="0343f-113">Diese Bibliothek von Hilfsfunktionen ergänzt die wichtigsten OpenGL-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0343f-113">This library of auxiliary functions complements the core OpenGL functions.</span></span> <span data-ttu-id="0343f-114">Die Befehle verwalten Textur Unterstützung, Koordinatentransformation, Polygon-Mosaik, renderingbereiche, Zylinder und Datenträger, NURBS (nicht einheitliche rationale B-Spline-Kurven und-Oberflächen) und Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="0343f-114">The commands manage texture support, coordinate transformation, polygon tessellation, rendering spheres, cylinders and disks, NURBS (Non-Uniform Rational B-Spline) curves and surfaces, and error handling.</span></span>

-   <span data-ttu-id="0343f-115">Hilfsbibliothek für OpenGL-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="0343f-115">The OpenGL Programming Guide Auxiliary library</span></span>

    <span data-ttu-id="0343f-116">Dies ist eine einfache, plattformunabhängige Funktionsbibliothek für die Verwaltung von Fenstern, das Behandeln von Eingabe Ereignissen, das Zeichnen klassischer 3D-Objekte, das Verwalten eines Hintergrund Prozesses und das Ausführen eines Programms.</span><span class="sxs-lookup"><span data-stu-id="0343f-116">This is a simple, platform-independent library of functions for managing windows, handling input events, drawing classic 3-D objects, managing a background process, and running a program.</span></span> <span data-ttu-id="0343f-117">Die Fensterverwaltung und Eingabe Routinen stellen eine grundlegende Funktionalität bereit, mit der Sie schnell mit der Programmierung in OpenGL beginnen können.</span><span class="sxs-lookup"><span data-stu-id="0343f-117">The window management and input routines provide a base level of functionality with which you can quickly get started programming in OpenGL.</span></span>

    <span data-ttu-id="0343f-118">Verwenden Sie Sie jedoch nicht in einer Produktionsanwendung.</span><span class="sxs-lookup"><span data-stu-id="0343f-118">Do not use them, however, in a production application.</span></span> <span data-ttu-id="0343f-119">Dies sind einige Gründe für diese Warnung:</span><span class="sxs-lookup"><span data-stu-id="0343f-119">Here are some reasons for this warning:</span></span>

    -   <span data-ttu-id="0343f-120">Die Nachrichten Schleife befindet sich im Bibliotheks Code.</span><span class="sxs-lookup"><span data-stu-id="0343f-120">The message loop is in the library code.</span></span>
    -   <span data-ttu-id="0343f-121">Es gibt keine Möglichkeit zum Hinzufügen von Handlern für zusätzliche WM- \* Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="0343f-121">There is no way to add handlers for additional WM\* messages.</span></span>
    -   <span data-ttu-id="0343f-122">Logische Paletten werden nur sehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0343f-122">There is very little support for logical palettes.</span></span>

    <span data-ttu-id="0343f-123">Die Bibliothek wird im *OpenGL-Programmier Handbuch* beschrieben und verwendet.</span><span class="sxs-lookup"><span data-stu-id="0343f-123">The library is described and used in the *OpenGL Programming Guide*.</span></span>

-   <span data-ttu-id="0343f-124">Die WGL-Funktionen</span><span class="sxs-lookup"><span data-stu-id="0343f-124">The WGL functions</span></span>

    <span data-ttu-id="0343f-125">Dieser Funktions Satz verbindet OpenGL mit dem Windows-windowingsystem.</span><span class="sxs-lookup"><span data-stu-id="0343f-125">This set of functions connects OpenGL to the Windows windowing system.</span></span> <span data-ttu-id="0343f-126">Die Funktionen verwalten renderingkontexte, Anzeigelisten, Erweiterungsfunktionen und Schriftart Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="0343f-126">The functions manage rendering contexts, display lists, extension functions, and font bitmaps.</span></span> <span data-ttu-id="0343f-127">Die WGL-Funktionen entsprechen den glx-Erweiterungen, die OpenGL mit dem X-Fenster System verbinden.</span><span class="sxs-lookup"><span data-stu-id="0343f-127">The WGL functions are analogous to the GLX extensions that connect OpenGL to the X Window System.</span></span> <span data-ttu-id="0343f-128">Die Namen für diese Funktionen haben das Präfix "WGL".</span><span class="sxs-lookup"><span data-stu-id="0343f-128">The names for these functions have a "wgl" prefix.</span></span>

-   <span data-ttu-id="0343f-129">Neue Windows-Funktionen für Pixel Formate und doppelte Pufferung</span><span class="sxs-lookup"><span data-stu-id="0343f-129">New Windows functions for pixel formats and double buffering</span></span>

    <span data-ttu-id="0343f-130">Diese Funktionen unterstützen Pixel Formate pro Fenster und doppelte Pufferung (für Smooth-Abbild Änderungen) von Fenstern.</span><span class="sxs-lookup"><span data-stu-id="0343f-130">These functions support per-window pixel formats and double buffering (for smooth image changes) of windows.</span></span> <span data-ttu-id="0343f-131">Diese neuen Funktionen gelten nur für OpenGL-Grafikfenster.</span><span class="sxs-lookup"><span data-stu-id="0343f-131">These new functions apply only to OpenGL graphics windows.</span></span>

 

 




