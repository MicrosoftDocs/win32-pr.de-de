---
description: Die get- \_ Zeichensatz Methode ruft einen BLOB- \_ \_ Zeichensatz Deskriptor des Zeichensatzes ab, der im aktuellen Konferenz-BLOB verwendet wird.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'Itconferendceblob:: get_CharacterSet-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681085672f49c75a8434c4b0311e75d2b9cea270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367033"
---
# <a name="itconferenceblobget_characterset-method"></a><span data-ttu-id="1b55f-103">Itconferenceblob:: get- \_ Merkmal Satz Methode</span><span class="sxs-lookup"><span data-stu-id="1b55f-103">ITConferenceBlob::get\_CharacterSet method</span></span>

<span data-ttu-id="1b55f-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b55f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1b55f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1b55f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1b55f-106">Die **get \_** -Zeichensatz Methode ruft einen [**BLOB- \_ \_ Zeichensatz**](blob-character-set.md) Deskriptor des Zeichensatzes ab, der im aktuellen Konferenz-BLOB verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b55f-106">The **get\_CharacterSet** method gets a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set used in the current conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b55f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b55f-107">Syntax</span></span>


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a><span data-ttu-id="1b55f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b55f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b55f-109">*pcharakteriseset* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b55f-109">*pCharacterSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b55f-110">Zeiger auf einen [**BLOB \_ - \_ Zeichensatz**](blob-character-set.md) Deskriptor des Zeichensatzes.</span><span class="sxs-lookup"><span data-stu-id="1b55f-110">Pointer to a [**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b55f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b55f-111">Return value</span></span>

<span data-ttu-id="1b55f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1b55f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1b55f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1b55f-113">Return code</span></span>                                                                                                   | <span data-ttu-id="1b55f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b55f-114">Description</span></span>                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b55f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-115"><dt>**S\_OK**</dt></span></span> </dl>                          | <span data-ttu-id="1b55f-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1b55f-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="1b55f-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-117"><dt>**E\_POINTER**</dt></span></span> </dl>                     | <span data-ttu-id="1b55f-118">Der *pcharakteriset* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="1b55f-118">The *pCharacterSet* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="1b55f-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>                 | <span data-ttu-id="1b55f-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1b55f-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="1b55f-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-121"><dt>**E\_FAIL**</dt></span></span> </dl>                        | <span data-ttu-id="1b55f-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1b55f-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1b55f-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                     | <span data-ttu-id="1b55f-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1b55f-124">This method is not yet implemented.</span></span><br/>                   |
| <dl> <span data-ttu-id="1b55f-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                  | <span data-ttu-id="1b55f-126">*pcharakteriset* ist **null**.</span><span class="sxs-lookup"><span data-stu-id="1b55f-126">*pCharacterSet* is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="1b55f-127"><dt>**HRESULT \_ungültige \_ Daten**</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-127"><dt>**(HRESULT) ERROR\_INVALID\_DATA**</dt></span></span> </dl> | <span data-ttu-id="1b55f-128">Der aktuelle Zeichensatz ist ungültig oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b55f-128">The current character set is invalid or unavailable.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="1b55f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b55f-129">Requirements</span></span>



| <span data-ttu-id="1b55f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b55f-130">Requirement</span></span> | <span data-ttu-id="1b55f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="1b55f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b55f-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1b55f-132">TAPI version</span></span><br/> | <span data-ttu-id="1b55f-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1b55f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1b55f-134">Header</span><span class="sxs-lookup"><span data-stu-id="1b55f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="1b55f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b55f-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b55f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="1b55f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1b55f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1b55f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="1b55f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b55f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b55f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b55f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b55f-141">**Itconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="1b55f-141">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="1b55f-142">**BLOB- \_ Zeichen \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="1b55f-142">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

 




