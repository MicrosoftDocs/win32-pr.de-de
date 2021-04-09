---
title: Ändern des internen MIDI-synthesizervolumes
description: Ändern des internen MIDI-synthesizervolumes
ms.assetid: 75ab7ff5-f394-4a79-8dcc-f4eef434a36e
keywords:
- Digital Instrumentation Digital Interface (MIDI), interne Synthesizer
- MIDI (Digital Instrumentation Digital Interface), interne Synthesizer
- Abspielen von MIDI-Dateien, internen Synthesizern
- Interne MIDI-Synthesizer
- Digital Instrumentation Digital Interface (MIDI), Ändern des Volumes
- MIDI (Digital Instrumentation Digital Interface), Ändern des Volumes
- Abspielen von MIDI-Dateien, Ändern des Volumes
- Ändern des MIDI-Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2369b13483ce6fa45d82ee177282a0de5e86538e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948711"
---
# <a name="changing-internal-midi-synthesizer-volume"></a><span data-ttu-id="60211-111">Ändern des internen MIDI-synthesizervolumes</span><span class="sxs-lookup"><span data-stu-id="60211-111">Changing Internal MIDI Synthesizer Volume</span></span>

<span data-ttu-id="60211-112">Windows stellt die folgenden Funktionen zum Abrufen und Festlegen der Volumeebene interner Geräte mit dem Typ "MIDI" bereit:</span><span class="sxs-lookup"><span data-stu-id="60211-112">Windows provides the following functions to retrieve and set the volume level of internal MIDI synthesizer devices:</span></span>



| <span data-ttu-id="60211-113">Wert</span><span class="sxs-lookup"><span data-stu-id="60211-113">Value</span></span>                                        | <span data-ttu-id="60211-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="60211-114">Meaning</span></span>                                                                       |
|----------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="60211-115">**midioutgetvolume**</span><span class="sxs-lookup"><span data-stu-id="60211-115">**midiOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume) | <span data-ttu-id="60211-116">Ruft die Volumeebene des angegebenen internen MIDI-Synthesizer-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="60211-116">Retrieves the volume level of the specified internal MIDI synthesizer device.</span></span> |
| [<span data-ttu-id="60211-117">**midioutsetvolume**</span><span class="sxs-lookup"><span data-stu-id="60211-117">**midiOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume) | <span data-ttu-id="60211-118">Legt die Volumeebene des angegebenen internen MIDI-Synthesizer-Geräts fest.</span><span class="sxs-lookup"><span data-stu-id="60211-118">Sets the volume level of the specified internal MIDI synthesizer device.</span></span>      |



 

<span data-ttu-id="60211-119">Nicht alle auf den Geräten mit der Ausgabe von "MIDI" ausgebene</span><span class="sxs-lookup"><span data-stu-id="60211-119">Not all MIDI output devices support volume changes.</span></span> <span data-ttu-id="60211-120">Einige Geräte können Änderungen einzelner Volumes sowohl auf dem linken als auch auf dem rechten Kanal unterstützen.</span><span class="sxs-lookup"><span data-stu-id="60211-120">Some devices can support individual volume changes on both the left and right channels.</span></span> <span data-ttu-id="60211-121">Informationen dazu, wie Sie feststellen können, ob ein bestimmtes Gerät volumeänderungen unterstützt, finden Sie unter [Abfragen von MIDI-Ausgabegeräten](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="60211-121">For information on how to determine if a particular device supports volume changes, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

<span data-ttu-id="60211-122">Sie sollten ein Audiogerät öffnen, bevor Sie das Volume ändern können, es sei denn, Ihre Anwendung ist als Master-Volumen Steuerungsanwendung konzipiert (bietet dem Benutzer eine volumesteuerung für alle Audiogeräte in einem System).</span><span class="sxs-lookup"><span data-stu-id="60211-122">Unless your application is designed to be a master volume-control application (provides the user with volume control for all audio devices in a system), you should open an audio device before changing its volume.</span></span> <span data-ttu-id="60211-123">Sie sollten auch die Volumeebene überprüfen, bevor Sie Sie ändern und die Volumeebene so bald wie möglich auf die vorherige Ebene wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="60211-123">You should also check the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="60211-124">Das Volume wird als Double Word-Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="60211-124">Volume is specified as a doubleword value.</span></span> <span data-ttu-id="60211-125">Die oberen 16 Bits geben das relative Volume des rechten Kanals an, und die unteren 16 Bits geben das relative Volume des linken Kanals an.</span><span class="sxs-lookup"><span data-stu-id="60211-125">The upper 16 bits specify the relative volume of the right channel, and the lower 16 bits specify the relative volume of the left channel.</span></span>

<span data-ttu-id="60211-126">Bei Geräten, die keine einzelnen volumeänderungen auf dem linken und rechten Kanal unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="60211-126">For devices that do not support individual volume changes on both the left and right channels, the lower 16 bits specify the volume level and the upper 16 bits are ignored.</span></span> <span data-ttu-id="60211-127">Werte für die Volumeebene liegen zwischen 0x0 (Ruhe) und 0xFFFF (maximales Volume) und werden logarithmisch interpretiert.</span><span class="sxs-lookup"><span data-stu-id="60211-127">Values for the volume level range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="60211-128">Die wahrgenommene Volumenzunahme ist gleich, wenn die Volumeebene von 0x5.000 auf 0x6000 erhöht wird, da Sie zwischen 0x4000 und 0x5.000 liegt.</span><span class="sxs-lookup"><span data-stu-id="60211-128">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 