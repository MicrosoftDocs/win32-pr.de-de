---
description: Die get \_ enumerationif-Methode gibt die ienumtime-Enumerationsschnittstelle zurück, die ittime auflistet.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'Ittimecollection:: get_EnumerationIf-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356414"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="22723-103">Ittimecollection:: get \_ enumerationif-Methode</span><span class="sxs-lookup"><span data-stu-id="22723-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="22723-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22723-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="22723-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="22723-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="22723-106">Die **get \_ enumerationif** -Methode gibt die [**ienumtime**](ienumtime.md) -Enumerationsschnittstelle zurück, die [**ittime**](ittime.md)auflistet.</span><span class="sxs-lookup"><span data-stu-id="22723-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="22723-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22723-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="22723-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22723-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22723-109">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22723-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22723-110">Zeiger auf die [**ienumtime**](ienumtime.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="22723-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22723-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22723-111">Return value</span></span>

<span data-ttu-id="22723-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22723-112">This method can return one of these values.</span></span>



| <span data-ttu-id="22723-113">Wert</span><span class="sxs-lookup"><span data-stu-id="22723-113">Value</span></span>                                                                                         | <span data-ttu-id="22723-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="22723-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="22723-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22723-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="22723-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="22723-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="22723-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="22723-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="22723-118">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="22723-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="22723-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="22723-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="22723-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="22723-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="22723-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="22723-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="22723-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="22723-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="22723-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="22723-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="22723-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="22723-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="22723-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22723-125">Remarks</span></span>

<span data-ttu-id="22723-126">Diese Methode ist mit [**get \_ \_ netwenum**](ittimecollection-get--newenum.md) austauschbar, mit der Ausnahme, dass Sie [**ienumtime**](ienumtime.md) anstelle von **IUnknown** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="22723-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="22723-127">TAPI Ruft die **adressf** -Methode für die [**ienumtime**](ienumtime.md) -Schnittstelle auf, die von **ittimecollection:: get \_ enumerationif** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="22723-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="22723-128">Die Anwendung muss Release auf der [**ienumtime**](ienumtime.md) -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="22723-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="22723-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22723-129">Requirements</span></span>



| <span data-ttu-id="22723-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22723-130">Requirement</span></span> | <span data-ttu-id="22723-131">Wert</span><span class="sxs-lookup"><span data-stu-id="22723-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22723-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="22723-132">TAPI version</span></span><br/> | <span data-ttu-id="22723-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="22723-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="22723-134">Header</span><span class="sxs-lookup"><span data-stu-id="22723-134">Header</span></span><br/>       | <dl> <span data-ttu-id="22723-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="22723-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="22723-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22723-136">Library</span></span><br/>      | <dl> <span data-ttu-id="22723-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22723-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="22723-138">DLL</span><span class="sxs-lookup"><span data-stu-id="22723-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="22723-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22723-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22723-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22723-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22723-141">**Ienumtime**</span><span class="sxs-lookup"><span data-stu-id="22723-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="22723-142">**Ittimecollection**</span><span class="sxs-lookup"><span data-stu-id="22723-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="22723-143">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="22723-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




