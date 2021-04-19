---
description: Die Set-Methode legt den Wert einer bestimmten audiogeräteeigenschaft fest.
ms.assetid: 701cdfd4-9241-408c-8497-3983018e7da0
title: 'Itaudiodevicecontrol:: Set-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25aa3a6013ce79bdcea5345dcc00f52c96c8a8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366913"
---
# <a name="itaudiodevicecontrolset-method"></a><span data-ttu-id="f9418-103">Itaudiodevicecontrol:: Set-Methode</span><span class="sxs-lookup"><span data-stu-id="f9418-103">ITAudioDeviceControl::Set method</span></span>

<span data-ttu-id="f9418-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9418-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f9418-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="f9418-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f9418-106">Die **Set** -Methode legt den Wert einer bestimmten [**audiogeräteeigenschaft**](audiodeviceproperty.md)fest.</span><span class="sxs-lookup"><span data-stu-id="f9418-106">The **Set** method sets the value of a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9418-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9418-107">Syntax</span></span>


```C++
HRESULT get_Error(
  [out] HRESULT *phrErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="f9418-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9418-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9418-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9418-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9418-110">Member der [**audiodeviceproperty**](audiodeviceproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="f9418-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="f9418-111">*Lvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9418-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9418-112">Der gewünschte Wert für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f9418-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="f9418-113">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9418-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9418-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der *Eigenschafts* Wert gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9418-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9418-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9418-115">Return value</span></span>

<span data-ttu-id="f9418-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f9418-116">This method can return one of these values.</span></span>



| <span data-ttu-id="f9418-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f9418-117">Return code</span></span>                                                                                   | <span data-ttu-id="f9418-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9418-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f9418-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9418-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f9418-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f9418-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f9418-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f9418-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f9418-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f9418-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f9418-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9418-123">Requirements</span></span>



| <span data-ttu-id="f9418-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9418-124">Requirement</span></span> | <span data-ttu-id="f9418-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f9418-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9418-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="f9418-126">TAPI version</span></span><br/> | <span data-ttu-id="f9418-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f9418-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="f9418-128">Header</span><span class="sxs-lookup"><span data-stu-id="f9418-128">Header</span></span><br/>       | <dl> <span data-ttu-id="f9418-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9418-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9418-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9418-130">Library</span></span><br/>      | <dl> <span data-ttu-id="f9418-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9418-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f9418-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f9418-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="f9418-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9418-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9418-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9418-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9418-135">**Itaudiodebug econtrol**</span><span class="sxs-lookup"><span data-stu-id="f9418-135">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="f9418-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="f9418-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="f9418-137">**Audiodeviceproperty**</span><span class="sxs-lookup"><span data-stu-id="f9418-137">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




