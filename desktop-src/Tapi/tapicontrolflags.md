---
description: Die tapicontrolflags-Enumeration wird von einer Reihe von Methoden verwendet, um anzugeben, ob eine bestimmte Eigenschaft automatisch oder manuell gesteuert wird.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Tapicontrolflags-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356038"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="11545-103">Tapicontrolflags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="11545-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="11545-104">\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="11545-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="11545-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="11545-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="11545-106">Die **tapicontrolflags** -Enumeration wird von einer Reihe von Methoden verwendet, um anzugeben, ob eine bestimmte Eigenschaft automatisch oder manuell gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="11545-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="11545-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="11545-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="11545-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="11545-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11545-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**Tapicontrol- \_ Flags " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="11545-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="11545-110">TAPI weist keine steuerungflags für die Eigenschaft auf.</span><span class="sxs-lookup"><span data-stu-id="11545-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="11545-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**Tapicontrol- \_ Flags \_ automatisch**</span><span class="sxs-lookup"><span data-stu-id="11545-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="11545-112">Die-Eigenschaft wird automatisch gesteuert.</span><span class="sxs-lookup"><span data-stu-id="11545-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="11545-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**Tapicontrol- \_ Flags \_ manuell**</span><span class="sxs-lookup"><span data-stu-id="11545-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="11545-114">Die-Eigenschaft wird manuell gesteuert.</span><span class="sxs-lookup"><span data-stu-id="11545-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11545-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11545-115">Requirements</span></span>



| <span data-ttu-id="11545-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11545-116">Requirement</span></span> | <span data-ttu-id="11545-117">Wert</span><span class="sxs-lookup"><span data-stu-id="11545-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11545-118">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="11545-118">TAPI version</span></span><br/> | <span data-ttu-id="11545-119">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="11545-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="11545-120">Header</span><span class="sxs-lookup"><span data-stu-id="11545-120">Header</span></span><br/>       | <dl> <span data-ttu-id="11545-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="11545-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11545-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11545-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11545-123">**Itaudiodebug econtrol:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="11545-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="11545-124">**Itaudiodebug econtrol:: Get**</span><span class="sxs-lookup"><span data-stu-id="11545-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="11545-125">**Itaudiode vicecontrol:: Set**</span><span class="sxs-lookup"><span data-stu-id="11545-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="11545-126">**Itaudiosettings:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="11545-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="11545-127">**Itaudiosettings:: Get**</span><span class="sxs-lookup"><span data-stu-id="11545-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="11545-128">**Itaudiosettings:: Set**</span><span class="sxs-lookup"><span data-stu-id="11545-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="11545-129">**Itcallqualitycontrol:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="11545-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="11545-130">**Itcallqualitycontrol:: Get**</span><span class="sxs-lookup"><span data-stu-id="11545-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="11545-131">**Itcallqualitycontrol:: Set**</span><span class="sxs-lookup"><span data-stu-id="11545-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="11545-132">**Itstreamqualitycontrol:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="11545-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="11545-133">**Itstreamqualitycontrol:: Get**</span><span class="sxs-lookup"><span data-stu-id="11545-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="11545-134">**Itstreamqualitycontrol:: Set**</span><span class="sxs-lookup"><span data-stu-id="11545-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




