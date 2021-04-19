---
description: Die get \_ Item-Methode ruft einen ITmedia-Zeiger ab, der dem angegebenen Index entspricht.
ms.assetid: ad218357-82c8-4fcb-b71b-ba17564a5ca5
title: 'Itmediacollection:: get_Item-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c68f3571dbd1f66e325dd7fa1bb30dfe6d6bc35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373862"
---
# <a name="itmediacollectionget_item-method"></a><span data-ttu-id="98712-103">Itmediacollection:: get \_ Item-Methode</span><span class="sxs-lookup"><span data-stu-id="98712-103">ITMediaCollection::get\_Item method</span></span>

<span data-ttu-id="98712-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="98712-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="98712-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="98712-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="98712-106">Die **get \_ Item** -Methode ruft einen [**ITmedia**](itmedia.md) -Zeiger ab, der dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="98712-106">The **get\_Item** method gets an [**ITMedia**](itmedia.md) pointer corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="98712-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="98712-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG    Index,
  [out] ITMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="98712-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="98712-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98712-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98712-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98712-110">Der Index des zu entzurufenden Medien Elements.</span><span class="sxs-lookup"><span data-stu-id="98712-110">Index of media item to get.</span></span>

</dd> <dt>

<span data-ttu-id="98712-111">*PVal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98712-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98712-112">Ein Zeiger auf die [**ITmedia**](itmedia.md) -Schnittstelle für das gewünschte Element.</span><span class="sxs-lookup"><span data-stu-id="98712-112">Pointer to the [**ITMedia**](itmedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98712-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98712-113">Return value</span></span>

<span data-ttu-id="98712-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="98712-114">This method can return one of these values.</span></span>



| <span data-ttu-id="98712-115">Wert</span><span class="sxs-lookup"><span data-stu-id="98712-115">Value</span></span>                                                                                         | <span data-ttu-id="98712-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="98712-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="98712-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98712-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="98712-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="98712-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="98712-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="98712-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="98712-120">Der *PVal* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="98712-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="98712-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="98712-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="98712-122">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="98712-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="98712-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="98712-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="98712-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="98712-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="98712-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="98712-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="98712-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="98712-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="98712-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="98712-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="98712-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="98712-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="98712-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98712-129">Remarks</span></span>

<span data-ttu-id="98712-130">Die meisten C-und C++-Listen sind 0-basiert, aber dieser Index basiert auf Visual Basic Kompatibilität, d. h., das erste Element hat eine Indexnummer von 1.</span><span class="sxs-lookup"><span data-stu-id="98712-130">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="98712-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98712-131">Requirements</span></span>



| <span data-ttu-id="98712-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98712-132">Requirement</span></span> | <span data-ttu-id="98712-133">Wert</span><span class="sxs-lookup"><span data-stu-id="98712-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98712-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="98712-134">TAPI version</span></span><br/> | <span data-ttu-id="98712-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="98712-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="98712-136">Header</span><span class="sxs-lookup"><span data-stu-id="98712-136">Header</span></span><br/>       | <dl> <span data-ttu-id="98712-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="98712-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="98712-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="98712-138">Library</span></span><br/>      | <dl> <span data-ttu-id="98712-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98712-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="98712-140">DLL</span><span class="sxs-lookup"><span data-stu-id="98712-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="98712-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98712-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98712-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98712-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98712-143">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="98712-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="98712-144">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="98712-144">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




