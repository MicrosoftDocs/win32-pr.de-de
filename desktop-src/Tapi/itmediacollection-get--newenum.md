---
description: 'ITMediaCollection::get__NewEnum-Methode: Die get NewEnum-Methode gibt einen \_ \_ Enumerator für die Auflistung zurück.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: ITMediaCollection::get__NewEnum-Methode (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6683ce0a00f0128cb959dd5a2c39e8b06382f65d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098358"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="6d3c2-103">ITMediaCollection::get \_ \_ NewEnum-Methode</span><span class="sxs-lookup"><span data-stu-id="6d3c2-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="6d3c2-104">\[ Rendezvous IP-Telefoniekonferenz-Steuerelemente und -Schnittstellen sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6d3c2-105">Die RTC-Client-API bietet ähnliche Funktionen.\]</span><span class="sxs-lookup"><span data-stu-id="6d3c2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6d3c2-106">Die **get \_ \_ NewEnum-Methode** gibt einen Enumerator für die Auflistung zurück.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d3c2-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="6d3c2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d3c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3c2-109">*pVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6d3c2-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3c2-110">Zeiger auf eine [IUnknown-Schnittstelle](/windows/win32/api/unknwn/nn-unknwn-iunknown) für ein Enumeratorobjekt für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="6d3c2-111">Rufen Sie [die QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für die **zurückgegebene IUnknown-Schnittstelle** auf, um einen Zeiger auf eine [IEnumVARIANT-Enumerationsschnittstelle](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) für die Auflistung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="6d3c2-112">**IEnumVARIANT** bietet eine Reihe von Methoden, die Sie verwenden können, um die Auflistung zu iterieren.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="6d3c2-113">Weitere Informationen finden Sie im folgenden Abschnitt "Hinweise".</span><span class="sxs-lookup"><span data-stu-id="6d3c2-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3c2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d3c2-114">Return value</span></span>

<span data-ttu-id="6d3c2-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="6d3c2-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6d3c2-116">Return code</span></span>                                                                                   | <span data-ttu-id="6d3c2-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d3c2-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6d3c2-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6d3c2-119">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6d3c2-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6d3c2-121">Der *pVal-Parameter* ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="6d3c2-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6d3c2-123">Es ist nicht genügend Arbeitsspeicher vorhanden, um den Vorgang durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6d3c2-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6d3c2-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6d3c2-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6d3c2-127">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6d3c2-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6d3c2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d3c2-128">Remarks</span></span>

<span data-ttu-id="6d3c2-129">Diese Methode kann mit get [**\_ EnumerationIf austauschbar sein,**](itmediacollection-get-enumerationif.md) mit der Ausnahme, dass **sie IUnknown** anstelle von [**IEnumMedia zurückgibt.**](ienummedia.md)</span><span class="sxs-lookup"><span data-stu-id="6d3c2-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3c2-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d3c2-130">Requirements</span></span>



| <span data-ttu-id="6d3c2-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d3c2-131">Requirement</span></span> | <span data-ttu-id="6d3c2-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6d3c2-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3c2-133">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="6d3c2-133">TAPI version</span></span><br/> | <span data-ttu-id="6d3c2-134">Erfordert TAPI 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6d3c2-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6d3c2-135">Header</span><span class="sxs-lookup"><span data-stu-id="6d3c2-135">Header</span></span><br/>       | <dl> <span data-ttu-id="6d3c2-136"><dt>Sdpblb.h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d3c2-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d3c2-137">Library</span></span><br/>      | <dl> <span data-ttu-id="6d3c2-138"><dt>Uuid.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6d3c2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6d3c2-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="6d3c2-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d3c2-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d3c2-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6d3c2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3c2-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="6d3c2-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

