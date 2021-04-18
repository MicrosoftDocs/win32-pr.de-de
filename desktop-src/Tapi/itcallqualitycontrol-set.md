---
description: Die Set-Methode legt den Wert einer angegebenen Eigenschaft für den Qualitäts Steuerungs Wert fest.
ms.assetid: e83ed9d7-0a53-4555-ae44-737ab3dfb749
title: 'Itcallqualitycontrol:: Set-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c0a83702ba0dd4d04eb129eeed95c46d2a79a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361502"
---
# <a name="itcallqualitycontrolset-method"></a><span data-ttu-id="7f37c-103">Itcallqualitycontrol:: Set-Methode</span><span class="sxs-lookup"><span data-stu-id="7f37c-103">ITCallQualityControl::Set method</span></span>

<span data-ttu-id="7f37c-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f37c-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7f37c-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7f37c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7f37c-106">Die **Set** -Methode legt den Wert einer angegebenen [Eigenschaft für den Qualitäts Steuerungs](callqualityproperty.md)Wert fest.</span><span class="sxs-lookup"><span data-stu-id="7f37c-106">The **Set** method sets the value of a given [call quality control property](callqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f37c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f37c-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] CallQualityProperty Property,
  [in] long                lValue,
  [in] TAPIControlFlags    lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7f37c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f37c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f37c-109">*Eigenschaft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f37c-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f37c-110">Member der [**callqualityproperty**](callqualityproperty.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="7f37c-110">Member of the [**CallQualityProperty**](callqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="7f37c-111">*Lvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f37c-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f37c-112">Der gewünschte Wert für die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7f37c-112">Desired value for the property.</span></span>

</dd> <dt>

<span data-ttu-id="7f37c-113">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f37c-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f37c-114">Der Wert der [**tapicontrolflags**](tapicontrolflags.md) -Enumeration, die angibt, wie der *Eigenschafts* Wert gesteuert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f37c-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f37c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f37c-115">Return value</span></span>

<span data-ttu-id="7f37c-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7f37c-116">This method can return one of these values.</span></span>



| <span data-ttu-id="7f37c-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7f37c-117">Return code</span></span>                                                                                   | <span data-ttu-id="7f37c-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f37c-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7f37c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f37c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7f37c-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7f37c-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7f37c-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="7f37c-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7f37c-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7f37c-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f37c-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f37c-123">Requirements</span></span>



| <span data-ttu-id="7f37c-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f37c-124">Requirement</span></span> | <span data-ttu-id="7f37c-125">Wert</span><span class="sxs-lookup"><span data-stu-id="7f37c-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7f37c-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="7f37c-126">TAPI version</span></span><br/> | <span data-ttu-id="7f37c-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7f37c-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7f37c-128">Header</span><span class="sxs-lookup"><span data-stu-id="7f37c-128">Header</span></span><br/>       | <dl> <span data-ttu-id="7f37c-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f37c-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f37c-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f37c-130">Library</span></span><br/>      | <dl> <span data-ttu-id="7f37c-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f37c-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7f37c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7f37c-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="7f37c-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f37c-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f37c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f37c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f37c-135">**Itcallqualitycontrol**</span><span class="sxs-lookup"><span data-stu-id="7f37c-135">**ITCallQualityControl**</span></span>](itcallqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="7f37c-136">**Tapicontrolflags**</span><span class="sxs-lookup"><span data-stu-id="7f37c-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="7f37c-137">**Callqualityproperty**</span><span class="sxs-lookup"><span data-stu-id="7f37c-137">**CallQualityProperty**</span></span>](callqualityproperty.md)
</dt> </dl>

 

 




