---
description: Die Init-Methode initialisiert das Konferenz-BLOB auf Grundlage einer Text Zeichenfolge. Wenn pBlob den Wert NULL hat, werden Standardwerte verwendet.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Itconferendceblob:: Init-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369709"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="1c7b3-104">Itconferendceblob:: Init-Methode</span><span class="sxs-lookup"><span data-stu-id="1c7b3-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="1c7b3-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c7b3-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1c7b3-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1c7b3-107">Die **Init** -Methode initialisiert das Konferenz-BLOB auf Grundlage einer Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="1c7b3-108">Wenn *pBlob* den Wert **null** hat, werden Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c7b3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c7b3-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="1c7b3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c7b3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c7b3-111">*PName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c7b3-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7b3-112">Zeiger auf eine **BSTR** -Darstellung des Konferenz namens.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="1c7b3-113">*Merkmal Satz* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c7b3-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7b3-114">[**BLOB \_ \_Zeichensatz**](blob-character-set.md) Deskriptor des Zeichensatzes.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="1c7b3-115">*pBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c7b3-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c7b3-116">Zeiger auf ein **BSTR** , das das Konferenz-BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="1c7b3-117">Wenn der Wert **null** ist, wird das Konferenz-BLOB mit den Standardwerten initialisiert.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="1c7b3-118">Derzeit sind Standard-Konferenz Werte nur verfügbar, wenn der Parameter " *Merkmal Satz* " auf BCS ASCII festgelegt ist \_ .</span><span class="sxs-lookup"><span data-stu-id="1c7b3-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c7b3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1c7b3-119">Return value</span></span>

<span data-ttu-id="1c7b3-120">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-120">This method can return one of these values.</span></span>



| <span data-ttu-id="1c7b3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1c7b3-121">Value</span></span>                                                                                         | <span data-ttu-id="1c7b3-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1c7b3-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c7b3-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1c7b3-124">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1c7b3-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1c7b3-126">Der Parameter " *PName*", " *Merkmal Satz*" oder " *pBlob* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="1c7b3-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1c7b3-128">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="1c7b3-129"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1c7b3-130">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="1c7b3-131"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1c7b3-132">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="1c7b3-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c7b3-133">Remarks</span></span>

<span data-ttu-id="1c7b3-134">**Itconfererceblob:: init** gibt einen Fehler zurück, wenn das BLOB bereits initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="1c7b3-135">Die Anwendung muss " [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) " verwenden, um Arbeitsspeicher für die Parameter " *PName* " und " *pBlob* " zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="1c7b3-136">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den Arbeitsspeicher freizugeben, wenn die Variablen nicht mehr benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="1c7b3-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c7b3-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c7b3-137">Requirements</span></span>



| <span data-ttu-id="1c7b3-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c7b3-138">Requirement</span></span> | <span data-ttu-id="1c7b3-139">Wert</span><span class="sxs-lookup"><span data-stu-id="1c7b3-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c7b3-140">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="1c7b3-140">TAPI version</span></span><br/> | <span data-ttu-id="1c7b3-141">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="1c7b3-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1c7b3-142">Header</span><span class="sxs-lookup"><span data-stu-id="1c7b3-142">Header</span></span><br/>       | <dl> <span data-ttu-id="1c7b3-143"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c7b3-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1c7b3-144">Library</span></span><br/>      | <dl> <span data-ttu-id="1c7b3-145"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1c7b3-146">DLL</span><span class="sxs-lookup"><span data-stu-id="1c7b3-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="1c7b3-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c7b3-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c7b3-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c7b3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c7b3-149">**Itconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="1c7b3-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="1c7b3-150">**BLOB- \_ Zeichen \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="1c7b3-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

