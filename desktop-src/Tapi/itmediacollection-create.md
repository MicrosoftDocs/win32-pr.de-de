---
description: Die Create-Methode erstellt ein neues Medium mit Standardeigenschaften, fügt es der Collection am angegebenen Index hinzu und gibt einen Zeiger auf die ITmedia-Schnittstelle zurück.
ms.assetid: f0036556-d2e7-4589-8bb4-e2c5559902fe
title: 'Itmediacollection:: Create-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8033fb2f541f5451f918845858df756b32361f54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370904"
---
# <a name="itmediacollectioncreate-method"></a><span data-ttu-id="8228b-103">Itmediacollection:: Create-Methode</span><span class="sxs-lookup"><span data-stu-id="8228b-103">ITMediaCollection::Create method</span></span>

<span data-ttu-id="8228b-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8228b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8228b-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="8228b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8228b-106">Die **Create** -Methode erstellt ein neues Medium mit Standardeigenschaften, fügt es der Collection am angegebenen Index hinzu und gibt einen Zeiger auf die [**ITmedia**](itmedia.md) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="8228b-106">The **Create** method creates a new media with default properties, adds it to the collection at the specified index, and returns a pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8228b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8228b-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG    Index,
  [out] ITMedia **ppMedia
);
```



## <a name="parameters"></a><span data-ttu-id="8228b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8228b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8228b-109">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8228b-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8228b-110">Der Index für das neue Element.</span><span class="sxs-lookup"><span data-stu-id="8228b-110">Index for the new item.</span></span> <span data-ttu-id="8228b-111">Der minimale Wert für den Index ist 1, und der Höchstwert für den Index ist die aktuelle Anzahl von Elementen + 1.</span><span class="sxs-lookup"><span data-stu-id="8228b-111">The minimum value for the index is 1, and the maximum value for the index is the current number of items + 1.</span></span>

</dd> <dt>

<span data-ttu-id="8228b-112">*ppmedia* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8228b-112">*ppMedia* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8228b-113">Zeiger auf die erstellte [**ITmedia**](itmedia.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8228b-113">Pointer to [**ITMedia**](itmedia.md) interface created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8228b-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8228b-114">Return value</span></span>

<span data-ttu-id="8228b-115">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8228b-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8228b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8228b-116">Value</span></span>                                                                                         | <span data-ttu-id="8228b-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8228b-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8228b-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8228b-119">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8228b-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8228b-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8228b-121">Der *ppmedia* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8228b-121">The *ppMedia* parameter is not a valid pointer.</span></span><br/>      |
| <dl> <span data-ttu-id="8228b-122"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8228b-123">Der *Index* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8228b-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="8228b-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8228b-125">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8228b-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8228b-126"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8228b-127">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="8228b-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8228b-128"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8228b-129">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="8228b-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8228b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8228b-130">Remarks</span></span>

<span data-ttu-id="8228b-131">Die meisten C-und C++-Listen sind 0-basiert, aber dieser Index basiert auf Visual Basic Kompatibilität, d. h., das erste Element hat eine Indexnummer von 1.</span><span class="sxs-lookup"><span data-stu-id="8228b-131">Most C and C++ lists are 0-based, but this index is 1-based for Visual Basic compatibility, meaning the first item has an index number of 1.</span></span>

<span data-ttu-id="8228b-132">TAPI Ruft die **adressf** -Methode auf der [**ITmedia**](itmedia.md) -Schnittstelle auf, die von **itmediacollection:: Create** zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8228b-132">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **ITMediaCollection::Create**.</span></span> <span data-ttu-id="8228b-133">Die Anwendung muss Release auf der [**ITmedia**](itmedia.md) -Schnittstelle aufzurufen, um Ressourcen frei **zugeben** , die ihr zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8228b-133">The application must call **Release** on the [**ITMedia**](itmedia.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8228b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8228b-134">Requirements</span></span>



| <span data-ttu-id="8228b-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8228b-135">Requirement</span></span> | <span data-ttu-id="8228b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="8228b-136">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8228b-137">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="8228b-137">TAPI version</span></span><br/> | <span data-ttu-id="8228b-138">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="8228b-138">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8228b-139">Header</span><span class="sxs-lookup"><span data-stu-id="8228b-139">Header</span></span><br/>       | <dl> <span data-ttu-id="8228b-140"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-140"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8228b-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8228b-141">Library</span></span><br/>      | <dl> <span data-ttu-id="8228b-142"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-142"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8228b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="8228b-143">DLL</span></span><br/>          | <dl> <span data-ttu-id="8228b-144"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8228b-144"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8228b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8228b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8228b-146">**ITmedia**</span><span class="sxs-lookup"><span data-stu-id="8228b-146">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="8228b-147">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="8228b-147">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




