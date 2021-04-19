---
description: Die getphonenumbers-Methode ruft ein Array von Telefonnummern ab, die einem Konferenz-BLOB zugeordnet sind.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'Itsdp:: getphonenumbers-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372478"
---
# <a name="itsdpgetphonenumbers-method"></a><span data-ttu-id="331fa-103">Itsdp:: getphonenumbers-Methode</span><span class="sxs-lookup"><span data-stu-id="331fa-103">ITSdp::GetPhoneNumbers method</span></span>

<span data-ttu-id="331fa-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="331fa-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="331fa-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="331fa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="331fa-106">Die **getphonenumbers** -Methode ruft ein Array von Telefonnummern ab, die einem Konferenz-BLOB zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="331fa-106">The **GetPhoneNumbers** method gets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="331fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="331fa-107">Syntax</span></span>


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="331fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="331fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="331fa-109">*pnumbers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="331fa-109">*pNumbers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="331fa-110">**Variant** -Zeiger auf ein SafeArray von **BSTR** s, das Telefonnummern auflistet.</span><span class="sxs-lookup"><span data-stu-id="331fa-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="331fa-111">*pnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="331fa-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="331fa-112">**Variant** -Zeiger auf ein SafeArray von **BSTR** s-Auflistungs Namen.</span><span class="sxs-lookup"><span data-stu-id="331fa-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="331fa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="331fa-113">Return value</span></span>

<span data-ttu-id="331fa-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="331fa-114">This method can return one of these values.</span></span>



| <span data-ttu-id="331fa-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="331fa-115">Return code</span></span>                                                                                   | <span data-ttu-id="331fa-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="331fa-116">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="331fa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="331fa-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="331fa-118">Method succeeded.</span></span><br/>                                            |
| <dl> <span data-ttu-id="331fa-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="331fa-120">Der *pnumbers* -oder *pnames* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="331fa-120">The *pNumbers* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="331fa-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="331fa-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="331fa-122">Insufficient memory exists to perform the operation.</span></span><br/>         |
| <dl> <span data-ttu-id="331fa-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="331fa-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="331fa-124">Unspecified error.</span></span><br/>                                           |
| <dl> <span data-ttu-id="331fa-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="331fa-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="331fa-126">This method is not yet implemented.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="331fa-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="331fa-127">Remarks</span></span>

<span data-ttu-id="331fa-128">Die Listen, auf die *pnumbers* und *pnames* zeigen, haben dieselbe Länge.</span><span class="sxs-lookup"><span data-stu-id="331fa-128">The lists that *pNumbers* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="331fa-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="331fa-129">Requirements</span></span>



| <span data-ttu-id="331fa-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="331fa-130">Requirement</span></span> | <span data-ttu-id="331fa-131">Wert</span><span class="sxs-lookup"><span data-stu-id="331fa-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="331fa-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="331fa-132">TAPI version</span></span><br/> | <span data-ttu-id="331fa-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="331fa-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="331fa-134">Header</span><span class="sxs-lookup"><span data-stu-id="331fa-134">Header</span></span><br/>       | <dl> <span data-ttu-id="331fa-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="331fa-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="331fa-136">Library</span></span><br/>      | <dl> <span data-ttu-id="331fa-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="331fa-138">DLL</span><span class="sxs-lookup"><span data-stu-id="331fa-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="331fa-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="331fa-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="331fa-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="331fa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331fa-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="331fa-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




