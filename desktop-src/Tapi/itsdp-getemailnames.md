---
description: Die getemailnames-Methode ruft ein Array von e-Mail-Namen ab, die dem Konferenz-BLOB zugeordnet sind
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'Itsdp:: getemailnames-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365919"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="fba3b-103">Itsdp:: getemailnames-Methode</span><span class="sxs-lookup"><span data-stu-id="fba3b-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="fba3b-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fba3b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fba3b-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="fba3b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fba3b-106">Die **getemailnames** -Methode ruft ein Array von e-Mail-Namen ab, die dem Konferenz-BLOB zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="fba3b-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba3b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fba3b-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="fba3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fba3b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba3b-109">*padressen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fba3b-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba3b-110">**Variant** -Zeiger auf ein SafeArray von **BSTR**, das e-Mail-Adressen auflistet.</span><span class="sxs-lookup"><span data-stu-id="fba3b-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="fba3b-111">*pnames* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fba3b-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba3b-112">**Variant** -Zeiger auf ein SafeArray von **BSTR** s-Auflistungs Namen.</span><span class="sxs-lookup"><span data-stu-id="fba3b-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba3b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fba3b-113">Return value</span></span>

<span data-ttu-id="fba3b-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fba3b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="fba3b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fba3b-115">Return code</span></span>                                                                                   | <span data-ttu-id="fba3b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fba3b-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fba3b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fba3b-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fba3b-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="fba3b-119"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="fba3b-120">Der *padressen* -oder *pnames* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="fba3b-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="fba3b-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fba3b-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fba3b-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="fba3b-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="fba3b-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="fba3b-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="fba3b-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="fba3b-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="fba3b-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="fba3b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fba3b-127">Remarks</span></span>

<span data-ttu-id="fba3b-128">Die Listen, auf die *padressen* und *pnames* zeigen, haben dieselbe Länge.</span><span class="sxs-lookup"><span data-stu-id="fba3b-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="fba3b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fba3b-129">Requirements</span></span>



| <span data-ttu-id="fba3b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fba3b-130">Requirement</span></span> | <span data-ttu-id="fba3b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="fba3b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fba3b-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="fba3b-132">TAPI version</span></span><br/> | <span data-ttu-id="fba3b-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fba3b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="fba3b-134">Header</span><span class="sxs-lookup"><span data-stu-id="fba3b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="fba3b-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="fba3b-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fba3b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="fba3b-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fba3b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fba3b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="fba3b-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba3b-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba3b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fba3b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba3b-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="fba3b-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




