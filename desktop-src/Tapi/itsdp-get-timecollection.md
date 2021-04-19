---
description: Die get \_ timecollection-Methode erhält einen Zeiger auf eine ittimecollection-Schnittstelle für die Konferenz.
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'Itsdp:: get_TimeCollection-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368646"
---
# <a name="itsdpget_timecollection-method"></a><span data-ttu-id="833ae-103">Itsdp:: get \_ timecollection-Methode</span><span class="sxs-lookup"><span data-stu-id="833ae-103">ITSdp::get\_TimeCollection method</span></span>

<span data-ttu-id="833ae-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="833ae-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="833ae-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="833ae-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="833ae-106">Die **get \_ timecollection** -Methode erhält einen Zeiger auf eine [**ittimecollection**](ittimecollection.md) -Schnittstelle für die Konferenz.</span><span class="sxs-lookup"><span data-stu-id="833ae-106">The **get\_TimeCollection** method gets a pointer to an [**ITTimeCollection**](ittimecollection.md) interface for conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="833ae-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="833ae-107">Syntax</span></span>


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a><span data-ttu-id="833ae-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="833ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833ae-109">*pptimecollection* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="833ae-109">*ppTimeCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="833ae-110">Zeiger auf [**ittimecollection**](ittimecollection.md).</span><span class="sxs-lookup"><span data-stu-id="833ae-110">Pointer to [**ITTimeCollection**](ittimecollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833ae-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="833ae-111">Return value</span></span>

<span data-ttu-id="833ae-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="833ae-112">This method can return one of these values.</span></span>



| <span data-ttu-id="833ae-113">Wert</span><span class="sxs-lookup"><span data-stu-id="833ae-113">Value</span></span>                                                                                                                           | <span data-ttu-id="833ae-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="833ae-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="833ae-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="833ae-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="833ae-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="833ae-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="833ae-118">Der *pptimecollection* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="833ae-118">The *ppTimeCollection* parameter is not a valid pointer.</span></span><br/>                         |
| <dl> <span data-ttu-id="833ae-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="833ae-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="833ae-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="833ae-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="833ae-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="833ae-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="833ae-123"><dt>**HRESULT \_ aus \_ Fehler \_ Code ( \_ ungültige \_ Daten)**</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="833ae-124">Ein interner Fehler ist aufgetreten, normalerweise aufgrund des Fehlers einer vorherigen Methode.</span><span class="sxs-lookup"><span data-stu-id="833ae-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="833ae-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="833ae-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="833ae-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="833ae-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="833ae-127">Remarks</span></span>

<span data-ttu-id="833ae-128">Ein [**ittimecollection**](ittimecollection.md) -Zeiger kann auch mithilfe von **QueryInterface** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="833ae-128">An [**ITTimeCollection**](ittimecollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="833ae-129">TAPI Ruft die **adressf** -Methode für die [**ittimecollection**](ittimecollection.md) -Schnittstelle auf, die von **itsdp:: get \_ timecollection** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="833ae-129">TAPI calls the **AddRef** method on the [**ITTimeCollection**](ittimecollection.md) interface returned by **ITSdp::get\_TimeCollection**.</span></span> <span data-ttu-id="833ae-130">Die Anwendung muss Release auf der **ittimecollection** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="833ae-130">The application must call **Release** on the **ITTimeCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="833ae-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="833ae-131">Requirements</span></span>



| <span data-ttu-id="833ae-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="833ae-132">Requirement</span></span> | <span data-ttu-id="833ae-133">Wert</span><span class="sxs-lookup"><span data-stu-id="833ae-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="833ae-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="833ae-134">TAPI version</span></span><br/> | <span data-ttu-id="833ae-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="833ae-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="833ae-136">Header</span><span class="sxs-lookup"><span data-stu-id="833ae-136">Header</span></span><br/>       | <dl> <span data-ttu-id="833ae-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="833ae-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="833ae-138">Library</span></span><br/>      | <dl> <span data-ttu-id="833ae-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="833ae-140">DLL</span><span class="sxs-lookup"><span data-stu-id="833ae-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="833ae-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833ae-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833ae-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="833ae-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833ae-143">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="833ae-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="833ae-144">**Ittimecollection**</span><span class="sxs-lookup"><span data-stu-id="833ae-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> </dl>

 

 




