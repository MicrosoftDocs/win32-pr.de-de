---
description: Die get \_ numadkleidungs-Methode ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'Itconnection:: get_NumAddresses-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364887"
---
# <a name="itconnectionget_numaddresses-method"></a><span data-ttu-id="92c28-103">Itconnection:: get \_ numadkleider-Methode</span><span class="sxs-lookup"><span data-stu-id="92c28-103">ITConnection::get\_NumAddresses method</span></span>

<span data-ttu-id="92c28-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92c28-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="92c28-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="92c28-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="92c28-106">Die **get \_ numadkleidungs** -Methode ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92c28-106">The **get\_NumAddresses** method gets the number of addresses to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="92c28-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="92c28-107">Syntax</span></span>


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="92c28-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="92c28-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c28-109">*pnumadkleider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="92c28-109">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92c28-110">Anzahl der Adressen für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="92c28-110">Number of addresses for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c28-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92c28-111">Return value</span></span>

<span data-ttu-id="92c28-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="92c28-112">This method can return one of these values.</span></span>



| <span data-ttu-id="92c28-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="92c28-113">Return code</span></span>                                                                                   | <span data-ttu-id="92c28-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92c28-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="92c28-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="92c28-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="92c28-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="92c28-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="92c28-118">Der *pnumaddresse* s-Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="92c28-118">The *pNumAddresse* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="92c28-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="92c28-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92c28-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="92c28-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="92c28-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="92c28-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="92c28-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="92c28-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="92c28-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="92c28-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92c28-125">Requirements</span></span>



| <span data-ttu-id="92c28-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92c28-126">Requirement</span></span> | <span data-ttu-id="92c28-127">Wert</span><span class="sxs-lookup"><span data-stu-id="92c28-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92c28-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="92c28-128">TAPI version</span></span><br/> | <span data-ttu-id="92c28-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="92c28-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="92c28-130">Header</span><span class="sxs-lookup"><span data-stu-id="92c28-130">Header</span></span><br/>       | <dl> <span data-ttu-id="92c28-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="92c28-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92c28-132">Library</span></span><br/>      | <dl> <span data-ttu-id="92c28-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="92c28-134">DLL</span><span class="sxs-lookup"><span data-stu-id="92c28-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="92c28-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c28-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c28-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92c28-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c28-137">**Itconnection**</span><span class="sxs-lookup"><span data-stu-id="92c28-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




