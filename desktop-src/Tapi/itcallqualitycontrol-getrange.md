---
description: Die GetRange-Methode ruft den Bereich der gültigen Werte für eine angegebene Eigenschaft zum Aufrufen der Qualität ab.
ms.assetid: 974033cf-59ce-4593-93d7-290094c20a7c
title: 'Itcallqualitycontrol:: GetRange-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd3941ee8d7d0605cc6fefc61963065e4e5ba57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372047"
---
# <a name="itcallqualitycontrolgetrange-method"></a><span data-ttu-id="332c3-103">Itcallqualitycontrol:: GetRange-Methode</span><span class="sxs-lookup"><span data-stu-id="332c3-103">ITCallQualityControl::GetRange method</span></span>

<span data-ttu-id="332c3-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="332c3-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="332c3-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="332c3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="332c3-106">Die **GetRange** -Methode ruft den Bereich der gültigen Werte für eine angegebene [Eigenschaft zum Aufrufen der Qualität](callqualityproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="332c3-106">The **GetRange** method gets the range of valid values for a given [call quality property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="332c3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="332c3-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  CallQualityProperty Property,
  [out] long                *plMin,
  [out] long                *plMax,
  [out] long                *plSteppingDelta,
  [out] long                *plDefault,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="332c3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="332c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="332c3-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="332c3-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="332c3-110">Member der [**callqualityproperty**](callqualityproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="332c3-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="332c3-111">*plmin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="332c3-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332c3-112">Der minimale gültige Wert für die Input-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="332c3-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="332c3-113">*plmax* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="332c3-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332c3-114">Maximal gültiger Wert für die Eingabe Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="332c3-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="332c3-115">*plsteppingdelta* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="332c3-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332c3-116">Inkrement, um den der Eigenschafts Wert vergrößert oder verkleinert werden kann.</span><span class="sxs-lookup"><span data-stu-id="332c3-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="332c3-117">*pldefault* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="332c3-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332c3-118">Der Standardwert für den *Property* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="332c3-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="332c3-119">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="332c3-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="332c3-120">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="332c3-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="332c3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="332c3-121">Return value</span></span>

<span data-ttu-id="332c3-122">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="332c3-122">This method can return one of these values.</span></span>



| <span data-ttu-id="332c3-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="332c3-123">Return code</span></span>                                                                                   | <span data-ttu-id="332c3-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="332c3-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="332c3-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="332c3-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="332c3-126">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="332c3-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="332c3-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="332c3-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="332c3-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="332c3-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="332c3-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="332c3-129">Requirements</span></span>



| <span data-ttu-id="332c3-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="332c3-130">Requirement</span></span> | <span data-ttu-id="332c3-131">Wert</span><span class="sxs-lookup"><span data-stu-id="332c3-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="332c3-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="332c3-132">TAPI version</span></span><br/> | <span data-ttu-id="332c3-133">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="332c3-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="332c3-134">Header</span><span class="sxs-lookup"><span data-stu-id="332c3-134">Header</span></span><br/>       | <dl> <span data-ttu-id="332c3-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="332c3-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="332c3-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="332c3-136">Library</span></span><br/>      | <dl> <span data-ttu-id="332c3-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="332c3-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="332c3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="332c3-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="332c3-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="332c3-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332c3-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="332c3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332c3-141">**Itcallqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="332c3-141">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="332c3-142">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="332c3-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="332c3-143">**Callqualityproperty**</span><span class="sxs-lookup"><span data-stu-id="332c3-143">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




