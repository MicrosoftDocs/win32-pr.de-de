---
description: 'Weitere Informationen finden Sie hier: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524080"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="ce8fa-103">Pkey \_ audioendpoint \_ physicalspeakers</span><span class="sxs-lookup"><span data-stu-id="ce8fa-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="ce8fa-104">Die Eigenschaft " **pkey \_ audioendpoint \_ physicalspeakers** " gibt die Kanal konfigurationsmaske für das audioendpunktgerät an.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="ce8fa-105">Die Maske gibt die physische Konfiguration eines Satzes von Referenten an und gibt die Zuweisung von Kanälen zu Referenten an.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="ce8fa-106">Weitere Informationen zu kanalkonfigurationsmasken finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="ce8fa-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="ce8fa-107">Die Beschreibung der Eigenschaft "ksproperty \_ \_ AudioChannel \_ config" in der Windows-DDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="ce8fa-108">Das Whitepaper "audiotreiberunterstützung für Home-Theater-Sprecher-Konfigurationen" auf der Website " [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) ".</span><span class="sxs-lookup"><span data-stu-id="ce8fa-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="ce8fa-109">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="ce8fa-110">Der **uintval** -Member der **PROPVARIANT** -Struktur enthält eine kanalkonfigurationsmaske, die in den **uint**-Typ umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="ce8fa-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce8fa-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce8fa-111">Requirements</span></span>



| <span data-ttu-id="ce8fa-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce8fa-112">Requirement</span></span> | <span data-ttu-id="ce8fa-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ce8fa-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce8fa-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce8fa-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ce8fa-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce8fa-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce8fa-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce8fa-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ce8fa-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce8fa-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce8fa-118">Header</span><span class="sxs-lookup"><span data-stu-id="ce8fa-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce8fa-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce8fa-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce8fa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce8fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce8fa-121">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="ce8fa-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="ce8fa-122">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="ce8fa-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




