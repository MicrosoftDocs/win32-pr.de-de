---
description: 'ITTimeCollection::get__NewEnum-Methode: Die get NewEnum-Methode gibt einen \_ \_ Enumerator für die Auflistung zurück.'
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: ITTimeCollection::get__NewEnum-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acfc9d616efb58c6173f2c9c6e5913d27776958c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088888"
---
# <a name="ittimecollectionget__newenum-method"></a><span data-ttu-id="b4301-103">ITTimeCollection::get \_ \_ NewEnum-Methode</span><span class="sxs-lookup"><span data-stu-id="b4301-103">ITTimeCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="b4301-104">\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4301-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b4301-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="b4301-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b4301-106">Die **get \_ \_ NewEnum-Methode** gibt einen Enumerator für die Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="b4301-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4301-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4301-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b4301-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4301-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4301-109">*pVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b4301-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4301-110">Zeiger auf eine [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) für ein Enumeratorobjekt für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b4301-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="b4301-111">Rufen Sie [die QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die **zurückgegebene IUnknown-Schnittstelle** auf, um einen Zeiger auf eine [IEnumVARIANT-Enumerationsschnittstelle](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für die Auflistung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b4301-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="b4301-112">**IEnumVARIANT** bietet eine Reihe von Methoden, die Sie verwenden können, um die Auflistung zu iterieren.</span><span class="sxs-lookup"><span data-stu-id="b4301-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="b4301-113">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="b4301-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4301-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4301-114">Return value</span></span>

<span data-ttu-id="b4301-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b4301-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b4301-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b4301-116">Return code</span></span>                                                                                   | <span data-ttu-id="b4301-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4301-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b4301-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b4301-119">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b4301-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b4301-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b4301-121">Der *pVal-Parameter* ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="b4301-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="b4301-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b4301-123">Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="b4301-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b4301-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b4301-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="b4301-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b4301-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b4301-127">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="b4301-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b4301-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4301-128">Remarks</span></span>

<span data-ttu-id="b4301-129">Diese Methode kann mit get [**\_ EnumerationIf austauschbar sein,**](ittimecollection-get-enumerationif.md) mit der Ausnahme, dass **sie IUnknown** anstelle von [**IEnumTime zurückgibt.**](ienumtime.md)</span><span class="sxs-lookup"><span data-stu-id="b4301-129">This method is interchangeable with [**get\_EnumerationIf**](ittimecollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumTime**](ienumtime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4301-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4301-130">Requirements</span></span>



| <span data-ttu-id="b4301-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4301-131">Requirement</span></span> | <span data-ttu-id="b4301-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b4301-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4301-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b4301-133">TAPI version</span></span><br/> | <span data-ttu-id="b4301-134">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b4301-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b4301-135">Header</span><span class="sxs-lookup"><span data-stu-id="b4301-135">Header</span></span><br/>       | <dl> <span data-ttu-id="b4301-136"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4301-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4301-137">Library</span></span><br/>      | <dl> <span data-ttu-id="b4301-138"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b4301-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b4301-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="b4301-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4301-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4301-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b4301-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4301-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="b4301-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="b4301-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="b4301-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

