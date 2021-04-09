---
title: Activebasicdevice geteffectivebandwidth-Methode (playondevice. h)
description: Ruft die aktuelle effektive Bandbreite für das Gerät ab.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- Geteffectivebandwidth-Methode Medien Streaming-API
- Geteffectivebandwidth-Methode Medien Streaming-API, activebasicdevice-Schnittstelle
- Activebasicdevice-Schnittstelle Medien Streaming-API, geteffectivebandwidth-Methode
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040959"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="cb32c-106">Activebasicdevice:: geteffectivebandwidth-Methode</span><span class="sxs-lookup"><span data-stu-id="cb32c-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="cb32c-107">Ruft die aktuelle effektive Bandbreite für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="cb32c-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb32c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb32c-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="cb32c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb32c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb32c-110">*transmitspeed* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="cb32c-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cb32c-111">Gibt an, ob die Übertragungsgeschwindigkeit abgerufen oder die Empfangs Geschwindigkeit abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cb32c-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="cb32c-112">" **true** ", um die Übertragungsgeschwindigkeit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cb32c-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="cb32c-113">**false** zum Abrufen der Empfangs Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="cb32c-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="cb32c-114">*currentspeed* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cb32c-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb32c-115">Empfängt die aktuelle effektive Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="cb32c-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb32c-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb32c-116">Return value</span></span>

<span data-ttu-id="cb32c-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="cb32c-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cb32c-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb32c-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb32c-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb32c-119">Requirements</span></span>



| <span data-ttu-id="cb32c-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb32c-120">Requirement</span></span> | <span data-ttu-id="cb32c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="cb32c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb32c-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb32c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb32c-123">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="cb32c-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb32c-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb32c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb32c-125">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb32c-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb32c-126">Header</span><span class="sxs-lookup"><span data-stu-id="cb32c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb32c-127"><dt>Playondevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb32c-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb32c-128">IDL</span><span class="sxs-lookup"><span data-stu-id="cb32c-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb32c-129"><dt>Playto Device. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb32c-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="cb32c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cb32c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb32c-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb32c-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb32c-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb32c-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb32c-133">[**Activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb32c-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

