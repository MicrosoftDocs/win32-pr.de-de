---
description: Die GetRange-Methode ruft den Bereich der gültigen Werte für eine angegebene audiogeräteeigenschaft ab.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'Itaudiodevicecontrol:: GetRange-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351209"
---
# <a name="itaudiodevicecontrolgetrange-method"></a><span data-ttu-id="6f653-103">Itaudiodevicecontrol:: GetRange-Methode</span><span class="sxs-lookup"><span data-stu-id="6f653-103">ITAudioDeviceControl::GetRange method</span></span>

<span data-ttu-id="6f653-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6f653-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6f653-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6f653-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6f653-106">Die **GetRange** -Methode ruft den Bereich der gültigen Werte für eine angegebene [**audiogeräteeigenschaft**](audiodeviceproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="6f653-106">The **GetRange** method retrieves the range of valid values for a given [**audio device property**](audiodeviceproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f653-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f653-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="6f653-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f653-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f653-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f653-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f653-110">Member der [**audiodeviceproperty**](audiodeviceproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="6f653-110">Member of the [**AudioDeviceProperty**](audiodeviceproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="6f653-111">*plmin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f653-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f653-112">Der minimale gültige Wert für die Input-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6f653-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="6f653-113">*plmax* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f653-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f653-114">Maximal gültiger Wert für die Eingabe Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6f653-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="6f653-115">*plsteppingdelta* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f653-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f653-116">Inkrement, um den der Eigenschafts Wert vergrößert oder verkleinert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6f653-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="6f653-117">*pldefault* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f653-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f653-118">Der Standardwert für den *Property* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6f653-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6f653-119">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f653-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f653-120">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="6f653-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f653-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f653-121">Return value</span></span>

<span data-ttu-id="6f653-122">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6f653-122">This method can return one of these values.</span></span>



| <span data-ttu-id="6f653-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6f653-123">Return code</span></span>                                                                                   | <span data-ttu-id="6f653-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f653-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6f653-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f653-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6f653-126">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6f653-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6f653-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6f653-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6f653-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6f653-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6f653-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f653-129">Requirements</span></span>



| <span data-ttu-id="6f653-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f653-130">Requirement</span></span> | <span data-ttu-id="6f653-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6f653-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6f653-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6f653-132">TAPI version</span></span><br/> | <span data-ttu-id="6f653-133">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6f653-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="6f653-134">Header</span><span class="sxs-lookup"><span data-stu-id="6f653-134">Header</span></span><br/>       | <dl> <span data-ttu-id="6f653-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f653-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f653-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f653-136">Library</span></span><br/>      | <dl> <span data-ttu-id="6f653-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f653-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="6f653-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6f653-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="6f653-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f653-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f653-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f653-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f653-141">**Itaudiodebug econtrol**</span><span class="sxs-lookup"><span data-stu-id="6f653-141">**ITAudioDeviceControl**</span></span>](itaudiodevicecontrol.md)
</dt> <dt>

[<span data-ttu-id="6f653-142">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="6f653-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="6f653-143">**Audiodeviceproperty**</span><span class="sxs-lookup"><span data-stu-id="6f653-143">**AudioDeviceProperty**</span></span>](audiodeviceproperty.md)
</dt> </dl>

 

 




