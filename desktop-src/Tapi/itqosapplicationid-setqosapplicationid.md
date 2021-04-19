---
description: Die setqosapplicationid-Methode legt den QoS-Bezeichner für die Anwendung fest.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'Itqosapplicationid:: setqosapplicationid-Methode (ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372505"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="2ddf8-103">Itqosapplicationid:: setqosapplicationid-Methode</span><span class="sxs-lookup"><span data-stu-id="2ddf8-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="2ddf8-104">\[ Diese Methode ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ddf8-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2ddf8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2ddf8-106">Die **setqosapplicationid** -Methode legt den QoS-Bezeichner für die Anwendung fest.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddf8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ddf8-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="2ddf8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ddf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddf8-109">*papplicationid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ddf8-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddf8-110">Eindeutiger Bezeichner für den Anwendungsprozess.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="2ddf8-111">*papplicationguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ddf8-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddf8-112">Anwendungs-GUID.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="2ddf8-113">*psugebote* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ddf8-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddf8-114">Sub-IDs dem aktuellen-Befehl zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddf8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ddf8-115">Return value</span></span>

<span data-ttu-id="2ddf8-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2ddf8-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2ddf8-117">Return code</span></span>                                                                                   | <span data-ttu-id="2ddf8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ddf8-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2ddf8-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ddf8-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ddf8-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2ddf8-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2ddf8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ddf8-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="2ddf8-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2ddf8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ddf8-123">Requirements</span></span>



| <span data-ttu-id="2ddf8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ddf8-124">Requirement</span></span> | <span data-ttu-id="2ddf8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2ddf8-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddf8-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2ddf8-126">TAPI version</span></span><br/> | <span data-ttu-id="2ddf8-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="2ddf8-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="2ddf8-128">Header</span><span class="sxs-lookup"><span data-stu-id="2ddf8-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2ddf8-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ddf8-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ddf8-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ddf8-130">Library</span></span><br/>      | <dl> <span data-ttu-id="2ddf8-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ddf8-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2ddf8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2ddf8-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="2ddf8-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ddf8-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ddf8-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ddf8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddf8-135">**Itqosapplicationid**</span><span class="sxs-lookup"><span data-stu-id="2ddf8-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




