---
description: Die \_ Methode Get conferenceblob erhält einen Zeiger auf das Textkonferenz-BLOB, das zurzeit im Konferenz-BLOB-Objekt gespeichert ist.
ms.assetid: eb378f84-11bc-4f6e-9133-bc303e07eb53
title: 'Itconferendceblob:: get_ConferenceBlob-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5642f60f7abc1cb10734de1897d35bd5222dd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353001"
---
# <a name="itconferenceblobget_conferenceblob-method"></a><span data-ttu-id="22e5f-103">Itconferendceblob:: get- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="22e5f-103">ITConferenceBlob::get\_ConferenceBlob method</span></span>

<span data-ttu-id="22e5f-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22e5f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="22e5f-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="22e5f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="22e5f-106">Die Methode **get \_ conferenceblob** erhält einen Zeiger auf das Textkonferenz-BLOB, das zurzeit im Konferenz-BLOB-Objekt gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="22e5f-106">The **get\_ConferenceBlob** method gets a pointer to the textual conference blob currently stored in the conference blob object.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e5f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="22e5f-107">Syntax</span></span>


```C++
HRESULT get_ConferenceBlob(
  [out] BSTR *ppBlob
);
```



## <a name="parameters"></a><span data-ttu-id="22e5f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="22e5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e5f-109">*ppBlob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="22e5f-109">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22e5f-110">Zeiger auf ein **BSTR** , das das Konferenz-BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="22e5f-110">Pointer to a **BSTR** containing the conference blob.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e5f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22e5f-111">Return value</span></span>

<span data-ttu-id="22e5f-112">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="22e5f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="22e5f-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22e5f-113">Return code</span></span>                                                                                   | <span data-ttu-id="22e5f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22e5f-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="22e5f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="22e5f-116">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="22e5f-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="22e5f-117"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="22e5f-118">Der *ppBlob* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="22e5f-118">The *ppBlob* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="22e5f-119"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="22e5f-120">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="22e5f-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="22e5f-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="22e5f-122">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="22e5f-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="22e5f-123"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="22e5f-124">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="22e5f-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="22e5f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22e5f-125">Remarks</span></span>

<span data-ttu-id="22e5f-126">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) verwenden, um den für den *ppBlob* -Parameter zugeordneten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="22e5f-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppBlob* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="22e5f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22e5f-127">Requirements</span></span>



| <span data-ttu-id="22e5f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22e5f-128">Requirement</span></span> | <span data-ttu-id="22e5f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="22e5f-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22e5f-130">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="22e5f-130">TAPI version</span></span><br/> | <span data-ttu-id="22e5f-131">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="22e5f-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="22e5f-132">Header</span><span class="sxs-lookup"><span data-stu-id="22e5f-132">Header</span></span><br/>       | <dl> <span data-ttu-id="22e5f-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="22e5f-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="22e5f-134">Library</span></span><br/>      | <dl> <span data-ttu-id="22e5f-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="22e5f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="22e5f-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="22e5f-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22e5f-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22e5f-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22e5f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e5f-139">**Itconfererceblob**</span><span class="sxs-lookup"><span data-stu-id="22e5f-139">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="22e5f-140">**BLOB- \_ Zeichen \_ Satz**</span><span class="sxs-lookup"><span data-stu-id="22e5f-140">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

