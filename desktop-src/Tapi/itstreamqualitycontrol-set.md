---
description: Die Set-Methode legt den Wert einer angegebenen Eigenschaft für die Streamqualität fest.
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'Itstreamqualitycontrol:: Set-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372411"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="41890-103">Itstreamqualitycontrol:: Set-Methode</span><span class="sxs-lookup"><span data-stu-id="41890-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="41890-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41890-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="41890-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="41890-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="41890-106">Die **Set** -Methode legt den Wert einer angegebenen [**Eigenschaft für die Streamqualität**](streamqualityproperty.md)fest.</span><span class="sxs-lookup"><span data-stu-id="41890-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="41890-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="41890-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="41890-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="41890-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41890-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41890-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41890-110">Member der [**streamqualityproperty**](streamqualityproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="41890-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="41890-111">*Lvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41890-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41890-112">Gewünschter Wert für die input- *Eigenschaft*.</span><span class="sxs-lookup"><span data-stu-id="41890-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="41890-113">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41890-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41890-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der *Eigenschafts* Wert gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="41890-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41890-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41890-115">Return value</span></span>

<span data-ttu-id="41890-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="41890-116">This method can return one of these values.</span></span>



| <span data-ttu-id="41890-117">Wert</span><span class="sxs-lookup"><span data-stu-id="41890-117">Value</span></span>                                                                                         | <span data-ttu-id="41890-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="41890-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="41890-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41890-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="41890-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="41890-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="41890-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="41890-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="41890-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="41890-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="41890-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41890-123">Requirements</span></span>



| <span data-ttu-id="41890-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41890-124">Requirement</span></span> | <span data-ttu-id="41890-125">Wert</span><span class="sxs-lookup"><span data-stu-id="41890-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="41890-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="41890-126">TAPI version</span></span><br/> | <span data-ttu-id="41890-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="41890-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="41890-128">Header</span><span class="sxs-lookup"><span data-stu-id="41890-128">Header</span></span><br/>       | <dl> <span data-ttu-id="41890-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41890-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="41890-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41890-130">Library</span></span><br/>      | <dl> <span data-ttu-id="41890-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41890-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="41890-132">DLL</span><span class="sxs-lookup"><span data-stu-id="41890-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="41890-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41890-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41890-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41890-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41890-135">**Itstreamqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="41890-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="41890-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="41890-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="41890-137">**Streamqualityproperty**</span><span class="sxs-lookup"><span data-stu-id="41890-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




