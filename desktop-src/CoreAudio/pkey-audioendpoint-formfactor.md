---
description: Die pkey \_ audioendpoint \_ FormFactor-Eigenschaft gibt den Formfaktor des audioendpunktgeräts an. Der Formular Faktor gibt die physischen Attribute des audioendpunktgeräts an, das der Benutzer bearbeitet.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483683"
---
# <a name="pkey_audioendpoint_formfactor"></a><span data-ttu-id="f61c4-104">Pkey- \_ audioendpoint- \_ FormFactor</span><span class="sxs-lookup"><span data-stu-id="f61c4-104">PKEY\_AudioEndpoint\_FormFactor</span></span>

<span data-ttu-id="f61c4-105">Die **pkey \_ audioendpoint \_ FormFactor** -Eigenschaft gibt den Formfaktor des audioendpunktgeräts an.</span><span class="sxs-lookup"><span data-stu-id="f61c4-105">The **PKEY\_AudioEndpoint\_FormFactor** property specifies the form factor of the audio endpoint device.</span></span> <span data-ttu-id="f61c4-106">Der Formular Faktor gibt die physischen Attribute des audioendpunktgeräts an, das der Benutzer bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="f61c4-106">The form factor indicates the physical attributes of the audio endpoint device that the user manipulates.</span></span>

<span data-ttu-id="f61c4-107">Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f61c4-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="f61c4-108">Der **uintval** -Member der **PROPVARIANT** -Struktur enthält einen Enumerationswert, der in den uint-Typ umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="f61c4-108">The **uintVal** member of the **PROPVARIANT** structure contains an enumeration value that is cast to type UINT.</span></span> <span data-ttu-id="f61c4-109">Sie wird auf einen der folgenden [**endpointformfactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) -Enumerationswerte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="f61c4-109">It is set to one of the following [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) enumeration values:</span></span>

-   <span data-ttu-id="f61c4-110">Remotenetworkdevice</span><span class="sxs-lookup"><span data-stu-id="f61c4-110">RemoteNetworkDevice</span></span>
-   <span data-ttu-id="f61c4-111">Speakers</span><span class="sxs-lookup"><span data-stu-id="f61c4-111">Speakers</span></span>
-   <span data-ttu-id="f61c4-112">Linelevel</span><span class="sxs-lookup"><span data-stu-id="f61c4-112">LineLevel</span></span>
-   <span data-ttu-id="f61c4-113">Aufgesetzt</span><span class="sxs-lookup"><span data-stu-id="f61c4-113">Headphones</span></span>
-   <span data-ttu-id="f61c4-114">Mikrofon</span><span class="sxs-lookup"><span data-stu-id="f61c4-114">Microphone</span></span>
-   <span data-ttu-id="f61c4-115">Headset</span><span class="sxs-lookup"><span data-stu-id="f61c4-115">Headset</span></span>
-   <span data-ttu-id="f61c4-116">Ge</span><span class="sxs-lookup"><span data-stu-id="f61c4-116">Handset</span></span>
-   <span data-ttu-id="f61c4-117">Unknowndigitalpassthrough</span><span class="sxs-lookup"><span data-stu-id="f61c4-117">UnknownDigitalPassthrough</span></span>
-   <span data-ttu-id="f61c4-118">SPDIF</span><span class="sxs-lookup"><span data-stu-id="f61c4-118">SPDIF</span></span>
-   <span data-ttu-id="f61c4-119">HDMI</span><span class="sxs-lookup"><span data-stu-id="f61c4-119">HDMI</span></span>
-   <span data-ttu-id="f61c4-120">Unknownformfactor</span><span class="sxs-lookup"><span data-stu-id="f61c4-120">UnknownFormFactor</span></span>

## <a name="requirements"></a><span data-ttu-id="f61c4-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f61c4-121">Requirements</span></span>



| <span data-ttu-id="f61c4-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f61c4-122">Requirement</span></span> | <span data-ttu-id="f61c4-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f61c4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61c4-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f61c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f61c4-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f61c4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f61c4-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f61c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f61c4-127">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f61c4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f61c4-128">Header</span><span class="sxs-lookup"><span data-stu-id="f61c4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61c4-129"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61c4-129"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f61c4-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f61c4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61c4-131">**Eigenschaften des audioendpunkts**</span><span class="sxs-lookup"><span data-stu-id="f61c4-131">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="f61c4-132">Kernaudioeigenschaften</span><span class="sxs-lookup"><span data-stu-id="f61c4-132">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




