---
description: Die setemailnames-Methode legt ein Array von e-Mail-Adressen fest, das dem Konferenz-BLOB zugeordnet ist.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'Itsdp:: Setup Mail Names-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367087"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="098d1-103">Itsdp:: Server Mail Names-Methode</span><span class="sxs-lookup"><span data-stu-id="098d1-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="098d1-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="098d1-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="098d1-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="098d1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="098d1-106">Die **setemailnames** -Methode legt ein Array von e-Mail-Adressen fest, das dem Konferenz-BLOB zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="098d1-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="098d1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="098d1-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="098d1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="098d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="098d1-109">*Adressen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="098d1-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098d1-110">SAFEARRAY der **BSTR**-e-Mail-Adressen.</span><span class="sxs-lookup"><span data-stu-id="098d1-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="098d1-111">*Namen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="098d1-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="098d1-112">SafeArray von **BSTR** s-Auflistungs Namen.</span><span class="sxs-lookup"><span data-stu-id="098d1-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="098d1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="098d1-113">Return value</span></span>

<span data-ttu-id="098d1-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="098d1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="098d1-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="098d1-115">Return code</span></span>                                                                                   | <span data-ttu-id="098d1-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="098d1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="098d1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="098d1-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="098d1-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="098d1-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="098d1-120">Der Parameter " *Adressen* " oder " *Names* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="098d1-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="098d1-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="098d1-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="098d1-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="098d1-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="098d1-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="098d1-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="098d1-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="098d1-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="098d1-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="098d1-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="098d1-127">Remarks</span></span>

<span data-ttu-id="098d1-128">Die Liste, auf die *Adressen* und *Namen* zeigen, haben dieselbe Länge.</span><span class="sxs-lookup"><span data-stu-id="098d1-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="098d1-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="098d1-129">Requirements</span></span>



| <span data-ttu-id="098d1-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="098d1-130">Requirement</span></span> | <span data-ttu-id="098d1-131">Wert</span><span class="sxs-lookup"><span data-stu-id="098d1-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="098d1-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="098d1-132">TAPI version</span></span><br/> | <span data-ttu-id="098d1-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="098d1-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="098d1-134">Header</span><span class="sxs-lookup"><span data-stu-id="098d1-134">Header</span></span><br/>       | <dl> <span data-ttu-id="098d1-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="098d1-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="098d1-136">Library</span></span><br/>      | <dl> <span data-ttu-id="098d1-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="098d1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="098d1-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="098d1-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="098d1-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098d1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="098d1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098d1-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="098d1-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




