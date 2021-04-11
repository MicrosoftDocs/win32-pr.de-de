---
description: DVD-Anwendungen
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: DVD-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341849"
---
# <a name="dvd-applications"></a><span data-ttu-id="6c821-103">DVD-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6c821-103">DVD Applications</span></span>

<span data-ttu-id="6c821-104">DirectShow stellt eine Komponente namens " [DVD Navigator](dvd-navigator-filter.md) Source Filter" bereit, die DVD-Navigationsaufgaben in C++ vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="6c821-104">DirectShow provides a component called the [DVD Navigator](dvd-navigator-filter.md) source filter which simplifies DVD navigation tasks in C++.</span></span> <span data-ttu-id="6c821-105">Der DVD-Navigator bietet alle Funktionen, die Sie auf einem eigenständigen DVD-Player mit vollem Funktionsumfang finden, sowie zusätzliche Funktionen, die für die Wiedergabe von DVDs auf persönlichen Computern spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="6c821-105">The DVD Navigator has all the capabilities that you find on a full-featured stand-alone DVD player, plus additional capabilities specific to playing DVDs on personal computers.</span></span> <span data-ttu-id="6c821-106">Mit dem DVD-Navigator können C++-und Skriptentwickler mit voll funktionsfähigen DVD-Anwendungen erstellen, ohne auf die DVD-Spezifikation zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6c821-106">Using the DVD Navigator, C++ and scripting developers can create full-featured DVD applications without referring to the DVD specification.</span></span> <span data-ttu-id="6c821-107">Der DVD-Navigator übernimmt in Verbindung mit den decoderfiltern auch die regionale Verwaltung und den Schutz vor Urheberrechten (CSS-und analoger Kopierschutz) und isoliert die Anwendungsentwickler von diesen Details.</span><span class="sxs-lookup"><span data-stu-id="6c821-107">The DVD Navigator, in coordination with the decoder filters, also handles regional management and copyright protection (CSS and analog copy protection), isolating application developers from these details.</span></span>

<span data-ttu-id="6c821-108">Der Filter für den DVD-Navigator funktioniert auf einem gesamten DVD-Video Volume, das aus den Dateien im Verzeichnis "Video TS" besteht \_ .</span><span class="sxs-lookup"><span data-stu-id="6c821-108">The DVD Navigator filter works across an entire DVD-Video volume, which consists of the files in the VIDEO\_TS directory.</span></span> <span data-ttu-id="6c821-109">Im Gegensatz zu den meisten DirectShow-Quell filtern, die mit einzelnen Streams oder Dateien arbeiten, verwendet der DVD-Navigator die DVD-Video Struktur von Titeln, Kapiteln und Zeit Codes.</span><span class="sxs-lookup"><span data-stu-id="6c821-109">Unlike most DirectShow source filters that work with individual streams or files, the DVD Navigator uses the DVD-Video structure of titles, chapters, and time codes.</span></span> <span data-ttu-id="6c821-110">Entwickler, die einzelne MPEG-2-Dateien in DirectShow wiedergeben möchten, sollten den [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) anstelle des DVD-Navigator-Filters verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c821-110">Developers wishing to play individual MPEG-2 files in DirectShow should use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead of the DVD Navigator filter.</span></span> <span data-ttu-id="6c821-111">Weitere Informationen finden Sie [unter MPEG-2-Unterstützung in DirectShow](mpeg-2-support-in-directshow.md) .</span><span class="sxs-lookup"><span data-stu-id="6c821-111">See [MPEG-2 Support in DirectShow](mpeg-2-support-in-directshow.md) for more information.</span></span>

> [!Note]  
> <span data-ttu-id="6c821-112">Zum Abspielen von DVDs muss der Benutzer über einen MPEG-2-Decoder verfügen.</span><span class="sxs-lookup"><span data-stu-id="6c821-112">To play DVDs, the user must have an MPEG-2 decoder.</span></span>

 

<span data-ttu-id="6c821-113">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="6c821-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="6c821-114">Features der DVD-Unterstützung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c821-114">DVD Support Features in DirectShow</span></span>](dvd-support-features-in-directshow.md)
-   [<span data-ttu-id="6c821-115">DVD-Grundlagen</span><span class="sxs-lookup"><span data-stu-id="6c821-115">DVD Basics</span></span>](dvd-basics.md)
-   [<span data-ttu-id="6c821-116">Entwickeln des DVD-Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="6c821-116">Building the DVD Filter Graph</span></span>](building-the-dvd-filter-graph.md)
-   [<span data-ttu-id="6c821-117">Abrufen der DVD-Schnittstellen Zeiger</span><span class="sxs-lookup"><span data-stu-id="6c821-117">Obtaining the DVD Interface Pointers</span></span>](obtaining-the-dvd-interface-pointers.md)
-   [<span data-ttu-id="6c821-118">DVD-Befehle</span><span class="sxs-lookup"><span data-stu-id="6c821-118">DVD Commands</span></span>](dvd-commands.md)
-   [<span data-ttu-id="6c821-119">Identifizieren gültiger DVD-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="6c821-119">Identifying Valid DVD Operations</span></span>](identifying-valid-dvd-operations.md)
-   [<span data-ttu-id="6c821-120">Synchronisieren von DVD-Befehlen</span><span class="sxs-lookup"><span data-stu-id="6c821-120">Synchronizing DVD Commands</span></span>](synchronizing-dvd-commands.md)
-   [<span data-ttu-id="6c821-121">Datenfluss im DVD-Navigator</span><span class="sxs-lookup"><span data-stu-id="6c821-121">Data Flow in the DVD Navigator</span></span>](data-flow-in-the-dvd-navigator.md)
-   [<span data-ttu-id="6c821-122">Behandeln von DVD-Ereignis Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="6c821-122">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
-   [<span data-ttu-id="6c821-123">Arbeiten mit DVD-Menüs</span><span class="sxs-lookup"><span data-stu-id="6c821-123">Working With DVD Menus</span></span>](working-with-dvd-menus.md)
-   [<span data-ttu-id="6c821-124">Audiodaten Ströme</span><span class="sxs-lookup"><span data-stu-id="6c821-124">Audio and Subpicture Streams</span></span>](audio-and-subpicture-streams.md)
-   [<span data-ttu-id="6c821-125">Erzwingen von Eltern Verwaltungsebenen</span><span class="sxs-lookup"><span data-stu-id="6c821-125">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
-   [<span data-ttu-id="6c821-126">Speichern und Wiederherstellen von dvdstate-Objekten</span><span class="sxs-lookup"><span data-stu-id="6c821-126">Saving and Restoring DvdState Objects</span></span>](saving-and-restoring-dvdstate-objects.md)
-   [<span data-ttu-id="6c821-127">Arbeiten mit DVD-Text Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="6c821-127">Working with DVD Text Strings</span></span>](working-with-dvd-text-strings.md)
-   [<span data-ttu-id="6c821-128">Wiedergabe von Karaoke-Audiostreams</span><span class="sxs-lookup"><span data-stu-id="6c821-128">Playing Karaoke Audio Streams</span></span>](playing-karaoke-audio-streams.md)
-   [<span data-ttu-id="6c821-129">Behandlung von Disc-ejections</span><span class="sxs-lookup"><span data-stu-id="6c821-129">Handling Disc Ejections</span></span>](handling-disc-ejections.md)
-   [<span data-ttu-id="6c821-130">Erweiterungen der DVD-Wiedergabe in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c821-130">DVD Playback Enhancements in Windows Vista</span></span>](dvd-playback-enhancements-in-windows-vista.md)
-   [<span data-ttu-id="6c821-131">Konfiguration des DVD-Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="6c821-131">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
-   [<span data-ttu-id="6c821-132">Verknüpfungen zu C++-DVD-Referenzseiten</span><span class="sxs-lookup"><span data-stu-id="6c821-132">Shortcuts to C++ DVD Reference Pages</span></span>](shortcuts-to-c-dvd-reference-pages.md)

<span data-ttu-id="6c821-133">Verweise auf die Entwicklung von DVD/MPEG2-Decodern finden Sie unter [DVD-decoderentwicklung in DirectShow](dvd-decoder-development-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="6c821-133">For references on DVD/MPEG2 decoder development, see [DVD Decoder Development in DirectShow](dvd-decoder-development-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c821-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6c821-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c821-135">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="6c821-135">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



