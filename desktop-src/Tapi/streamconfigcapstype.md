---
description: Der "streamconfigcapstype"-Enumerationstyp wird von der TAPI \_ \_ -Struktur "Stream config \_ Caps" als Switch verwendet, um anzugeben, ob ein Audiostreaming oder Video Streaming beteiligt ist.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Streamconfigcapstype-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369304"
---
# <a name="streamconfigcapstype-enumeration"></a><span data-ttu-id="be32a-103">Streamconfigcapstype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="be32a-103">StreamConfigCapsType enumeration</span></span>

<span data-ttu-id="be32a-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be32a-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="be32a-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="be32a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="be32a-106">Der " **streamconfigcapstype** "-Enumerationstyp wird von der TAPI-Struktur " [**\_ Stream \_ config \_ Caps**](tapi-stream-config-caps.md) " als Switch verwendet, um anzugeben, ob ein Audiostreaming oder Video Streaming beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="be32a-106">The **StreamConfigCapsType** enumeration type is used by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure as a switch to indicate whether audio or video streaming is involved.</span></span>

## <a name="syntax"></a><span data-ttu-id="be32a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be32a-107">Syntax</span></span>


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a><span data-ttu-id="be32a-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="be32a-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="be32a-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**Audiostreamconfigcaps**</span><span class="sxs-lookup"><span data-stu-id="be32a-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="be32a-110">Audiostreamingkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="be32a-110">Audio streaming configuration.</span></span>

</dd> <dt>

<span data-ttu-id="be32a-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**Videostreamconfigcaps**</span><span class="sxs-lookup"><span data-stu-id="be32a-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="be32a-112">Videostreamingkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="be32a-112">Video streaming configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be32a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be32a-113">Requirements</span></span>



| <span data-ttu-id="be32a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be32a-114">Requirement</span></span> | <span data-ttu-id="be32a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="be32a-115">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="be32a-116">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="be32a-116">TAPI version</span></span><br/> | <span data-ttu-id="be32a-117">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="be32a-117">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="be32a-118">Header</span><span class="sxs-lookup"><span data-stu-id="be32a-118">Header</span></span><br/>       | <dl> <span data-ttu-id="be32a-119"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be32a-119"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be32a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be32a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be32a-121">**TAPI \_ - \_ streamkonfigurationscaps \_**</span><span class="sxs-lookup"><span data-stu-id="be32a-121">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




