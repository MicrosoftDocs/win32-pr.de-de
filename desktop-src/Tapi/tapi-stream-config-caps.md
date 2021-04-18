---
description: Die Struktur der TAPI \_ -Stream-Konfigurations Ober \_ \_ Grenzen enthält entweder Video-oder audiodatenstream-Konfigurationsinformationen.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS Struktur (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357709"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="7f806-103">Struktur der TAPI- \_ \_ streamkonfigurationscaps \_</span><span class="sxs-lookup"><span data-stu-id="7f806-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="7f806-104">\[ Diese Struktur ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f806-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7f806-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7f806-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7f806-106">Die Struktur der TAPI-Stream-Konfigurations Ober **\_ \_ \_ Grenzen** enthält entweder Video-oder audiodatenstream-Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="7f806-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f806-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f806-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="7f806-108">Member</span><span class="sxs-lookup"><span data-stu-id="7f806-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f806-109">**Capstype**</span><span class="sxs-lookup"><span data-stu-id="7f806-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="7f806-110">Definiert, ob das Unionmember Video-oder Audioinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7f806-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="7f806-111">**VideoCap**</span><span class="sxs-lookup"><span data-stu-id="7f806-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="7f806-112">Eine [**TAPI \_ - \_ Dateistream- \_ config \_**](tapi-video-stream-config-caps.md) -Struktur, die die videostreamfunktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="7f806-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="7f806-113">**Audiocap**</span><span class="sxs-lookup"><span data-stu-id="7f806-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="7f806-114">Eine [**TAPI \_ -Daten \_ Strom- \_ config \_ -**](tapi-audio-stream-config-caps.md) Struktur, die die audiostreamfunktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="7f806-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7f806-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f806-115">Requirements</span></span>



| <span data-ttu-id="7f806-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f806-116">Requirement</span></span> | <span data-ttu-id="7f806-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7f806-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f806-118">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="7f806-118">TAPI version</span></span><br/> | <span data-ttu-id="7f806-119">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7f806-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="7f806-120">Header</span><span class="sxs-lookup"><span data-stu-id="7f806-120">Header</span></span><br/>       | <dl> <span data-ttu-id="7f806-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f806-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f806-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f806-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f806-123">**Itformatcontrol:: getstreamcaps**</span><span class="sxs-lookup"><span data-stu-id="7f806-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="7f806-124">**Streamconfigcapstype**</span><span class="sxs-lookup"><span data-stu-id="7f806-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="7f806-125">**TAPI- \_ Video Daten \_ Strom- \_ Konfigurations \_ Caps**</span><span class="sxs-lookup"><span data-stu-id="7f806-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="7f806-126">**TAPI \_ - \_ Audiodatenstrom- \_ Konfigurations \_ Caps**</span><span class="sxs-lookup"><span data-stu-id="7f806-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




