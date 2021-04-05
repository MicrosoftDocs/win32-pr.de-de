---
title: Informationen zu MIDI
description: Informationen zu MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia, Digital Instrumentation Digital Interface (MIDI)
- Multimedia-Audiodatei, Digital Instrumentation Digital Interface (MIDI)
- Audioschnittstelle (Digital Instrumentation Digital Interface, MIDI)
- Digital Instrumentation Digital Interface (MIDI), Informationen zu
- MIDI (Digital Instrumentation Digital Interface), Informationen zu
- Digital Instrumentation Digital Interface (MIDI), Media Control Interface (MCI)
- MIDI (Digital Instrumentation Digital Interface), Medien Steuerungs Schnittstelle (MCI)
- Digital Instrumentation Digital Interface (MIDI), Streampuffer
- MIDI (Digital Instrumentation Digital Interface), Streampuffer
- Digital Instrumentation Digital Interface (MIDI), MIDI-Dienste
- MIDI (Digital Instrumentation Digital Interface), MIDI-Dienste
- Media Control Interface (MCI), Digital Instrumentation Digital Interface (MIDI)
- MCI (Media Control Interface), Digital Instrumentation Digital Interface (MIDI)
- Streampuffer, Informationen
- MIDI-Dienste, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708927"
---
# <a name="about-midi"></a><span data-ttu-id="efa99-119">Informationen zu MIDI</span><span class="sxs-lookup"><span data-stu-id="efa99-119">About MIDI</span></span>

<span data-ttu-id="efa99-120">Die Microsoft Win32-API (Application Programming Interface) bietet die folgenden Methoden für Anwendungen, um mit den Daten von MIDI zu arbeiten:</span><span class="sxs-lookup"><span data-stu-id="efa99-120">The Microsoft Win32 application programming interface (API) provides the following methods for applications to work with MIDI data:</span></span>

-   <span data-ttu-id="efa99-121">Die Media Control Interface (MCI).</span><span class="sxs-lookup"><span data-stu-id="efa99-121">The Media Control Interface (MCI).</span></span> <span data-ttu-id="efa99-122">Die einfachste Möglichkeit zum Wiedergeben einer MIDI-Datei ist die Verwendung der mciwnd-Fenster Klasse, Sie können jedoch auch MCI-Befehle verwenden, um eine benutzerdefinierte Schnittstelle zu einem MIDI-Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="efa99-122">Although the simplest way to play a MIDI file is to use the MCIWnd window class, you can also use MCI commands to create a customized interface to a MIDI device.</span></span> <span data-ttu-id="efa99-123">Weitere Informationen zur mciwnd-Fenster Klasse finden Sie unter [mciwnd Window Class](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="efa99-123">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span> <span data-ttu-id="efa99-124">Weitere Informationen zu MCI finden Sie unter [MCI](mci.md)oder [Media Control Interface (MCI)](media-control-interface--mci.md).</span><span class="sxs-lookup"><span data-stu-id="efa99-124">For more information about MCI, see [MCI](mci.md), or [Media Control Interface (MCI)](media-control-interface--mci.md).</span></span>
-   <span data-ttu-id="efa99-125">[Streampuffer](stream-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="efa99-125">[Stream Buffers](stream-buffers.md).</span></span> <span data-ttu-id="efa99-126">Dieses Format ermöglicht es einer Anwendung, Puffer von mit Zeitstempel versehene MIDI-Daten für die Wiedergabe zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="efa99-126">This format allows an application to manipulate buffers of time-stamped MIDI data for playback.</span></span> <span data-ttu-id="efa99-127">Streampuffer sind für Anwendungen nützlich, die eine präzisere Kontrolle über die Ausgabe benötigen als MCI bietet.</span><span class="sxs-lookup"><span data-stu-id="efa99-127">Stream buffers are useful to applications that require more precise control over output than MCI offers.</span></span>
-   <span data-ttu-id="efa99-128">[MIDI-Dienste](midi-services.md).</span><span class="sxs-lookup"><span data-stu-id="efa99-128">[MIDI Services](midi-services.md).</span></span> <span data-ttu-id="efa99-129">Anwendungen, die die präzisere Kontrolle über die Daten von MIDI benötigen, verwenden normalerweise diese Dienste auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="efa99-129">Applications that need the most precise control of MIDI data typically use these low-level services.</span></span>

<span data-ttu-id="efa99-130">In den folgenden Themen wird jede dieser Methoden beschrieben, und es wird eine Übersicht über den MIDI-Mapper bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="efa99-130">The following topics discuss each of these methods and provides an overview of the MIDI Mapper.</span></span>

-   [<span data-ttu-id="efa99-131">Der MIDI-Mapper</span><span class="sxs-lookup"><span data-stu-id="efa99-131">The MIDI Mapper</span></span>](the-midi-mapper.md)
-   [<span data-ttu-id="efa99-132">Medien Steuerungs Schnittstelle (MCI)</span><span class="sxs-lookup"><span data-stu-id="efa99-132">Media Control Interface (MCI)</span></span>](media-control-interface--mci.md)
-   [<span data-ttu-id="efa99-133">Streampuffer</span><span class="sxs-lookup"><span data-stu-id="efa99-133">Stream Buffers</span></span>](stream-buffers.md)
-   [<span data-ttu-id="efa99-134">MIDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="efa99-134">MIDI Services</span></span>](midi-services.md)
-   [<span data-ttu-id="efa99-135">Abspielen von MIDI-Dateien</span><span class="sxs-lookup"><span data-stu-id="efa99-135">Playing MIDI Files</span></span>](playing-midi-files.md)
-   [<span data-ttu-id="efa99-136">Aufzeichnen von MIDI-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="efa99-136">Recording MIDI Audio</span></span>](recording-midi-audio.md)
-   [<span data-ttu-id="efa99-137">Verarbeiten von MIDI-Daten aus zwei MIDI-Quellen</span><span class="sxs-lookup"><span data-stu-id="efa99-137">Processing MIDI Data from Two MIDI Sources</span></span>](processing-midi-data-from-two-midi-sources.md)
-   [<span data-ttu-id="efa99-138">Erstellen von MIDI-Dateien</span><span class="sxs-lookup"><span data-stu-id="efa99-138">Creating MIDI Files</span></span>](creating-midi-files.md)

 

 




