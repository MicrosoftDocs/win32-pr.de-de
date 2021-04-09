---
title: Einfache Audiowiedergabe
description: Einfache Audiowiedergabe
ms.assetid: 51a0244d-123d-4efe-92e9-972e914cef78
keywords:
- Multimedia-Audiodatei, Wellenform
- Audiodaten, Wellenform
- Wellenform-Audiodatei, einfache Wiedergabe
- MessageBeep-Funktion
- SndPlaySound-Funktion
- PlaySound-Funktion, einfache Wiedergabe
- Multimedia-Audio, PlaySound-Funktion
- Audio, PlaySound-Funktion
- Wellenform-Audio, PlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256feded06de4ee92ee415f14bb08adc7fb4456e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948661"
---
# <a name="simple-audio-playback"></a><span data-ttu-id="feda9-112">Einfache Audiowiedergabe</span><span class="sxs-lookup"><span data-stu-id="feda9-112">Simple Audio Playback</span></span>

<span data-ttu-id="feda9-113">Sie können die folgenden Funktionen verwenden, um Wellenform-Audiodaten in der Anwendung in einem einzelnen Funktions aufzurufen wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="feda9-113">You can use the following functions to play waveform audio in your application in a single function call.</span></span>



| <span data-ttu-id="feda9-114">Funktion</span><span class="sxs-lookup"><span data-stu-id="feda9-114">Function</span></span>                                                      | <span data-ttu-id="feda9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="feda9-115">Description</span></span>                                                                                                         |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feda9-116">MessageBeep</span><span class="sxs-lookup"><span data-stu-id="feda9-116">MessageBeep</span></span>](/windows/win32/api/winuser/nf-winuser-messagebeep) | <span data-ttu-id="feda9-117">Gibt den Sound wieder, der einer angegebenen System Warnstufe entspricht.</span><span class="sxs-lookup"><span data-stu-id="feda9-117">Plays the sound that corresponds to a specified system-alert level.</span></span>                                                 |
| <span data-ttu-id="feda9-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="feda9-118">[**sndPlaySound**](/previous-versions//dd798676(v=vs.85))</span></span>                          | <span data-ttu-id="feda9-119">Gibt den Sound wieder, der dem in der Registrierung eingegebenen System Sound oder dem Inhalt der angegebenen Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="feda9-119">Plays the sound that corresponds to the system sound entered in the registry or the contents of the specified file.</span></span> |
| <span data-ttu-id="feda9-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="feda9-120">[**PlaySound**](/previous-versions//dd743680(v=vs.85))</span></span>                                | <span data-ttu-id="feda9-121">Bietet die gesamte Funktionalität von [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) und kann direkt auf Ressourcen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="feda9-121">Provides all the functionality of [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and can directly access resources.</span></span>           |



 

<span data-ttu-id="feda9-122">Die **MessageBeep** -Funktion ist ein Standard Teil der Win32-API. Da die Funktionen sehr eingeschränkt sind und an anderer Stelle dokumentiert werden, werden Sie hier nicht erläutert.</span><span class="sxs-lookup"><span data-stu-id="feda9-122">The **MessageBeep** function is a standard part of the Win32 API; because its capabilities are very limited and it is documented elsewhere, it is not discussed here.</span></span>

<span data-ttu-id="feda9-123">Die aufgeführten Funktionen unterstützen die folgenden Quellen der Wellenform-Audiodatei:</span><span class="sxs-lookup"><span data-stu-id="feda9-123">The functions listed support the following sources of waveform audio:</span></span>

-   <span data-ttu-id="feda9-124">Waveform-Audiodateien, die System Warn Stufen zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="feda9-124">Waveform-audio files associated with system-alert levels</span></span>
-   <span data-ttu-id="feda9-125">Waveform-Audiodateien, die durch Einträge in der Registrierung angegeben werden</span><span class="sxs-lookup"><span data-stu-id="feda9-125">Waveform-audio files specified by entries in the registry</span></span>
-   <span data-ttu-id="feda9-126">In-Memory-Wellen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="feda9-126">In-memory WAVE resources</span></span>
-   <span data-ttu-id="feda9-127">Waveform-Audiodateien, angegeben nach Name</span><span class="sxs-lookup"><span data-stu-id="feda9-127">Waveform-audio files specified by name</span></span>

<span data-ttu-id="feda9-128">Die Funktionen [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) und [**PlaySound**](/previous-versions//dd743680(v=vs.85)) laden eine gesamte Waveform-Audiodatei in den Arbeitsspeicher und schränken die Größe der Datei ein, die Sie wiedergeben können.</span><span class="sxs-lookup"><span data-stu-id="feda9-128">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) and [**PlaySound**](/previous-versions//dd743680(v=vs.85)) functions load an entire waveform-audio file into memory and, in effect, limit the size of the file they can play.</span></span> <span data-ttu-id="feda9-129">Verwenden Sie **sndPlaySound** und **PlaySound** , um Waveform-Audiodateien wiederzugeben, die klein sind – bis zu 100 KB.</span><span class="sxs-lookup"><span data-stu-id="feda9-129">Use **sndPlaySound** and **PlaySound** to play waveform-audio files that are small — up to about 100K.</span></span> <span data-ttu-id="feda9-130">Diese beiden Funktionen erfordern auch, dass die Audiodaten in einem Format vorliegen, das von einem der installierten Waveform-Audiotreiber (einschließlich der Wave-Mapper) abgespielt werden kann.</span><span class="sxs-lookup"><span data-stu-id="feda9-130">These two functions also require the sound data to be in a format that is playable by one of the installed waveform-audio drivers, including the wave mapper.</span></span>

<span data-ttu-id="feda9-131">Verwenden Sie für größere Audiodateien die MCI-Dienste (Media Control Interface).</span><span class="sxs-lookup"><span data-stu-id="feda9-131">For larger sound files, use the Media Control Interface (MCI) services.</span></span> <span data-ttu-id="feda9-132">Weitere Informationen finden Sie unter [MCI](mci.md).</span><span class="sxs-lookup"><span data-stu-id="feda9-132">For more information, see [MCI](mci.md).</span></span>

 

 