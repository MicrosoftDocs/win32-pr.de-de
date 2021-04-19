---
description: Die Get-Methode ruft den Wert einer angegebenen Stream Quality-Eigenschaft ab.
ms.assetid: a8b5b8c7-47c9-4561-be96-af8416d854dc
title: 'Itstreamqualitycontrol:: Get-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6758678dfacc8e0fe169189beaa8e890e801c907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356501"
---
# <a name="itstreamqualitycontrolget-method"></a><span data-ttu-id="e2a1d-103">Itstreamqualitycontrol:: Get-Methode</span><span class="sxs-lookup"><span data-stu-id="e2a1d-103">ITStreamQualityControl::Get method</span></span>

<span data-ttu-id="e2a1d-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e2a1d-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e2a1d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e2a1d-106">Die **Get** -Methode ruft den Wert einer angegebenen [**Stream Quality-Eigenschaft**](streamqualityproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-106">The **Get** method retrieves the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a1d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2a1d-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  StreamQualityProperty Property,
  [out] long                  *plValue,
  [out] TAPIControlFlags      *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e2a1d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2a1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2a1d-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2a1d-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2a1d-110">Member der [**streamqualityproperty**](streamqualityproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="e2a1d-111">*plvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2a1d-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2a1d-112">Der Wert der input- *Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="e2a1d-113">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2a1d-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2a1d-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2a1d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2a1d-115">Return value</span></span>

<span data-ttu-id="e2a1d-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-116">This method can return one of these values.</span></span>



| <span data-ttu-id="e2a1d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e2a1d-117">Return code</span></span>                                                                                   | <span data-ttu-id="e2a1d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2a1d-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e2a1d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e2a1d-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e2a1d-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e2a1d-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e2a1d-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e2a1d-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e2a1d-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e2a1d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2a1d-123">Requirements</span></span>



| <span data-ttu-id="e2a1d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2a1d-124">Requirement</span></span> | <span data-ttu-id="e2a1d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e2a1d-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a1d-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e2a1d-126">TAPI version</span></span><br/> | <span data-ttu-id="e2a1d-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="e2a1d-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="e2a1d-128">Header</span><span class="sxs-lookup"><span data-stu-id="e2a1d-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e2a1d-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2a1d-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e2a1d-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2a1d-130">Library</span></span><br/>      | <dl> <span data-ttu-id="e2a1d-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2a1d-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e2a1d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e2a1d-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="e2a1d-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2a1d-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a1d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2a1d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a1d-135">**Itstreamqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="e2a1d-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="e2a1d-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="e2a1d-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="e2a1d-137">**Streamqualityproperty**</span><span class="sxs-lookup"><span data-stu-id="e2a1d-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




