---
description: Die get \_ \_ netwenum-Methode gibt einen Enumerator für die Auflistung zurück.
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'Itmediacollection:: get__NewEnum-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfa5655d70026fe2c481aedad0e76923f4caa646
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361563"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="fe839-103">Itmediacollection:: get- \_ \_ Methode</span><span class="sxs-lookup"><span data-stu-id="fe839-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="fe839-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe839-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fe839-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fe839-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fe839-106">Die **get \_ \_ netwenum** -Methode gibt einen Enumerator für die Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="fe839-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe839-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe839-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="fe839-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe839-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe839-109">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe839-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe839-110">Zeiger auf eine [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für ein Enumeratorobjekt für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="fe839-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="fe839-111">Rufen Sie die [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode auf der zurückgegebenen **IUnknown** -Schnittstelle auf, um einen Zeiger auf eine [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) -Enumerationsschnittstelle für die Auflistung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fe839-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="fe839-112">**IEnumVARIANT** bietet eine Reihe von Methoden, die Sie verwenden können, um die Auflistung zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="fe839-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="fe839-113">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="fe839-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe839-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe839-114">Return value</span></span>

<span data-ttu-id="fe839-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fe839-115">This method can return one of these values.</span></span>



| <span data-ttu-id="fe839-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fe839-116">Return code</span></span>                                                                                   | <span data-ttu-id="fe839-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe839-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fe839-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fe839-119">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fe839-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fe839-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fe839-121">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="fe839-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="fe839-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fe839-123">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fe839-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="fe839-124"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fe839-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="fe839-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="fe839-126"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fe839-127">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fe839-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="fe839-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe839-128">Remarks</span></span>

<span data-ttu-id="fe839-129">Diese Methode ist mit [**get \_ enumerationif**](itmediacollection-get-enumerationif.md) austauschbar, mit dem Unterschied, dass Sie anstelle von [**ienummedia**](ienummedia.md) **IUnknown** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fe839-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fe839-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe839-130">Requirements</span></span>



| <span data-ttu-id="fe839-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe839-131">Requirement</span></span> | <span data-ttu-id="fe839-132">Wert</span><span class="sxs-lookup"><span data-stu-id="fe839-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe839-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fe839-133">TAPI version</span></span><br/> | <span data-ttu-id="fe839-134">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fe839-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fe839-135">Header</span><span class="sxs-lookup"><span data-stu-id="fe839-135">Header</span></span><br/>       | <dl> <span data-ttu-id="fe839-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe839-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe839-137">Library</span></span><br/>      | <dl> <span data-ttu-id="fe839-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fe839-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fe839-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="fe839-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe839-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe839-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe839-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe839-142">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="fe839-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

