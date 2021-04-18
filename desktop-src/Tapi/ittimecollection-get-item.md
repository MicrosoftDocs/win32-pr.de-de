---
description: Die get \_ Item-Methode ruft mithilfe eines Indexes ein Element aus der Auflistung ab.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'Ittimecollection:: get_Item-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351267"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="57ead-103">Ittimecollection:: get \_ Item-Methode</span><span class="sxs-lookup"><span data-stu-id="57ead-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="57ead-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="57ead-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="57ead-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="57ead-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="57ead-106">Die **get \_ Item** -Methode ruft mithilfe eines Indexes ein Element aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="57ead-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ead-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ead-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="57ead-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="57ead-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ead-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57ead-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ead-110">Der Index des zu entzurufenden Elements.</span><span class="sxs-lookup"><span data-stu-id="57ead-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="57ead-111">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57ead-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57ead-112">Zeiger auf die gewünschte [**ittime**](ittime.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="57ead-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ead-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57ead-113">Return value</span></span>

<span data-ttu-id="57ead-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="57ead-114">This method can return one of these values.</span></span>



| <span data-ttu-id="57ead-115">Wert</span><span class="sxs-lookup"><span data-stu-id="57ead-115">Value</span></span>                                                                                         | <span data-ttu-id="57ead-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="57ead-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="57ead-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="57ead-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="57ead-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="57ead-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="57ead-120">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="57ead-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="57ead-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="57ead-122">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="57ead-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="57ead-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="57ead-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="57ead-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="57ead-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="57ead-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="57ead-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="57ead-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="57ead-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="57ead-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="57ead-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="57ead-129">Remarks</span></span>

<span data-ttu-id="57ead-130">TAPI Ruft die **adressf** -Methode für die [**ittime**](ittime.md) -Schnittstelle auf, die vom **\_ Element "ttimecollection:: Get**" zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="57ead-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="57ead-131">Die Anwendung muss Release auf der **ittime** -Schnittstelle aufzurufen, um die damit verbundenen Ressourcen frei **zugeben** .</span><span class="sxs-lookup"><span data-stu-id="57ead-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ead-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57ead-132">Requirements</span></span>



| <span data-ttu-id="57ead-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57ead-133">Requirement</span></span> | <span data-ttu-id="57ead-134">Wert</span><span class="sxs-lookup"><span data-stu-id="57ead-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57ead-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="57ead-135">TAPI version</span></span><br/> | <span data-ttu-id="57ead-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="57ead-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="57ead-137">Header</span><span class="sxs-lookup"><span data-stu-id="57ead-137">Header</span></span><br/>       | <dl> <span data-ttu-id="57ead-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="57ead-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="57ead-139">Library</span></span><br/>      | <dl> <span data-ttu-id="57ead-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="57ead-141">DLL</span><span class="sxs-lookup"><span data-stu-id="57ead-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="57ead-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ead-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ead-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57ead-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ead-144">**Ittimecollection**</span><span class="sxs-lookup"><span data-stu-id="57ead-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="57ead-145">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="57ead-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




