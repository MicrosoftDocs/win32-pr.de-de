---
description: Die GetRange-Methode ruft den Bereich der gültigen Werte für eine angegebene Eigenschaft der Streamqualität ab.
ms.assetid: 8c5e4652-1a40-4d7d-aa89-606e979dc03d
title: 'Itstreamqualitycontrol:: GetRange-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea8b20c2617eb0fe54ccc4603997464fca25f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372412"
---
# <a name="itstreamqualitycontrolgetrange-method"></a><span data-ttu-id="6c6fe-103">Itstreamqualitycontrol:: GetRange-Methode</span><span class="sxs-lookup"><span data-stu-id="6c6fe-103">ITStreamQualityControl::GetRange method</span></span>

<span data-ttu-id="6c6fe-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6c6fe-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6c6fe-106">Die **GetRange** -Methode ruft den Bereich der gültigen Werte für eine angegebene [**Eigenschaft der Streamqualität**](streamqualityproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-106">The **GetRange** method gets the range of valid values for a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c6fe-107">Syntax</span></span>


```C++
HRESULT GetRange(
  [in]  StreamQualityProperty Property,
  [out] long                  *plMin,
  [out] long                  *plMax,
  [out] long                  *plSteppingDelta,
  [out] long                  *plDefault,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6c6fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c6fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6fe-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6fe-110">Member der [**streamqualityproperty**](streamqualityproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="6c6fe-111">*plmin* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-111">*plMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6fe-112">Der minimale gültige Wert für die Input-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-112">Minimum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="6c6fe-113">*plmax* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-113">*plMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6fe-114">Maximal gültiger Wert für die Eingabe Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-114">Maximum valid value for the input property.</span></span>

</dd> <dt>

<span data-ttu-id="6c6fe-115">*plsteppingdelta* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-115">*plSteppingDelta* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6fe-116">Inkrement, um den der Eigenschafts Wert vergrößert oder verkleinert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-116">Increment by which the property value can be increased or decreased.</span></span>

</dd> <dt>

<span data-ttu-id="6c6fe-117">*pldefault* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-117">*plDefault* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6fe-118">Der Standardwert für den *Property* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-118">Default value for the *Property* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6c6fe-119">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6c6fe-119">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6fe-120">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-120">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6fe-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c6fe-121">Return value</span></span>

<span data-ttu-id="6c6fe-122">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-122">This method can return one of these values.</span></span>



| <span data-ttu-id="6c6fe-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c6fe-123">Return code</span></span>                                                                                   | <span data-ttu-id="6c6fe-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c6fe-124">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6c6fe-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c6fe-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6c6fe-126">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-126">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6c6fe-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6c6fe-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6c6fe-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6c6fe-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c6fe-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c6fe-129">Requirements</span></span>



| <span data-ttu-id="6c6fe-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c6fe-130">Requirement</span></span> | <span data-ttu-id="6c6fe-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6c6fe-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6fe-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6c6fe-132">TAPI version</span></span><br/> | <span data-ttu-id="6c6fe-133">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="6c6fe-133">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="6c6fe-134">Header</span><span class="sxs-lookup"><span data-stu-id="6c6fe-134">Header</span></span><br/>       | <dl> <span data-ttu-id="6c6fe-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6fe-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c6fe-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c6fe-136">Library</span></span><br/>      | <dl> <span data-ttu-id="6c6fe-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c6fe-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="6c6fe-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6c6fe-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="6c6fe-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c6fe-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6fe-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c6fe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6fe-141">**Itstreamqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="6c6fe-141">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="6c6fe-142">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="6c6fe-142">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="6c6fe-143">**Streamqualityproperty**</span><span class="sxs-lookup"><span data-stu-id="6c6fe-143">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




