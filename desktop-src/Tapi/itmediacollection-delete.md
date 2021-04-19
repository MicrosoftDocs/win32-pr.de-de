---
description: Mit der Delete-Methode wird das Medium gelöscht, das dem angegebenen Index entspricht.
ms.assetid: 5fcbd026-75a8-4db2-a701-e080dc222537
title: Itmediacollection::D Elete-Methode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ffabee84bd7d04f517ef26ad5259f642cfed48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372583"
---
# <a name="itmediacollectiondelete-method"></a><span data-ttu-id="70eec-103">Itmediacollection::D Elete-Methode</span><span class="sxs-lookup"><span data-stu-id="70eec-103">ITMediaCollection::Delete method</span></span>

<span data-ttu-id="70eec-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="70eec-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70eec-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="70eec-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="70eec-106">Mit der **Delete** -Methode wird das Medium gelöscht, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="70eec-106">The **Delete** method deletes the media corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="70eec-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="70eec-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="70eec-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="70eec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70eec-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70eec-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70eec-110">Der Index des zu löschenden Mediums.</span><span class="sxs-lookup"><span data-stu-id="70eec-110">Index of media to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70eec-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70eec-111">Return value</span></span>

<span data-ttu-id="70eec-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="70eec-112">This method can return one of these values.</span></span>



| <span data-ttu-id="70eec-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="70eec-113">Return code</span></span>                                                                                                                              | <span data-ttu-id="70eec-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70eec-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="70eec-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-115"><dt>**S\_OK**</dt></span></span> </dl>                                                     | <span data-ttu-id="70eec-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="70eec-116">Method succeeded.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="70eec-117"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                                             | <span data-ttu-id="70eec-118">Der *Index* -Parameter weist einen Wert auf, der kleiner als 1 oder größer als die aktuelle Anzahl der Elemente ist.</span><span class="sxs-lookup"><span data-stu-id="70eec-118">The *Index* parameter has a value less than 1 or greater than the current number of elements.</span></span><br/> |
| <dl> <span data-ttu-id="70eec-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                                            | <span data-ttu-id="70eec-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="70eec-120">Insufficient memory exists to perform the operation.</span></span><br/>                                          |
| <dl> <span data-ttu-id="70eec-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-121"><dt>**E\_FAIL**</dt></span></span> </dl>                                                   | <span data-ttu-id="70eec-122">Interner Fehler (sollte nur auftreten, wenn ein vorheriger-Rückruf einen Fehler zurückgegeben hat).</span><span class="sxs-lookup"><span data-stu-id="70eec-122">Internal error (should only occur if a previous call returned an error).</span></span><br/>                      |
| <dl> <span data-ttu-id="70eec-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                                                | <span data-ttu-id="70eec-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="70eec-124">This method is not yet implemented.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="70eec-125"><dt>**HRESULT \_ aus \_ Fehler \_ Code (sdpblb \_ conf \_ BLOB \_ zerstört)**</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-125"><dt>**HRESULT\_FROM\_ERROR\_CODE(SDPBLB\_CONF\_BLOB\_DESTROYED)**</dt></span></span> </dl> | <span data-ttu-id="70eec-126">Das SDP-BLOB ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="70eec-126">The SDP blob doesn't exist.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="70eec-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70eec-127">Remarks</span></span>

<span data-ttu-id="70eec-128">Die meisten C-und C++-Listen sind 0-basiert, aber dieser Index basiert auf Visual Basic Kompatibilität, d. h., das erste Element hat eine Indexnummer von 1.</span><span class="sxs-lookup"><span data-stu-id="70eec-128">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="70eec-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70eec-129">Requirements</span></span>



| <span data-ttu-id="70eec-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70eec-130">Requirement</span></span> | <span data-ttu-id="70eec-131">Wert</span><span class="sxs-lookup"><span data-stu-id="70eec-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70eec-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="70eec-132">TAPI version</span></span><br/> | <span data-ttu-id="70eec-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="70eec-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="70eec-134">Header</span><span class="sxs-lookup"><span data-stu-id="70eec-134">Header</span></span><br/>       | <dl> <span data-ttu-id="70eec-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="70eec-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="70eec-136">Library</span></span><br/>      | <dl> <span data-ttu-id="70eec-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="70eec-138">DLL</span><span class="sxs-lookup"><span data-stu-id="70eec-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="70eec-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70eec-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70eec-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70eec-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70eec-141">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="70eec-141">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




