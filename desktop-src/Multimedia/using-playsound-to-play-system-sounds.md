---
title: Verwenden von PlaySound zum Abspielen von System Sounds
description: Verwenden von PlaySound zum Abspielen von System Sounds
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- Wellenform-Audio, PlaySound-Funktion
- Wellenform-Audio, Abspielen von Systemsounds
- Wellenform-Audio, Sound Ereignisse
- PlaySound-Funktion, Abspielen von Systemsounds
- PlaySound-Funktion, Sound Ereignisse
- Wiedergabe von Waveform-audiosystemsounds
- Sound Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858250"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="78f58-110">Verwenden von PlaySound zum Abspielen von System Sounds</span><span class="sxs-lookup"><span data-stu-id="78f58-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="78f58-111">Die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion gibt auch Sounds wieder, auf die in der Registrierung durch einen keyName verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="78f58-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="78f58-112">Benutzer können Ihren eigenen Soundsystem Warnungen und-Warnungen oder Benutzeraktionen zuweisen, z. b. durch Klicken auf die Maustaste.</span><span class="sxs-lookup"><span data-stu-id="78f58-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="78f58-113">Sounds, die Systemwarnungen und Warnungen zugeordnet sind, werden als *Sound Ereignisse* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="78f58-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="78f58-114">Um ein Sound Ereignis wiederzugeben, müssen Sie **PlaySound** mit dem *pszsound* -Parameter aufrufen, der auf eine Zeichenfolge verweist, die den Namen des Registrierungs Eintrags enthält, der den Sound identifiziert.</span><span class="sxs-lookup"><span data-stu-id="78f58-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="78f58-115">Verwenden Sie die folgende Anweisung, um beispielsweise den dem "moukliclick"-Eintrag zugeordneten Sound wiederzugeben und vor der Rückgabe auf den Abschluss des Sounds zu warten:</span><span class="sxs-lookup"><span data-stu-id="78f58-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="78f58-116">Wenn der angegebene Registrierungs Eintrag oder die anzuzeigende Waveform-Audiodatei nicht vorhanden ist, oder wenn die Datei nicht in den verfügbaren Arbeitsspeicher passt, gibt **PlaySound** den Standardsystem Sound wieder.</span><span class="sxs-lookup"><span data-stu-id="78f58-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="78f58-117">Die vom System vordefinierten Audioereignisse können von der Plattform abweichen.</span><span class="sxs-lookup"><span data-stu-id="78f58-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="78f58-118">Die folgende Liste enthält die Audioereignisse, die für alle Implementierungen der Win32-API definiert sind:</span><span class="sxs-lookup"><span data-stu-id="78f58-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="78f58-119">Systemasterisk</span><span class="sxs-lookup"><span data-stu-id="78f58-119">SystemAsterisk</span></span>
-   <span data-ttu-id="78f58-120">SystemExclamation</span><span class="sxs-lookup"><span data-stu-id="78f58-120">SystemExclamation</span></span>
-   <span data-ttu-id="78f58-121">System Exit</span><span class="sxs-lookup"><span data-stu-id="78f58-121">SystemExit</span></span>
-   <span data-ttu-id="78f58-122">Systemhand</span><span class="sxs-lookup"><span data-stu-id="78f58-122">SystemHand</span></span>
-   <span data-ttu-id="78f58-123">Systemfrage</span><span class="sxs-lookup"><span data-stu-id="78f58-123">SystemQuestion</span></span>
-   <span data-ttu-id="78f58-124">Systemstart</span><span class="sxs-lookup"><span data-stu-id="78f58-124">SystemStart</span></span>

<span data-ttu-id="78f58-125">Wenn eine Anwendung eigene Audioereignisse registriert, kann der Benutzer das Audioereignis mithilfe der standardmäßigen System Steuerungs Schnittstelle konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="78f58-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="78f58-126">Die Anwendung sollte das Sound Ereignis mithilfe der Standard Registrierungsfunktionen registrieren. Weitere Informationen finden Sie unter [Registry](../sysinfo/registry.md).</span><span class="sxs-lookup"><span data-stu-id="78f58-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="78f58-127">Die Einträge gehören zur gleichen Position in der Registrierungs Hierarchie wie die restlichen Sound Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="78f58-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="78f58-128">Diese Position variiert bei der Win32-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="78f58-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="78f58-129">Der entsprechende Datenwert variiert auch mit der-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="78f58-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="78f58-130">Die Funktion " [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) " durchsucht die Registrierung stets nach einem keyName, der mit *lpszsound* übereinstimmt, bevor versucht wird, eine Datei mit diesem Namen zu laden.</span><span class="sxs-lookup"><span data-stu-id="78f58-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="78f58-131">Die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion akzeptiert Flags, die den Speicherort des Sounds angeben.</span><span class="sxs-lookup"><span data-stu-id="78f58-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 