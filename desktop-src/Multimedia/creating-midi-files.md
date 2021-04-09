---
title: Erstellen von MIDI-Dateien
description: Erstellen von MIDI-Dateien
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows-Multimedia, Erstellen von MIDI-Dateien
- Multimedia, Erstellen von MIDI-Dateien
- Multimedia-Audiodatei, Erstellen von MIDI-Dateien
- Audiodatei, Erstellen von MIDI-Dateien
- Digital Instrumentation Digital Interface (MIDI), Erstellen von Dateien
- MIDI (Digital Instrumentation Digital Interface), Erstellen von Dateien
- Erstellen von MIDI-Dateien, Informationen zu
- Zuordnung von MIDI-Herstellern (MMA)
- MMA (Zuordnung von MIDI-Herstellern)
- Ausführliche Beschreibung von MIDI
- Standard-.
- Allgemeine (GVO-) Spezifikation
- GM-Spezifikation (General MIDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036682"
---
# <a name="creating-midi-files"></a><span data-ttu-id="5a215-116">Erstellen von MIDI-Dateien</span><span class="sxs-lookup"><span data-stu-id="5a215-116">Creating MIDI Files</span></span>

<span data-ttu-id="5a215-117">Die Digital Instrumentation Digital Interface (MIDI)-Spezifikationen werden von veröffentlicht und sind urheberrechtlich geschütztes Material der Zuordnung von MIDI-Herstellern (MMA).</span><span class="sxs-lookup"><span data-stu-id="5a215-117">The Musical Instrument Digital Interface (MIDI) specifications are published by and are copyrighted material of the MIDI Manufacturers Association (MMA).</span></span> <span data-ttu-id="5a215-118">In der folgenden Liste werden die Spezifikationen beschrieben, die das größte allgemeine Interesse haben:</span><span class="sxs-lookup"><span data-stu-id="5a215-118">The following list describes the specifications which are of the greatest general interest:</span></span>

## <a name="midi-detailed-specification"></a><span data-ttu-id="5a215-119">Ausführliche Beschreibung von MIDI</span><span class="sxs-lookup"><span data-stu-id="5a215-119">MIDI Detailed Specification</span></span>

<span data-ttu-id="5a215-120">In der detaillierten Beschreibung des Protokolls werden die Protokolle "Hardware und Software" von MIDI erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a215-120">The MIDI Detailed Specification explains the MIDI hardware and software protocols.</span></span> <span data-ttu-id="5a215-121">Dies ist nützlich für die Entwicklung von Multimedia-Anwendungen, die Unterstützung für die Unterstützung von MIDI mithilfe von MIDI-Funktionen zum Aufzeichnen, bearbeiten und/oder Wiedergeben von Daten von MIDI</span><span class="sxs-lookup"><span data-stu-id="5a215-121">This is useful to those developing multimedia applications which implement MIDI support by using MIDI functions to record, edit, and/or play MIDI data.</span></span>

## <a name="standard-midi-files-10"></a><span data-ttu-id="5a215-122">Standard-MIDI-Dateien 1,0</span><span class="sxs-lookup"><span data-stu-id="5a215-122">Standard MIDI Files 1.0</span></span>

<span data-ttu-id="5a215-123">Mit der Standard-Datei für die-MIDI-Dateien wird eine Möglichkeit zum Austauschen von Daten mit Zeitstempel zwischen verschiedenen Anwendungen auf derselben oder unterschiedlichen Hardwareplattformen definiert.</span><span class="sxs-lookup"><span data-stu-id="5a215-123">The Standard MIDI Files specification defines a way to interchange time-stamped MIDI data between different applications on the same or different hardware platforms.</span></span> <span data-ttu-id="5a215-124">Dies ist nützlich für Entwickler, die Anwendungen schreiben, die Datenträger Dateien lesen und analysieren, die die Daten auf dem Datenträger schreiben und/oder auf dem Datenträger schreiben.</span><span class="sxs-lookup"><span data-stu-id="5a215-124">This is useful to developers writing applications that read and parse disk files containing MIDI data and/or write MIDI data files to disk.</span></span>

## <a name="general-midi-system---level-1"></a><span data-ttu-id="5a215-125">Allgemeine System-und System Ebene 1</span><span class="sxs-lookup"><span data-stu-id="5a215-125">General MIDI System - Level 1</span></span>

<span data-ttu-id="5a215-126">In der allgemeinen "MIDI (GM)"-Spezifikation wird eine minimale MIDI-Konfiguration eines "allgemeinen MIDI-Systems" definiert.</span><span class="sxs-lookup"><span data-stu-id="5a215-126">The General MIDI (GM) specification defines a minimum MIDI configuration of a "General MIDI System".</span></span> <span data-ttu-id="5a215-127">Dieses System besteht aus einer bestimmten Klasse von MIDI-Wiedergabe Geräten und ist für multimediaderentwickler von Interesse, die als Autor von MIDI-Dateien arbeiten.</span><span class="sxs-lookup"><span data-stu-id="5a215-127">This system consists of a specific class of MIDI playback devices and is of interest to multimedia developers who author MIDI files.</span></span> <span data-ttu-id="5a215-128">Die meisten heute hergestellten PCs und MIDI-Synthesizer sind mit der GM-Spezifikation kompatibel.</span><span class="sxs-lookup"><span data-stu-id="5a215-128">Most PC sound cards and MIDI synthesizers manufactured today are compatible with the GM specification.</span></span> <span data-ttu-id="5a215-129">In der GM-Spezifikation erstellte MIDI-Dateien sollten in der Regel so klingen, als wären Sie für den Sound gedacht, unabhängig davon, auf welchem GM-kompatiblen Gerät Sie abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="5a215-129">MIDI files which are authored to the GM specification should generally sound as they were intended to sound, no matter which GM-compatible device they are played on.</span></span>

<span data-ttu-id="5a215-130">Um es zu ermöglichen, dass für die Darstellung von Dateien in Multimedia Computing ein brauchbares Format für die Darstellung von Dateien in einem Format vorliegt, befolgt Windows die allgemeine System Ebene 1</span><span class="sxs-lookup"><span data-stu-id="5a215-130">To enable MIDI files to be a viable format for representing music in multimedia computing, Windows follows the General MIDI System Level 1 specification.</span></span> <span data-ttu-id="5a215-131">Die folgenden Themen stellen zusätzliche Richtlinien für die Erstellung von Richtlinien zur</span><span class="sxs-lookup"><span data-stu-id="5a215-131">The following topics provide additional MIDI authoring guidelines:</span></span>

-   [<span data-ttu-id="5a215-132">Erstellungs Richtlinien für MIDI-Dateien</span><span class="sxs-lookup"><span data-stu-id="5a215-132">Authoring Guidelines for MIDI Files</span></span>](authoring-guidelines-for-midi-files.md)
-   [<span data-ttu-id="5a215-133">Standard mäßige MIDI-patchzuweisungen</span><span class="sxs-lookup"><span data-stu-id="5a215-133">Standard MIDI Patch Assignments</span></span>](standard-midi-patch-assignments.md)
-   [<span data-ttu-id="5a215-134">Standard-MIDI-schlüsselzuweisungen</span><span class="sxs-lookup"><span data-stu-id="5a215-134">Standard MIDI Key Assignments</span></span>](standard-midi-key-assignments.md)

 

 




