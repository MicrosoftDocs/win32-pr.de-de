---
description: Die Get-Methode ruft den Wert einer angegebenen audiogeräteeigenschaft ab.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: 'Itaudiodevicecontrol:: Get-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4311dc18291fcfbbe533dbe17042e6ba19c1122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372724"
---
# <a name="itaudiodevicecontrolget-method"></a><span data-ttu-id="91e29-103">Itaudiodevicecontrol:: Get-Methode</span><span class="sxs-lookup"><span data-stu-id="91e29-103">ITAudioDeviceControl::Get method</span></span>

<span data-ttu-id="91e29-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91e29-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="91e29-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="91e29-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="91e29-106">Die **Get** -Methode ruft den Wert einer angegebenen [**audiogeräteeigenschaft**](audiodeviceproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="91e29-106">The **Get** method retrieves the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="91e29-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e29-107">Syntax</span></span>


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a><span data-ttu-id="91e29-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="91e29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91e29-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="91e29-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91e29-110">Member der [**audiodeviceproperty**](audiodeviceproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="91e29-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="91e29-111">*plvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91e29-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91e29-112">Der Wert der input- *Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="91e29-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="91e29-113">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="91e29-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91e29-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="91e29-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91e29-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="91e29-115">Return value</span></span>

<span data-ttu-id="91e29-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="91e29-116">This method can return one of these values.</span></span>



| <span data-ttu-id="91e29-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="91e29-117">Return code</span></span>                                                                                   | <span data-ttu-id="91e29-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91e29-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="91e29-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91e29-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="91e29-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="91e29-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="91e29-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="91e29-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="91e29-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="91e29-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="91e29-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="91e29-123">Requirements</span></span>



| <span data-ttu-id="91e29-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="91e29-124">Requirement</span></span> | <span data-ttu-id="91e29-125">Wert</span><span class="sxs-lookup"><span data-stu-id="91e29-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="91e29-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="91e29-126">TAPI version</span></span><br/> | <span data-ttu-id="91e29-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="91e29-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="91e29-128">Header</span><span class="sxs-lookup"><span data-stu-id="91e29-128">Header</span></span><br/>       | <dl> <span data-ttu-id="91e29-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="91e29-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="91e29-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="91e29-130">Library</span></span><br/>      | <dl> <span data-ttu-id="91e29-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91e29-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="91e29-132">DLL</span><span class="sxs-lookup"><span data-stu-id="91e29-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="91e29-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91e29-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91e29-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91e29-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91e29-135">**Itaudiodebug econtrol**</span><span class="sxs-lookup"><span data-stu-id="91e29-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="91e29-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="91e29-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="91e29-137">**Audiodeviceproperty**</span><span class="sxs-lookup"><span data-stu-id="91e29-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




