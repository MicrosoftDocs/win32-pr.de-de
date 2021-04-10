---
title: Medien Steuerungs Schnittstelle (MCI)
description: Medien Steuerungs Schnittstelle (MCI)
ms.assetid: e22f23b5-0fa6-4957-bbbf-b1b3a4c8bd31
keywords:
- Windows Multimedia, Media Control Interface (MCI)
- Multimedia, Medien Steuerungs Schnittstelle (MCI)
- Multimedia-Audiodaten, Medien Steuerungs Schnittstelle (MCI)
- Audioschnittstelle, Medien Steuerungs Schnittstelle (MCI)
- Digital Instrumentation Digital Interface (MIDI), Media Control Interface (MCI)
- MIDI (Digital Instrumentation Digital Interface), Medien Steuerungs Schnittstelle (MCI)
- Media Control Interface (MCI), Digital Instrumentation Digital Interface (MIDI)
- MCI (Media Control Interface), Digital Instrumentation Digital Interface (MIDI)
- Media Control Interface (MCI), MIDI Sequencer
- MCI (Medien Steuerungs Schnittstelle), MIDI Sequencer
- MCI-MIDI-Sequencer, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00aaf582f625c4411a2400ee381ec5c17d4d8ae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036887"
---
# <a name="media-control-interface-mci"></a><span data-ttu-id="23576-114">Medien Steuerungs Schnittstelle (MCI)</span><span class="sxs-lookup"><span data-stu-id="23576-114">Media Control Interface (MCI)</span></span>

<span data-ttu-id="23576-115">Der MCI-c#-Sequencer ist die MCI-Systemkomponente, die die Dateien von MIDI wieder gibt</span><span class="sxs-lookup"><span data-stu-id="23576-115">The MCI MIDI sequencer is the MCI system component that plays MIDI files.</span></span> <span data-ttu-id="23576-116">Anwendungen können mithilfe von MCI die Verwendung von MIDI-Dateien problemlos wiedergeben, aber MCI erzwingt die folgenden Einschränkungen für die Funktionen von "</span><span class="sxs-lookup"><span data-stu-id="23576-116">Applications can play MIDI files easily using MCI, but MCI imposes the following restrictions on MIDI capabilities:</span></span>

-   <span data-ttu-id="23576-117">MCI unterstützt nur die MIDI-Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="23576-117">MCI supports MIDI output only.</span></span>
-   <span data-ttu-id="23576-118">MCI lässt die Synchronisierung zwischen den Integritäts-und anderen Echt Zeit Ereignissen (z. b. Video) nicht zu.</span><span class="sxs-lookup"><span data-stu-id="23576-118">MCI does not allow close synchronization between MIDI events and other real-time events (such as video).</span></span>

<span data-ttu-id="23576-119">Wenn Sie eine genaue MIDI-Synchronisierung benötigen, müssen Sie die Datenstrom Puffer oder die Dienst-MIDI-Dienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="23576-119">If you need accurate MIDI synchronization, you must use the stream buffers or the MIDI services.</span></span> <span data-ttu-id="23576-120">Wenn Sie über die Funktionen der MIDI-Eingabe verfügen, müssen Sie die-Dienst-Dienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="23576-120">If you need MIDI input capabilities, you must use the MIDI services.</span></span>

<span data-ttu-id="23576-121">Der MCI-Dienst für die Integration von MIDI gibt standardmäßige Dateien für die Dateiformat-und ssmid-Dateien (Resource Interchange File Format) wieder.</span><span class="sxs-lookup"><span data-stu-id="23576-121">The MCI MIDI sequencer plays standard MIDI files and resource interchange file format (RIFF) MIDI files, known as RMID files.</span></span> <span data-ttu-id="23576-122">Standard-MIDI-Dateien entsprechen der Standard--Datei für die-und- [Dateien 1,0](creating-midi-files.md)</span><span class="sxs-lookup"><span data-stu-id="23576-122">Standard MIDI files conform to the [Standard MIDI Files 1.0](creating-midi-files.md) specification.</span></span> <span data-ttu-id="23576-123">Da es sich bei RMID-Dateien um standardmäßige MIDI-Dateien mit einem Riff-Header handelt, gelten die Informationen zu den standardmäßigen-Dateien für die Verwendung von</span><span class="sxs-lookup"><span data-stu-id="23576-123">Because RMID files are standard MIDI files with a RIFF header, information about standard MIDI files also applies to RMID files.</span></span> <span data-ttu-id="23576-124">Weitere Informationen zu Riff Dateien finden Sie unter [Datei Format Dienste für den Ressourcenaustausch](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="23576-124">For more information about RIFF files, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

<span data-ttu-id="23576-125">Obwohl derzeit drei Arten von Standard-MIDI-Dateien vorhanden sind, gibt der MCI-Sequencer nur zwei der folgenden Elemente aus: Format 0 und Format 1-MIDI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="23576-125">Although there are currently three kinds of standard MIDI files, the MCI sequencer plays only two of them: Format 0 and Format 1 MIDI files.</span></span>

<span data-ttu-id="23576-126">Weitere Informationen zum Steuern von Multimedia-Geräten (einschließlich Sequencer) mithilfe von MCI-Befehlen finden Sie unter [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="23576-126">For more information about controlling multimedia devices (including sequencers) using MCI commands, see [MCI](mci.md).</span></span>

 

 




