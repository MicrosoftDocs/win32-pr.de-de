---
description: Die GetRange-Methode ruft den Bereich gültiger Werte für eine angegebene audioeinstellungs Eigenschaft ab.
ms.assetid: 09ee0c59-6ae6-47eb-a8cf-6b24e759d7fb
title: 'Itaudiosettings:: GetRange-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91dd4d7bed3134c17de9c5958c7e6184cd51918e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369425"
---
# <a name="itaudiosettingsgetrange-method"></a><span data-ttu-id="6b01f-103">Itaudiosettings:: GetRange-Methode</span><span class="sxs-lookup"><span data-stu-id="6b01f-103">ITAudioSettings::GetRange method</span></span>

<span data-ttu-id="6b01f-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b01f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6b01f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6b01f-106">Die **GetRange** -Methode ruft den Bereich gültiger Werte für eine angegebene [**audioeinstellungs Eigenschaft**](audiosettingsproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="6b01f-106">The **GetRange** method retrieves the range of valid values for a given [**audio settings property**](audiosettingsproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b01f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b01f-107">Syntax</span></span>


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a><span data-ttu-id="6b01f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b01f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b01f-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b01f-110">Member der [**audiosettingsproperty**](audiosettingsproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="6b01f-110">Member of the [**AudioSettingsProperty**](audiosettingsproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="6b01f-111">*plmin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b01f-112">Der minimale gültige Wert für die Input-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6b01f-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="6b01f-113">*plmax* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b01f-114">Maximal gültiger Wert für die Eingabe Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6b01f-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="6b01f-115">*plsteppingdelta* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b01f-116">Inkrement, um den der Eigenschafts Wert vergrößert oder verkleinert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6b01f-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="6b01f-117">*pldefault* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b01f-118">Der Standardwert für den *Property* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b01f-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6b01f-119">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b01f-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b01f-120">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="6b01f-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b01f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b01f-121">Return value</span></span>

<span data-ttu-id="6b01f-122">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6b01f-122">This method can return one of these values.</span></span>



| <span data-ttu-id="6b01f-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b01f-123">Return code</span></span>                                                                                   | <span data-ttu-id="6b01f-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b01f-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6b01f-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b01f-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6b01f-126">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6b01f-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6b01f-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6b01f-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6b01f-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6b01f-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6b01f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b01f-129">Requirements</span></span>



| <span data-ttu-id="6b01f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b01f-130">Requirement</span></span> | <span data-ttu-id="6b01f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6b01f-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6b01f-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6b01f-132">TAPI version</span></span><br/> | <span data-ttu-id="6b01f-133">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6b01f-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="6b01f-134">Header</span><span class="sxs-lookup"><span data-stu-id="6b01f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="6b01f-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b01f-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b01f-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6b01f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="6b01f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b01f-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="6b01f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6b01f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="6b01f-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b01f-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b01f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b01f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b01f-141">**Itaudiosettings**</span><span class="sxs-lookup"><span data-stu-id="6b01f-141">**ITAudioSettings**</span></span>](itaudiosettings.md)
</dt> <dt>

[<span data-ttu-id="6b01f-142">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="6b01f-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="6b01f-143">**Audiosettingsproperty**</span><span class="sxs-lookup"><span data-stu-id="6b01f-143">**AudioSettingsProperty**</span></span>](audiosettingsproperty.md)
</dt> </dl>

 

 




