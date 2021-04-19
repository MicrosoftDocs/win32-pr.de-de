---
description: Die setconferenceblob-Methode führt einen Commit für Änderungen an das Konferenz-BLOB aus. Verwenden Sie stattdessen die Init-Methode, um das Konferenz-BLOB zum ersten Mal zu initialisieren.
ms.assetid: 4a65edb9-77de-42d9-85a1-1e3c41706417
title: 'Itconfererceblob:: setconfererceblob-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47779807e5bde6a070b4600aec903309c7679dc8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370093"
---
# <a name="itconferenceblobsetconferenceblob-method"></a><span data-ttu-id="176b2-104">Itconfererceblob:: setconfererceblob-Methode</span><span class="sxs-lookup"><span data-stu-id="176b2-104">ITConferenceBlob::SetConferenceBlob method</span></span>

<span data-ttu-id="176b2-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="176b2-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="176b2-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="176b2-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="176b2-107">Die **setconferenceblob** -Methode führt einen Commit für Änderungen an das Konferenz-BLOB aus.</span><span class="sxs-lookup"><span data-stu-id="176b2-107">The **SetConferenceBlob** method commits changes to the conference blob.</span></span> <span data-ttu-id="176b2-108">Verwenden Sie stattdessen die [**Init**](itconferenceblob-init.md) -Methode, um das Konferenz-BLOB zum ersten Mal zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="176b2-108">To initialize the conference blob for the first time, use the [**Init**](itconferenceblob-init.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="176b2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="176b2-109">Syntax</span></span>


```C++
HRESULT SetConferenceBlob(
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="176b2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="176b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="176b2-111">*Merkmal Satz* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="176b2-111">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="176b2-112">[**BLOB \_ \_Zeichensatz**](blob-character-set.md) Deskriptor für den Zeichensatz des Konferenz-BLOBs.</span><span class="sxs-lookup"><span data-stu-id="176b2-112">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the conference blob's character set.</span></span>

</dd> <dt>

<span data-ttu-id="176b2-113">*pBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="176b2-113">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="176b2-114">Zeiger auf ein **BSTR** , das das Konferenz-BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="176b2-114">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="176b2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="176b2-115">Return value</span></span>

<span data-ttu-id="176b2-116">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="176b2-116">This method can return one of these values.</span></span>



| <span data-ttu-id="176b2-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="176b2-117">Return code</span></span>                                                                                   | <span data-ttu-id="176b2-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="176b2-118">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="176b2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="176b2-120">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="176b2-120">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="176b2-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="176b2-122">Der *charakterisetyp* oder der *pBlob* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="176b2-122">The *CharacterSet* or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="176b2-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="176b2-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="176b2-124">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="176b2-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="176b2-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="176b2-126">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="176b2-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="176b2-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="176b2-128">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="176b2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="176b2-129">Remarks</span></span>

<span data-ttu-id="176b2-130">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Speicher für den *pBlob* -Parameter zuzuweisen, und " [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) " verwenden, um den Arbeitsspeicher freizugeben, wenn die Variable nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="176b2-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pBlob* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="176b2-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="176b2-131">Requirements</span></span>



| <span data-ttu-id="176b2-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="176b2-132">Requirement</span></span> | <span data-ttu-id="176b2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="176b2-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="176b2-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="176b2-134">TAPI version</span></span><br/> | <span data-ttu-id="176b2-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="176b2-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="176b2-136">Header</span><span class="sxs-lookup"><span data-stu-id="176b2-136">Header</span></span><br/>       | <dl> <span data-ttu-id="176b2-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="176b2-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="176b2-138">Library</span></span><br/>      | <dl> <span data-ttu-id="176b2-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="176b2-140">DLL</span><span class="sxs-lookup"><span data-stu-id="176b2-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="176b2-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="176b2-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="176b2-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="176b2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="176b2-143">**Itconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="176b2-143">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="176b2-144">**BLOB- \_ Zeichen \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="176b2-144">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

