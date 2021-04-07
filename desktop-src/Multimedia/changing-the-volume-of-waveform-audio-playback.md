---
title: Ändern des Umfangs der Waveform-Audio Wiedergabe
description: Ändern des Umfangs der Waveform-Audio Wiedergabe
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- Wellenform-Audiodatei, Ändern des Wiedergabe Volumens
- Waveform-Audioschnittstelle, Ändern des Wiedergabe Volumens
- Wellenform-Audiodatei, Wiedergabe Volume
- Waveform-Audioschnittstelle, Wiedergabe Volume
- Ändern des Waveform-Audiowiedergabe-Volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727313"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a><span data-ttu-id="a8032-108">Ändern des Umfangs der Waveform-Audio Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="a8032-108">Changing the Volume of Waveform-Audio Playback</span></span>

<span data-ttu-id="a8032-109">Windows stellt die folgenden Funktionen bereit, um die Volumeebene von Waveform-audioausgabegeräten abzufragen und festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a8032-109">Windows provides the following functions to query and set the volume level of waveform-audio output devices.</span></span>



| <span data-ttu-id="a8032-110">Funktion</span><span class="sxs-lookup"><span data-stu-id="a8032-110">Function</span></span>                                     | <span data-ttu-id="a8032-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8032-111">Description</span></span>                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a8032-112">**waveoutgetvolume**</span><span class="sxs-lookup"><span data-stu-id="a8032-112">**waveOutGetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | <span data-ttu-id="a8032-113">Ruft die aktuelle Volumeebene des angegebenen Waveform-Audioausgabegeräts ab.</span><span class="sxs-lookup"><span data-stu-id="a8032-113">Retrieves the current volume level of the specified waveform-audio output device.</span></span> |
| [<span data-ttu-id="a8032-114">**waveoutsetvolume**</span><span class="sxs-lookup"><span data-stu-id="a8032-114">**waveOutSetVolume**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | <span data-ttu-id="a8032-115">Legt die Volumeebene des angegebenen Waveform-Audioausgabegeräts fest.</span><span class="sxs-lookup"><span data-stu-id="a8032-115">Sets the volume level of the specified waveform-audio output device.</span></span>              |



 

<span data-ttu-id="a8032-116">Nicht alle Waveform-Audiogeräte unterstützen volumeänderungen.</span><span class="sxs-lookup"><span data-stu-id="a8032-116">Not all waveform-audio devices support volume changes.</span></span> <span data-ttu-id="a8032-117">Einige Geräte unterstützen die einzelnen volumesteuerelemente sowohl im linken als auch im rechten Kanal.</span><span class="sxs-lookup"><span data-stu-id="a8032-117">Some devices support individual volume control on both the left and right channels.</span></span> <span data-ttu-id="a8032-118">Informationen zum Bestimmen der volumesteuerungsfunktionen von Waveform-Audiogeräten finden Sie unter [Geräte und Datentypen](devices-and-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="a8032-118">For information about how to determine the volume-control capabilities of waveform-audio devices, see [Devices and Data Types](devices-and-data-types.md).</span></span>

<span data-ttu-id="a8032-119">Einige Anwendungen ermöglichen es dem Benutzer, das Volume für alle Audiogeräte in einem System zu steuern.</span><span class="sxs-lookup"><span data-stu-id="a8032-119">Some applications allow the user to control the volume for all audio devices in a system.</span></span> <span data-ttu-id="a8032-120">(Viele Anwendungen dieses Typs verwenden die Audiomixer-Dienste. Weitere Informationen finden Sie unter [Audiomixer](audio-mixers.md).) Wenn Ihre Anwendung nicht in der Lage ist, eine solche Art von Master Volume zu steuern, sollten Sie vor dem Ändern des Volumes ein Audiogerät öffnen.</span><span class="sxs-lookup"><span data-stu-id="a8032-120">(Many applications of this type use the audio mixer services; for more information, see [Audio Mixers](audio-mixers.md).) Unless your application is capable of this kind of master volume control, you should open an audio device before changing its volume.</span></span> <span data-ttu-id="a8032-121">Sie sollten auch die Volumeebene Abfragen, bevor Sie Sie ändern und die Volumeebene so bald wie möglich auf die vorherige Ebene wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="a8032-121">You should also query the volume level before changing it and restore the volume level to its previous level as soon as possible.</span></span>

<span data-ttu-id="a8032-122">Das Volume wird in einem Double Word-Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="a8032-122">Volume is specified in a doubleword value.</span></span> <span data-ttu-id="a8032-123">Wenn das Audioformat Stereo ist, geben die oberen 16 Bits das relative Volume des rechten Kanals und die unteren 16 Bits das relative Volume des linken Kanals an.</span><span class="sxs-lookup"><span data-stu-id="a8032-123">When the audio format is stereo, the upper 16 bits specify the relative volume of the right channel and the lower 16 bits specify the relative volume of the left channel.</span></span> <span data-ttu-id="a8032-124">Bei Geräten, die die volumesteuerung auf der linken und rechten Channel nicht unterstützen, geben die unteren 16 Bits die Volumeebene an, und die oberen 16 Bits werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a8032-124">For devices that do not support left- and right-channel volume control, the lower 16 bits specify the volume level, and the upper 16 bits are ignored.</span></span>

<span data-ttu-id="a8032-125">Werte auf Volumeebene reichen von 0x0 (Ruhe) bis 0xFFFF (maximales Volume) und werden logarithmisch interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a8032-125">Volume-level values range from 0x0 (silence) to 0xFFFF (maximum volume) and are interpreted logarithmically.</span></span> <span data-ttu-id="a8032-126">Die wahrgenommene Volumenzunahme ist gleich, wenn die Volumeebene von 0x5.000 auf 0x6000 erhöht wird, da Sie zwischen 0x4000 und 0x5.000 liegt.</span><span class="sxs-lookup"><span data-stu-id="a8032-126">The perceived volume increase is the same when increasing the volume level from 0x5000 to 0x6000 as it is from 0x4000 to 0x5000.</span></span>

 

 