---
description: Mit der Get-Methode wird der Wert einer angegebenen Eigenschaft für die Eigenschaft "Callcenter" abgerufen.
ms.assetid: 0fec408e-2751-4c99-afe1-4337d22eff83
title: 'Itcallqualitycontrol:: Get-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea42768c173c0c073abe356e1ae6816a486a03c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358732"
---
# <a name="itcallqualitycontrolget-method"></a><span data-ttu-id="68ae8-103">Itcallqualitycontrol:: Get-Methode</span><span class="sxs-lookup"><span data-stu-id="68ae8-103">ITCallQualityControl::Get method</span></span>

<span data-ttu-id="68ae8-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68ae8-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="68ae8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="68ae8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="68ae8-106">Mit der **Get** -Methode wird der Wert einer angegebenen Eigenschaft für die [Eigenschaft "Callcenter" abgerufen](callqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="68ae8-106">The **Get** method gets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="68ae8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="68ae8-107">Syntax</span></span>


```C++
HRESULT Get(
  [in]  CallQualityProperty Property,
  [out] long                *plValue,
  [out] TAPIControlFlags    *plFlags
);
```



## <a name="parameters"></a><span data-ttu-id="68ae8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ae8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68ae8-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68ae8-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68ae8-110">Member der [**callqualityproperty**](callqualityproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="68ae8-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="68ae8-111">*plvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68ae8-111">*plValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68ae8-112">Der Wert der input- *Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="68ae8-112">Value of the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="68ae8-113">*plflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68ae8-113">*plFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68ae8-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der- *Eigenschafts* Wert gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="68ae8-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68ae8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68ae8-115">Return value</span></span>

<span data-ttu-id="68ae8-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68ae8-116">This method can return one of these values.</span></span>



| <span data-ttu-id="68ae8-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="68ae8-117">Return code</span></span>                                                                                   | <span data-ttu-id="68ae8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68ae8-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="68ae8-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68ae8-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="68ae8-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="68ae8-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="68ae8-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="68ae8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="68ae8-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68ae8-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="68ae8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68ae8-123">Requirements</span></span>



| <span data-ttu-id="68ae8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68ae8-124">Requirement</span></span> | <span data-ttu-id="68ae8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="68ae8-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="68ae8-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="68ae8-126">TAPI version</span></span><br/> | <span data-ttu-id="68ae8-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="68ae8-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="68ae8-128">Header</span><span class="sxs-lookup"><span data-stu-id="68ae8-128">Header</span></span><br/>       | <dl> <span data-ttu-id="68ae8-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="68ae8-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="68ae8-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68ae8-130">Library</span></span><br/>      | <dl> <span data-ttu-id="68ae8-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68ae8-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="68ae8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="68ae8-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="68ae8-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ae8-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68ae8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68ae8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ae8-135">**Itcallqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="68ae8-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="68ae8-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="68ae8-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="68ae8-137">**Callqualityproperty**</span><span class="sxs-lookup"><span data-stu-id="68ae8-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




