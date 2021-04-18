---
description: Die get \_ enumerationif-Methode ruft einen Zeiger auf eine mediumenumerationsschnittstelle ab.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Itmediacollection:: get_EnumerationIf-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365681"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="3d550-103">Itmediacollection:: get \_ enumerationif-Methode</span><span class="sxs-lookup"><span data-stu-id="3d550-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="3d550-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3d550-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3d550-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3d550-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3d550-106">Die **get \_ enumerationif** -Methode ruft einen Zeiger auf eine mediumenumerationsschnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="3d550-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d550-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d550-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="3d550-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d550-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d550-109">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3d550-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d550-110">Ein Zeiger auf die [**ienummedia**](ienummedia.md) -Schnittstelle für das gewünschte Element.</span><span class="sxs-lookup"><span data-stu-id="3d550-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d550-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d550-111">Return value</span></span>

<span data-ttu-id="3d550-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3d550-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3d550-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3d550-113">Value</span></span>                                                                                         | <span data-ttu-id="3d550-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="3d550-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3d550-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3d550-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3d550-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3d550-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3d550-118">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3d550-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="3d550-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3d550-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3d550-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3d550-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3d550-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="3d550-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3d550-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3d550-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="3d550-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3d550-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d550-125">Remarks</span></span>

<span data-ttu-id="3d550-126">Diese Methode ist mit [**get \_ \_ netwenum**](itmediacollection-get--newenum.md) austauschbar, mit dem Unterschied, dass Sie [**ienummedia**](ienummedia.md) anstelle von **IUnknown** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3d550-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="3d550-127">TAPI Ruft die **adressf** -Methode für die [**ienummedia**](ienummedia.md) -Schnittstelle auf, die von **itmediacollection:: get \_ enumerationlf** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="3d550-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="3d550-128">Die Anwendung muss Release auf der **ienummedia** -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d550-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d550-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d550-129">Requirements</span></span>



| <span data-ttu-id="3d550-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d550-130">Requirement</span></span> | <span data-ttu-id="3d550-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3d550-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d550-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="3d550-132">TAPI version</span></span><br/> | <span data-ttu-id="3d550-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="3d550-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3d550-134">Header</span><span class="sxs-lookup"><span data-stu-id="3d550-134">Header</span></span><br/>       | <dl> <span data-ttu-id="3d550-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d550-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3d550-136">Library</span></span><br/>      | <dl> <span data-ttu-id="3d550-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3d550-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3d550-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="3d550-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d550-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d550-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d550-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d550-141">**Ienummedia**</span><span class="sxs-lookup"><span data-stu-id="3d550-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="3d550-142">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="3d550-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




