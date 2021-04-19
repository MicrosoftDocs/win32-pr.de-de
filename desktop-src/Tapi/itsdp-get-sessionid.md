---
description: Die get \_ SessionID-Methode ruft den 32-Bit-NTP (Network Time Protocol)-Wert ab, der als Sitzungs Bezeichner fungiert. Diese wird automatisch generiert, wenn die Sitzung erstellt wird.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'Itsdp:: get_SessionId-Methode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358378"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="0da6f-104">Itsdp:: get \_ SessionID-Methode</span><span class="sxs-lookup"><span data-stu-id="0da6f-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="0da6f-105">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0da6f-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0da6f-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0da6f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0da6f-107">Die **get \_ SessionID** -Methode ruft den 32-Bit-NTP (Network Time Protocol)-Wert ab, der als Sitzungs Bezeichner fungiert.</span><span class="sxs-lookup"><span data-stu-id="0da6f-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="0da6f-108">Diese wird automatisch generiert, wenn die Sitzung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0da6f-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="0da6f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0da6f-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="0da6f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0da6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da6f-111">*psessionid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0da6f-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0da6f-112">Zeiger auf den Sitzungs Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="0da6f-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da6f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0da6f-113">Return value</span></span>

<span data-ttu-id="0da6f-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="0da6f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0da6f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0da6f-115">Return code</span></span>                                                                                   | <span data-ttu-id="0da6f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0da6f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0da6f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0da6f-118">Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0da6f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0da6f-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0da6f-120">Der *psessionid* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="0da6f-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="0da6f-121"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0da6f-122">Der *psessionid* -Parameter ist kein gültiger Zeiger.</span><span class="sxs-lookup"><span data-stu-id="0da6f-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="0da6f-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0da6f-124">Zum Ausführen des Vorgangs ist nicht genügend Arbeitsspeicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0da6f-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0da6f-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0da6f-126">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="0da6f-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0da6f-127"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0da6f-128">Diese Methode ist noch nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="0da6f-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0da6f-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0da6f-129">Remarks</span></span>

<span data-ttu-id="0da6f-130">Der Rückgabewert dieser Methode kann **ulong** lauten, Visual Basic den **ulong** -Typ jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0da6f-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="0da6f-131">Ein **Double** ist der nächste kleinste Typ, der den gesamten erforderlichen Wertebereich umfasst.</span><span class="sxs-lookup"><span data-stu-id="0da6f-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="0da6f-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0da6f-132">Requirements</span></span>



| <span data-ttu-id="0da6f-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0da6f-133">Requirement</span></span> | <span data-ttu-id="0da6f-134">Wert</span><span class="sxs-lookup"><span data-stu-id="0da6f-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0da6f-135">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0da6f-135">TAPI version</span></span><br/> | <span data-ttu-id="0da6f-136">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0da6f-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0da6f-137">Header</span><span class="sxs-lookup"><span data-stu-id="0da6f-137">Header</span></span><br/>       | <dl> <span data-ttu-id="0da6f-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0da6f-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0da6f-139">Library</span></span><br/>      | <dl> <span data-ttu-id="0da6f-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0da6f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0da6f-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="0da6f-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0da6f-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0da6f-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0da6f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da6f-144">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="0da6f-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




