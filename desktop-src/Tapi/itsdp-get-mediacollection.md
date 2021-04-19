---
description: Die get \_ mediacollection-Methode erhält einen Zeiger auf die itmediacollection-Schnittstelle für die Konferenz.
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'Itsdp:: get_MediaCollection-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f8812debf8c04fe022f24061660d6ea3bb5f162
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360366"
---
# <a name="itsdpget_mediacollection-method"></a><span data-ttu-id="0235f-103">Itsdp:: get \_ mediacollection-Methode</span><span class="sxs-lookup"><span data-stu-id="0235f-103">ITSdp::get\_MediaCollection method</span></span>

<span data-ttu-id="0235f-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0235f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0235f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0235f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0235f-106">Die **get \_ mediacollection** -Methode erhält einen Zeiger auf die [**itmediacollection**](itmediacollection.md) -Schnittstelle für die Konferenz.</span><span class="sxs-lookup"><span data-stu-id="0235f-106">The **get\_MediaCollection** method gets a pointer to the [**ITMediaCollection**](itmediacollection.md) interface for the conference.</span></span>

## <a name="syntax"></a><span data-ttu-id="0235f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0235f-107">Syntax</span></span>


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a><span data-ttu-id="0235f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0235f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0235f-109">*ppmediacollection* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0235f-109">*ppMediaCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0235f-110">Zeiger auf [**itmediacollection**](itmediacollection.md).</span><span class="sxs-lookup"><span data-stu-id="0235f-110">Pointer to [**ITMediaCollection**](itmediacollection.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0235f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0235f-111">Return value</span></span>

<span data-ttu-id="0235f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0235f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0235f-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0235f-113">Value</span></span>                                                                                                                           | <span data-ttu-id="0235f-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0235f-114">Meaning</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0235f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-115"><dt>**S\_OK**</dt></span></span> </dl>                                            | <span data-ttu-id="0235f-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0235f-116">Method succeeded.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="0235f-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                    | <span data-ttu-id="0235f-118">Der *ppmediacollection* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="0235f-118">The *ppMediaCollection* parameter is not a valid pointer.</span></span><br/>                        |
| <dl> <span data-ttu-id="0235f-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                   | <span data-ttu-id="0235f-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0235f-120">Insufficient memory exists to perform the operation.</span></span><br/>                             |
| <dl> <span data-ttu-id="0235f-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                          | <span data-ttu-id="0235f-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0235f-122">Unspecified error.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="0235f-123"><dt>**HRESULT \_ aus \_ Fehler \_ Code ( \_ ungültige \_ Daten)**</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-123"><dt>**HRESULT\_FROM\_ERROR\_CODE(ERROR\_INVALID\_DATA)**</dt></span></span> </dl> | <span data-ttu-id="0235f-124">Ein interner Fehler ist aufgetreten, normalerweise aufgrund des Fehlers einer vorherigen Methode.</span><span class="sxs-lookup"><span data-stu-id="0235f-124">An internal error has occurred, usually due to the failure of a previous method.</span></span><br/> |
| <dl> <span data-ttu-id="0235f-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                       | <span data-ttu-id="0235f-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0235f-126">This method is not yet implemented.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="0235f-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0235f-127">Remarks</span></span>

<span data-ttu-id="0235f-128">Ein [**itmediacollection**](itmediacollection.md) -Zeiger kann auch mithilfe von **QueryInterface** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0235f-128">An [**ITMediaCollection**](itmediacollection.md) pointer could also be obtained using **QueryInterface**.</span></span>

<span data-ttu-id="0235f-129">TAPI Ruft die **adressf** -Methode für die [**itmediacollection**](itmediacollection.md) -Schnittstelle auf, die von **itsdp:: get \_ mediacollection** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0235f-129">TAPI calls the **AddRef** method on the [**ITMediaCollection**](itmediacollection.md) interface returned by **ITSdp::get\_MediaCollection**.</span></span> <span data-ttu-id="0235f-130">Die Anwendung muss Release auf der **itmediacollection** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0235f-130">The application must call **Release** on the **ITMediaCollection** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="0235f-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0235f-131">Requirements</span></span>



| <span data-ttu-id="0235f-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0235f-132">Requirement</span></span> | <span data-ttu-id="0235f-133">Wert</span><span class="sxs-lookup"><span data-stu-id="0235f-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0235f-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0235f-134">TAPI version</span></span><br/> | <span data-ttu-id="0235f-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0235f-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0235f-136">Header</span><span class="sxs-lookup"><span data-stu-id="0235f-136">Header</span></span><br/>       | <dl> <span data-ttu-id="0235f-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0235f-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0235f-138">Library</span></span><br/>      | <dl> <span data-ttu-id="0235f-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0235f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0235f-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="0235f-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0235f-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0235f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0235f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0235f-143">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="0235f-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="0235f-144">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="0235f-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




