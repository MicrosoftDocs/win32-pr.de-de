---
title: Zuordnung von Waveform-Audio Geräten
description: Zuordnung von Waveform-Audio Geräten
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- Multimedia-Audiodatei, Mapping von Waveform-Audiogeräte
- Audiodatei, Mapping von Waveform-Audiogeräte
- Audiokomprimierungs-Manager (ACM), Mapping von Waveform-Audiogeräte
- ACM (Audiokomprimierungs-Manager), Mapping von Waveform-Audiogeräte
- Mapping von Waveform-Audiogeräten
- Multimedia-Audiodatei, Mapper
- Audiodatei, Mapper
- Audiokomprimierungs-Manager (ACM), Mapper
- ACM (Audiokomprimierungs-Manager), Mapper
- mapper
- Wellenform-Audiodatei, Mapping von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855863"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="0a01e-114">Zuordnung von Waveform-Audio Geräten</span><span class="sxs-lookup"><span data-stu-id="0a01e-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="0a01e-115">Windows stellt eine Reihe von Standardfunktionen für Audiogeräte bereit.</span><span class="sxs-lookup"><span data-stu-id="0a01e-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="0a01e-116">Diese Funktionen geben Aufrufe an Gerätetreiber aus, von denen Hardware Geräte verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0a01e-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="0a01e-117">Das System verwendet ein Modul, das als "Mapper" bezeichnet wird, um installierte Geräte zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="0a01e-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="0a01e-118">Der Mapper verwendet in der Treiberschnittstelle besondere Hooks, um Aufrufe abzufangen und als Vermittler zwischen dem System und den im System installierten Treibern zu fungieren.</span><span class="sxs-lookup"><span data-stu-id="0a01e-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="0a01e-119">Der Mapper ist für das Abgleichen von Anwendungsanforderungen für den Zugriff auf ein Gerät mit den verfügbaren Geräten und für die Suche nach einem Gerät zuständig, das den Audioanforderungen der aktuellen Anwendung entspricht.</span><span class="sxs-lookup"><span data-stu-id="0a01e-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="0a01e-120">Das System stellt Mapper für Standardtreiber Typen bereit: Waveform-Audiodaten, MIDI (Digital Interface Digital Interface) und hilfsangeräte.</span><span class="sxs-lookup"><span data-stu-id="0a01e-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="0a01e-121">Das ACM ist eine Erweiterung des grundlegenden Multimedia-Systems und wird als Mapper installiert.</span><span class="sxs-lookup"><span data-stu-id="0a01e-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="0a01e-122">Dies bedeutet, dass das ACM die Treiber Schnittstellen-Mapper-Hooks für Waveform-Audiogeräte verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a01e-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="0a01e-123">Die Verwendung dieser Hooks ermöglicht dem ACM das Decodieren oder Codieren von Waveform-Audiodaten vor der Übergabe an oder von einem Waveform-Audiogerätetreiber.</span><span class="sxs-lookup"><span data-stu-id="0a01e-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="0a01e-124">Der Unterschied zwischen dem ACM und dem Standardsystem Mapper besteht darin, dass das ACM nach einem Waveform-Audiogerät suchen kann, das ein bestimmtes Format unterstützt, oder eine Kombination aus einem Waveform-Audiogerät und einem ACM-Kompressor oder Dekompressor suchen kann, der ein bestimmtes Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a01e-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="0a01e-125">Wenn eine Anwendung anfordert, dass das System ein Waveform-Audiogerät für die Eingabe oder die Ausgabe öffnet, gibt die Anforderung das Format und das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="0a01e-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="0a01e-126">Wenn das angegebene Gerät der Mapper ist, muss der Mapper ein Gerät suchen, das das angegebene Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a01e-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="0a01e-127">Der im ACM implementierte Mapper sucht nach einem installierten Waveform-Audiogerät, das das angegebene Format unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0a01e-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="0a01e-128">Wenn das ACM ein solches Gerät nicht finden kann, sucht es nach einem Waveform-Audiogerät und einem Kompressor oder Dekompressor, von dem das Format unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0a01e-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="0a01e-129">Insbesondere sucht das ACM nach einem Kompressor oder Dekompressor, der das angegebene Format in ein Format konvertiert, das von einem installierten Waveform-Audiogerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0a01e-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="0a01e-130">Nachdem das ACM ein Gerät gefunden hat, das das konvertierte Format unterstützt, kann es Anforderungen zur Wiedergabe oder Aufzeichnung des ursprünglich angeforderten Formats berücksichtigen, obwohl dieses Format von keinem installierten Waveform-Audiogerät direkt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="0a01e-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="0a01e-131">Zusätzlich zur Formatkonvertierung bietet das ACM auch Dienste für die Unterstützung von Komprimierung, Dekomprimierung, Filterung, Format Auswahl und Filter Auswahl.</span><span class="sxs-lookup"><span data-stu-id="0a01e-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="0a01e-132">Sie stellt eine Standard-API bereit, die Sie unterstützt, indem Sie Ihre eigenen Treiber aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0a01e-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




