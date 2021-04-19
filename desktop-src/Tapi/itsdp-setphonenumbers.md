---
description: Mit der setphonenumbers-Methode wird ein Array von Telefonnummern festgelegt, die einem Konferenz-BLOB zugeordnet sind.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'Itsdp:: setphonenumbers-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367086"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="86f2b-103">Itsdp:: setphonenumbers-Methode</span><span class="sxs-lookup"><span data-stu-id="86f2b-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="86f2b-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86f2b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86f2b-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="86f2b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="86f2b-106">Mit der **setphonenumbers** -Methode wird ein Array von Telefonnummern festgelegt, die einem Konferenz-BLOB zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="86f2b-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f2b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="86f2b-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="86f2b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="86f2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f2b-109">*Zahlen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86f2b-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f2b-110">SafeArray von **BSTR** s Auflisten von Telefonnummern.</span><span class="sxs-lookup"><span data-stu-id="86f2b-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="86f2b-111">*Namen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86f2b-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f2b-112">SafeArray von **BSTR** s-Auflistungs Namen.</span><span class="sxs-lookup"><span data-stu-id="86f2b-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86f2b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86f2b-113">Return value</span></span>

<span data-ttu-id="86f2b-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="86f2b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="86f2b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86f2b-115">Return code</span></span>                                                                                   | <span data-ttu-id="86f2b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86f2b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="86f2b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="86f2b-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="86f2b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="86f2b-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="86f2b-120">Der Parameter " *Numbers* " und " *Names* " ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="86f2b-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="86f2b-121"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="86f2b-122">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="86f2b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="86f2b-123"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="86f2b-124">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="86f2b-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86f2b-125"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="86f2b-126">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="86f2b-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="86f2b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86f2b-127">Remarks</span></span>

<span data-ttu-id="86f2b-128">Die Liste, auf die *Zahlen* und *Namen* zeigen, ist dieselbe Länge.</span><span class="sxs-lookup"><span data-stu-id="86f2b-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="86f2b-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86f2b-129">Requirements</span></span>



| <span data-ttu-id="86f2b-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86f2b-130">Requirement</span></span> | <span data-ttu-id="86f2b-131">Wert</span><span class="sxs-lookup"><span data-stu-id="86f2b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86f2b-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="86f2b-132">TAPI version</span></span><br/> | <span data-ttu-id="86f2b-133">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="86f2b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="86f2b-134">Header</span><span class="sxs-lookup"><span data-stu-id="86f2b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="86f2b-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="86f2b-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86f2b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="86f2b-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86f2b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="86f2b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="86f2b-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86f2b-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86f2b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86f2b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f2b-141">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="86f2b-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




