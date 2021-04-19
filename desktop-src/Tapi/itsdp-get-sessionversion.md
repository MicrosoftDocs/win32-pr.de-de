---
description: Die get \_ sessionversion-Methode ruft den 32-Bit-Wert (idealerweise Network Time Protocol oder NTP) ab, der als Sitzungs Version fungiert.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Itsdp:: get_SessionVersion-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372014"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="4a67c-103">Itsdp:: get \_ sessionversion-Methode</span><span class="sxs-lookup"><span data-stu-id="4a67c-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="4a67c-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4a67c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4a67c-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4a67c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4a67c-106">Die **get \_ sessionversion** -Methode ruft den 32-Bit-Wert (idealerweise Network Time Protocol oder NTP) ab, der als Sitzungs Version fungiert.</span><span class="sxs-lookup"><span data-stu-id="4a67c-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="4a67c-107">Obwohl dies bei der Erstellung der Sitzung automatisch generiert wird, ist der Benutzer dafür verantwortlich, ihn zu ändern, wenn der SDP geändert wird.</span><span class="sxs-lookup"><span data-stu-id="4a67c-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a67c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a67c-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="4a67c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a67c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a67c-110">*psessionversion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4a67c-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a67c-111">Zeiger auf den Sitzungs Versions Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="4a67c-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a67c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a67c-112">Return value</span></span>

<span data-ttu-id="4a67c-113">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4a67c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="4a67c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4a67c-114">Return code</span></span>                                                                                   | <span data-ttu-id="4a67c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a67c-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a67c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4a67c-117">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="4a67c-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="4a67c-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4a67c-119">Der *psessionversion* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="4a67c-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="4a67c-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4a67c-121">Der *psessionversion* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="4a67c-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="4a67c-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4a67c-123">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4a67c-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="4a67c-124"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4a67c-125">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="4a67c-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="4a67c-126"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4a67c-127">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="4a67c-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="4a67c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a67c-128">Remarks</span></span>

<span data-ttu-id="4a67c-129">Der Rückgabewert dieser Methode kann **ulong** lauten, Visual Basic den **ulong** -Typ jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4a67c-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="4a67c-130">Ein **Double** ist der nächste kleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.</span><span class="sxs-lookup"><span data-stu-id="4a67c-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a67c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a67c-131">Requirements</span></span>



| <span data-ttu-id="4a67c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a67c-132">Requirement</span></span> | <span data-ttu-id="4a67c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="4a67c-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a67c-134">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="4a67c-134">TAPI version</span></span><br/> | <span data-ttu-id="4a67c-135">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4a67c-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4a67c-136">Header</span><span class="sxs-lookup"><span data-stu-id="4a67c-136">Header</span></span><br/>       | <dl> <span data-ttu-id="4a67c-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a67c-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a67c-138">Library</span></span><br/>      | <dl> <span data-ttu-id="4a67c-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4a67c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4a67c-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="4a67c-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a67c-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a67c-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a67c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a67c-143">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="4a67c-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="4a67c-144">**Itsdp::p UT \_ sessionversion**</span><span class="sxs-lookup"><span data-stu-id="4a67c-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




