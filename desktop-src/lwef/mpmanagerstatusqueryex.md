---
title: Mpmanagerstatus-QUERYEX-Funktion (mpclient. h)
description: Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück. | Mpmanagerstatus-QUERYEX-Funktion (mpclient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Mpmanagerstatus-QUERYEX-Funktion Legacy Features der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361173"
---
# <a name="mpmanagerstatusqueryex-function"></a><span data-ttu-id="de016-105">Mpmanagerstatus-QUERYEX-Funktion</span><span class="sxs-lookup"><span data-stu-id="de016-105">MpManagerStatusQueryEx function</span></span>

<span data-ttu-id="de016-106">Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="de016-106">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="de016-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de016-107">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="de016-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de016-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de016-109">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de016-109">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de016-110">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="de016-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="de016-111">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="de016-111">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="de016-112">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="de016-112">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="de016-113">*dwFlag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de016-113">*dwFlag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de016-114">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="de016-114">Type: **DWORD**</span></span>

<span data-ttu-id="de016-115">Steuert, welche Abfrage Informationen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="de016-115">Controls which query information is returned.</span></span> <span data-ttu-id="de016-116">Einige Informationen sind aufwendig und werden möglicherweise nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="de016-116">Some information is expensive and may not be needed.</span></span>



| <span data-ttu-id="de016-117">Wert</span><span class="sxs-lookup"><span data-stu-id="de016-117">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="de016-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="de016-118">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <span data-ttu-id="de016-119"><dt>**MP- \_ Status \_ Abfrage Flags " \_ \_ None"**</dt></span><span class="sxs-lookup"><span data-stu-id="de016-119"><dt>**MP\_STATUS\_QUERY\_FLAGS\_NONE**</dt></span></span> </dl>       | <span data-ttu-id="de016-120">Standard.</span><span class="sxs-lookup"><span data-stu-id="de016-120">Default.</span></span><br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <span data-ttu-id="de016-121"><dt>**MP \_ - \_ statusabfrageflag \_ \_ nostate**</dt></span><span class="sxs-lookup"><span data-stu-id="de016-121"><dt>**MP\_STATUS\_QUERY\_FLAG\_NOSTATE**</dt></span></span> </dl> | <span data-ttu-id="de016-122">Keine Abfrage von Zustandsinformationen.</span><span class="sxs-lookup"><span data-stu-id="de016-122">Do not query for state information.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="de016-123">*pstatusinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="de016-123">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de016-124">Typ: **pmpstatus- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="de016-124">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="de016-125">Zeiger auf eine-Struktur, die Statusinformationen zu den letzten Scans, aktiven Bedrohungen und verschiedenen Komponenten Status zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="de016-125">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="de016-126">Siehe [**mpstatus- \_ Informationen**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="de016-126">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de016-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de016-127">Return value</span></span>

<span data-ttu-id="de016-128">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="de016-128">Type: **HRESULT**</span></span>

<span data-ttu-id="de016-129">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="de016-129">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="de016-130">Dieser Funktions Aufrufvorgang ist garantiert auch dann erfolgreich, wenn kein antischadsoftwaredienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de016-130">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="de016-131">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="de016-131">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="de016-132">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="de016-132">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="de016-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de016-133">Requirements</span></span>



| <span data-ttu-id="de016-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de016-134">Requirement</span></span> | <span data-ttu-id="de016-135">Wert</span><span class="sxs-lookup"><span data-stu-id="de016-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de016-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de016-136">Minimum supported client</span></span><br/> | <span data-ttu-id="de016-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de016-137">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="de016-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de016-138">Minimum supported server</span></span><br/> | <span data-ttu-id="de016-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de016-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="de016-140">Header</span><span class="sxs-lookup"><span data-stu-id="de016-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="de016-141"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="de016-141"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="de016-142">DLL</span><span class="sxs-lookup"><span data-stu-id="de016-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de016-143"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de016-143"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de016-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de016-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de016-145">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="de016-145">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="de016-146">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="de016-146">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="de016-147">**mpstatus- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="de016-147">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





