---
description: 'Die callqualityproperty-Enumeration wird von den Methoden itcallqualitycontrol:: GetRange, itcallqualitycontrol:: Get und itcallqualitycontrol:: Set verwendet, um anzugeben, dass die Eigenschaft Anruf Qualität adressiert wird.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Callqualityproperty-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361540"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="04d63-103">Callqualityproperty-Enumeration</span><span class="sxs-lookup"><span data-stu-id="04d63-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="04d63-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="04d63-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="04d63-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="04d63-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="04d63-106">Die **callqualityproperty** -Enumeration wird von den Methoden [**itcallqualitycontrol:: GetRange**](itcallqualitycontrol-getrange.md), [**itcallqualitycontrol:: Get**](itcallqualitycontrol-get.md)und [**itcallqualitycontrol:: Set**](itcallqualitycontrol-set.md) verwendet, um anzugeben, dass die Eigenschaft Anruf Qualität adressiert wird.</span><span class="sxs-lookup"><span data-stu-id="04d63-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d63-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="04d63-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="04d63-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="04d63-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="04d63-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**Callquality- \_ controlinterval**</span><span class="sxs-lookup"><span data-stu-id="04d63-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-110">Steuerungs Intervall.</span><span class="sxs-lookup"><span data-stu-id="04d63-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**Callquality- \_ confbitrate**</span><span class="sxs-lookup"><span data-stu-id="04d63-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-112">Bitrate für die Konferenz.</span><span class="sxs-lookup"><span data-stu-id="04d63-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**Callquality \_ maxinputbitrate**</span><span class="sxs-lookup"><span data-stu-id="04d63-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-114">Maximale Eingabe Bitrate.</span><span class="sxs-lookup"><span data-stu-id="04d63-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**Callquality \_ currinputbitrate**</span><span class="sxs-lookup"><span data-stu-id="04d63-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-116">Aktuelle Eingabe Bitrate.</span><span class="sxs-lookup"><span data-stu-id="04d63-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**Callquality \_ maxoutputbitrate**</span><span class="sxs-lookup"><span data-stu-id="04d63-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-118">Maximale Ausgabe Bitrate.</span><span class="sxs-lookup"><span data-stu-id="04d63-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**Callquality- \_ Cursor Cursor-Bitrate**</span><span class="sxs-lookup"><span data-stu-id="04d63-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-120">Aktuelle Ausgabe Bitrate.</span><span class="sxs-lookup"><span data-stu-id="04d63-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**Callquality \_ maxcpuload**</span><span class="sxs-lookup"><span data-stu-id="04d63-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-122">Maximale CPU-Auslastung.</span><span class="sxs-lookup"><span data-stu-id="04d63-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="04d63-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**Callquality \_ currcpuload**</span><span class="sxs-lookup"><span data-stu-id="04d63-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="04d63-124">Aktuelle CPU-Auslastung.</span><span class="sxs-lookup"><span data-stu-id="04d63-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04d63-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04d63-125">Requirements</span></span>



| <span data-ttu-id="04d63-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04d63-126">Requirement</span></span> | <span data-ttu-id="04d63-127">Wert</span><span class="sxs-lookup"><span data-stu-id="04d63-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="04d63-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="04d63-128">TAPI version</span></span><br/> | <span data-ttu-id="04d63-129">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="04d63-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="04d63-130">Header</span><span class="sxs-lookup"><span data-stu-id="04d63-130">Header</span></span><br/>       | <dl> <span data-ttu-id="04d63-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d63-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d63-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04d63-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d63-133">**Itcallqualitycontrol:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="04d63-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="04d63-134">**Itcallqualitycontrol:: Get**</span><span class="sxs-lookup"><span data-stu-id="04d63-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="04d63-135">**Itcallqualitycontrol:: Set**</span><span class="sxs-lookup"><span data-stu-id="04d63-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




