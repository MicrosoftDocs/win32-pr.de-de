---
description: Die get \_ Count-Methode ruft die Anzahl der Medien in der Sitzung ab.
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'Itmediacollection:: get_Count-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365692"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="bd885-103">Itmediacollection:: get \_ Count-Methode</span><span class="sxs-lookup"><span data-stu-id="bd885-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="bd885-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bd885-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bd885-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="bd885-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bd885-106">Die **get \_ count** -Methode ruft die Anzahl der Medien in der Sitzung ab.</span><span class="sxs-lookup"><span data-stu-id="bd885-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd885-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd885-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="bd885-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd885-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd885-109">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bd885-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd885-110">Anzahl der Medien in der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bd885-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd885-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd885-111">Return value</span></span>

<span data-ttu-id="bd885-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bd885-112">This method can return one of these values.</span></span>



| <span data-ttu-id="bd885-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bd885-113">Return code</span></span>                                                                                   | <span data-ttu-id="bd885-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd885-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="bd885-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bd885-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="bd885-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bd885-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bd885-118">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="bd885-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="bd885-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bd885-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bd885-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="bd885-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="bd885-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bd885-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bd885-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="bd885-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="bd885-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="bd885-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd885-125">Requirements</span></span>



| <span data-ttu-id="bd885-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd885-126">Requirement</span></span> | <span data-ttu-id="bd885-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bd885-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd885-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="bd885-128">TAPI version</span></span><br/> | <span data-ttu-id="bd885-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bd885-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="bd885-130">Header</span><span class="sxs-lookup"><span data-stu-id="bd885-130">Header</span></span><br/>       | <dl> <span data-ttu-id="bd885-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd885-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd885-132">Library</span></span><br/>      | <dl> <span data-ttu-id="bd885-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bd885-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bd885-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="bd885-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd885-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd885-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd885-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd885-137">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="bd885-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




