---
title: Vorab Laden von Patches mit internen MIDI-Synthesizern
description: Vorab Laden von Patches mit internen MIDI-Synthesizern
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Digital Instrumentation Digital Interface (MIDI), interne Synthesizer
- MIDI (Digital Instrumentation Digital Interface), interne Synthesizer
- Abspielen von MIDI-Dateien, internen Synthesizern
- Interne MIDI-Synthesizer
- Digital Instrumentation Digital Interface (MIDI), vorab Laden von Patches
- MIDI (Digital Instrumentation Digital Interface), vorab Laden von Patches
- Abspielen von MIDI-Dateien, vorab Laden von Patches
- vorab Laden von MIDI-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948651"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a><span data-ttu-id="2c3cf-111">Vorab Laden von Patches mit internen MIDI-Synthesizern</span><span class="sxs-lookup"><span data-stu-id="2c3cf-111">Preloading Patches with Internal MIDI Synthesizers</span></span>

<span data-ttu-id="2c3cf-112">Bei einigen internen Geräten mit einem MIDI-Synthesizer können nicht alle Patches gleichzeitig geladen werden.</span><span class="sxs-lookup"><span data-stu-id="2c3cf-112">Some internal MIDI synthesizer devices cannot keep all of their patches loaded simultaneously.</span></span> <span data-ttu-id="2c3cf-113">Diese Geräte müssen die Patchdaten vorab laden.</span><span class="sxs-lookup"><span data-stu-id="2c3cf-113">These devices must preload their patch data.</span></span>

<span data-ttu-id="2c3cf-114">Windows stellt die folgenden Funktionen bereit, um anzufordern, dass ein Synthesizer bestimmte Patches vorab lädt und zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="2c3cf-114">Windows provides the following functions to request that a synthesizer preload and cache specified patches.</span></span>



| <span data-ttu-id="2c3cf-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2c3cf-115">Value</span></span>                                                      | <span data-ttu-id="2c3cf-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2c3cf-116">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c3cf-117">**midioutcachepatches**</span><span class="sxs-lookup"><span data-stu-id="2c3cf-117">**midiOutCachePatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | <span data-ttu-id="2c3cf-118">Fordert an, dass ein internes MIDI-Synthesizer-Gerät vorab geladen und zwischen angegebene melodische Patches zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="2c3cf-118">Requests that an internal MIDI synthesizer device preload and cache specified melodic patches.</span></span>              |
| [<span data-ttu-id="2c3cf-119">**midioutcachedrumpatches**</span><span class="sxs-lookup"><span data-stu-id="2c3cf-119">**midiOutCacheDrumPatches**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | <span data-ttu-id="2c3cf-120">Fordert an, dass ein internes MIDI-Synthesizer-Gerät bestimmte Schlüssel basierte Percussion-Patches vorab lädt und zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="2c3cf-120">Requests that an internal MIDI synthesizer device preload and cache specified key-based percussion patches.</span></span> |



 

<span data-ttu-id="2c3cf-121">Informationen dazu, wie Sie bestimmen können, ob ein bestimmtes Gerät das vorab Laden von Patches unterstützt, finden Sie unter [Abfragen von MIDI-Ausgabegeräten](querying-midi-output-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2c3cf-121">For information on how to determine if a particular device supports preloading patches, see [Querying MIDI Output Devices](querying-midi-output-devices.md).</span></span>

 

 