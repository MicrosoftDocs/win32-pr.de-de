---
title: Ändern der Menge an zusätzlichen Audio-Devices
description: Ändern der Menge an zusätzlichen Audio-Devices
ms.assetid: d7357900-132c-4758-8bc2-a890aead01c3
keywords:
- Wellenform-Audiodatei, Ändern des zusätzlichen audiogerätevolumes
- Ändern des Volumes mit zusätzlichen Audiogeräten
- zusätzliches Audiomaterial, Ändern des Geräte Volumes
- hilfsaudioschnittstelle
- zusätzliche Audiogeräte, Ändern des Volumes
- zusätzliches Audiomaterial, Schnittstelle
- zusätzliches Audiogerät, Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f80c499f18b60f0919214c91eeec834ed72c3e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727320"
---
# <a name="changing-the-volume-of-auxiliary-audio-devices"></a><span data-ttu-id="788dc-110">Ändern der Menge an zusätzlichen Audio-Devices</span><span class="sxs-lookup"><span data-stu-id="788dc-110">Changing the Volume of Auxiliary Audio-Devices</span></span>

<span data-ttu-id="788dc-111">Windows stellt die folgenden Funktionen zum Abfragen und Festlegen des Volumes für hilfaudiogeräte bereit.</span><span class="sxs-lookup"><span data-stu-id="788dc-111">Windows provides the following functions to query and set the volume for auxiliary audio devices.</span></span>



| <span data-ttu-id="788dc-112">Funktion</span><span class="sxs-lookup"><span data-stu-id="788dc-112">Function</span></span>                             | <span data-ttu-id="788dc-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="788dc-113">Description</span></span>                                                                    |
|--------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="788dc-114">**"auxgetvolume"**</span><span class="sxs-lookup"><span data-stu-id="788dc-114">**auxGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume) | <span data-ttu-id="788dc-115">Ruft die aktuelle volumeeinstellung des angegebenen zusätzlichen Ausgabegeräts ab.</span><span class="sxs-lookup"><span data-stu-id="788dc-115">Retrieves the current volume setting of the specified auxiliary output device.</span></span> |
| [<span data-ttu-id="788dc-116">**"auxsetvolume"**</span><span class="sxs-lookup"><span data-stu-id="788dc-116">**auxSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume) | <span data-ttu-id="788dc-117">Legt das Volume des angegebenen zusätzlichen Ausgabegeräts fest.</span><span class="sxs-lookup"><span data-stu-id="788dc-117">Sets the volume of the specified auxiliary output device.</span></span>                      |



 

<span data-ttu-id="788dc-118">Nicht alle zusätzlichen Audiogeräte unterstützen volumeänderungen.</span><span class="sxs-lookup"><span data-stu-id="788dc-118">Not all auxiliary audio devices support volume changes.</span></span> <span data-ttu-id="788dc-119">Einige Geräte können Änderungen einzelner Volumes sowohl auf der linken Seite als auch auf den rechten Kanälen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="788dc-119">Some devices can support individual volume changes on both the left and the right channels.</span></span>

<span data-ttu-id="788dc-120">Das Volume wird in einem Double Word-Wert angegeben, wie mit den volumesteuerungfunktionen Waveform-Audiofunktionen und MIDI.</span><span class="sxs-lookup"><span data-stu-id="788dc-120">Volume is specified in a doubleword value, as with the waveform-audio and MIDI volume-control functions.</span></span> <span data-ttu-id="788dc-121">Wenn das Audioformat Stereo ist, geben die oberen 16 Bits das relative Volume des rechten Kanals und die unteren 16 Bits das relative Volume des linken Kanals an.</span><span class="sxs-lookup"><span data-stu-id="788dc-121">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="788dc-122">Bei Geräten, die die volumesteuerung auf der linken und rechten Channel nicht unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="788dc-122">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="788dc-123">Werte auf Volumeebene reichen von 0x0 (Ruhe) bis 0xFFFF (maximales Volume) und werden logarithmisch interpretiert.</span><span class="sxs-lookup"><span data-stu-id="788dc-123">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="788dc-124">Die wahrgenommene Volumenzunahme ist gleich, wenn die Volumeebene von 0x5.000 auf 0x6000 erhöht wird, da Sie zwischen 0x4000 und 0x5.000 liegt.</span><span class="sxs-lookup"><span data-stu-id="788dc-124">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 