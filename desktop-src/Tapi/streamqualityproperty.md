---
description: 'Die streamqualityproperty-Enumeration, die von den itstreamqualitycontrol:: GetRange-, itstreamqualitycontrol:: Get-und itstreamqualitycontrol:: Set-Methoden verwendet wird, um anzugeben, welche Stream Quality-Eigenschaft adressiert wird.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Streamqualityproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362179"
---
# <a name="streamqualityproperty-enumeration"></a><span data-ttu-id="d7428-103">Streamqualityproperty-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d7428-103">StreamQualityProperty enumeration</span></span>

<span data-ttu-id="d7428-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d7428-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d7428-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="d7428-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d7428-106">Die **streamqualityproperty** -Enumeration, die von den [**itstreamqualitycontrol:: GetRange**](itstreamqualitycontrol-getrange.md)-, [**itstreamqualitycontrol:: Get**](itstreamqualitycontrol-get.md)-und [**itstreamqualitycontrol:: Set**](itstreamqualitycontrol-set.md) -Methoden verwendet wird, um anzugeben, welche Stream Quality-Eigenschaft adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="d7428-106">The **StreamQualityProperty** enum used by the [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md), and [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) methods to indicate the stream quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7428-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7428-107">Syntax</span></span>


```C++
} StreamQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="d7428-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d7428-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d7428-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**Streamquality- \_ maxbitrate**</span><span class="sxs-lookup"><span data-stu-id="d7428-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality\_MaxBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="d7428-110">Maximale Bitrate.</span><span class="sxs-lookup"><span data-stu-id="d7428-110">Maximum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="d7428-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**Streamquality- \_ currbitrate**</span><span class="sxs-lookup"><span data-stu-id="d7428-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality\_CurrBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="d7428-112">Minimale Bitrate.</span><span class="sxs-lookup"><span data-stu-id="d7428-112">Minimum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="d7428-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**Streamquality \_ minframeinterval**</span><span class="sxs-lookup"><span data-stu-id="d7428-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality\_MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="d7428-114">Maximales Frame Intervall.</span><span class="sxs-lookup"><span data-stu-id="d7428-114">Maximum frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="d7428-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**Streamquality \_ avgframeinterval**</span><span class="sxs-lookup"><span data-stu-id="d7428-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality\_AvgFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="d7428-116">Minimaler Frame Intervall.</span><span class="sxs-lookup"><span data-stu-id="d7428-116">Minimum frame interval.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7428-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7428-117">Requirements</span></span>



| <span data-ttu-id="d7428-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7428-118">Requirement</span></span> | <span data-ttu-id="d7428-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d7428-119">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7428-120">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="d7428-120">TAPI version</span></span><br/> | <span data-ttu-id="d7428-121">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="d7428-121">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="d7428-122">Header</span><span class="sxs-lookup"><span data-stu-id="d7428-122">Header</span></span><br/>       | <dl> <span data-ttu-id="d7428-123"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7428-123"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7428-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7428-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7428-125">**Itstreamqualitycontrol:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="d7428-125">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="d7428-126">**Itstreamqualitycontrol:: Get**</span><span class="sxs-lookup"><span data-stu-id="d7428-126">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="d7428-127">**Itstreamqualitycontrol:: Set**</span><span class="sxs-lookup"><span data-stu-id="d7428-127">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




