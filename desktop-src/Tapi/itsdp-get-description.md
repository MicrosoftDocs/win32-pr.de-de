---
description: Die get \_ Description-Methode ruft die Sitzungs Beschreibung (BSTR) ab.
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'Itsdp:: get_Description-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354836"
---
# <a name="itsdpget_description-method"></a><span data-ttu-id="4cd27-103">Itsdp:: get \_ Description-Methode</span><span class="sxs-lookup"><span data-stu-id="4cd27-103">ITSdp::get\_Description method</span></span>

<span data-ttu-id="4cd27-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4cd27-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4cd27-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4cd27-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4cd27-106">Die **get \_ Description** -Methode ruft die Sitzungs Beschreibung (**BSTR**) ab.</span><span class="sxs-lookup"><span data-stu-id="4cd27-106">The **get\_Description** method gets the session description (**BSTR**).</span></span> <span data-ttu-id="4cd27-107">Dies muss eine ASCII-konvertierbare Zeichenfolge sein, wenn es sich um einen ASCII-Zeichensatz handelt.</span><span class="sxs-lookup"><span data-stu-id="4cd27-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="4cd27-108">(Andernfalls kann es sich um eine beliebige **BSTR** -Zeichenfolge handeln.)</span><span class="sxs-lookup"><span data-stu-id="4cd27-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="4cd27-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4cd27-109">Syntax</span></span>


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a><span data-ttu-id="4cd27-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4cd27-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cd27-111">*ppdescription* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4cd27-111">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4cd27-112">Zeiger auf einen **BSTR** -Wert, der die Sitzungs Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="4cd27-112">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cd27-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4cd27-113">Return value</span></span>

<span data-ttu-id="4cd27-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4cd27-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4cd27-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4cd27-115">Return code</span></span>                                                                                   | <span data-ttu-id="4cd27-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4cd27-116">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="4cd27-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4cd27-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4cd27-118">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4cd27-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4cd27-120">Der *ppdescription* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4cd27-120">The *ppDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="4cd27-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4cd27-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4cd27-122">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="4cd27-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4cd27-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="4cd27-124">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4cd27-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4cd27-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4cd27-126">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="4cd27-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cd27-127">Remarks</span></span>

<span data-ttu-id="4cd27-128">Die Anwendung muss [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) zum Freigeben des *ppdescription* -Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="4cd27-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the *ppDescription* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cd27-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cd27-129">Requirements</span></span>



| <span data-ttu-id="4cd27-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cd27-130">Requirement</span></span> | <span data-ttu-id="4cd27-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4cd27-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cd27-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4cd27-132">TAPI version</span></span><br/> | <span data-ttu-id="4cd27-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4cd27-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4cd27-134">Header</span><span class="sxs-lookup"><span data-stu-id="4cd27-134">Header</span></span><br/>       | <dl> <span data-ttu-id="4cd27-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4cd27-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4cd27-136">Library</span></span><br/>      | <dl> <span data-ttu-id="4cd27-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4cd27-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4cd27-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="4cd27-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cd27-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cd27-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cd27-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cd27-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="4cd27-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="4cd27-142">**Itsdp::p UT- \_ Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4cd27-142">**ITSdp::put\_Description**</span></span>](itsdp-put-description.md)
</dt> </dl>

 

