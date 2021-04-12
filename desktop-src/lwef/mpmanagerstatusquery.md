---
title: Mpmanagerstatus Query-Funktion (mpclient. h)
description: Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück. | Mpmanagerstatus Query-Funktion (mpclient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Mpmanagerstatus Query-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352249"
---
# <a name="mpmanagerstatusquery-function"></a><span data-ttu-id="2beb1-105">Mpmanagerstatus Query-Funktion</span><span class="sxs-lookup"><span data-stu-id="2beb1-105">MpManagerStatusQuery function</span></span>

<span data-ttu-id="2beb1-106">\[**Mpmanagerstatus Query** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2beb1-106">\[**MpManagerStatusQuery** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="2beb1-107">Verwenden Sie stattdessen [**mpmanagerstatus-QUERYEX**](mpmanagerstatusqueryex.md).\]</span><span class="sxs-lookup"><span data-stu-id="2beb1-107">Instead, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]</span></span>

<span data-ttu-id="2beb1-108">Gibt Statusinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="2beb1-108">Returns status information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="2beb1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2beb1-109">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2beb1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2beb1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2beb1-111">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2beb1-111">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2beb1-112">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="2beb1-112">Type: **MPHANDLE**</span></span>

<span data-ttu-id="2beb1-113">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2beb1-113">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="2beb1-114">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2beb1-114">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2beb1-115">*pstatusinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2beb1-115">*pStatusInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2beb1-116">Typ: **pmpstatus- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="2beb1-116">Type: **PMPSTATUS\_INFO**</span></span>

<span data-ttu-id="2beb1-117">Zeiger auf eine-Struktur, die Statusinformationen zu den letzten Scans, aktiven Bedrohungen und verschiedenen Komponenten Status zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2beb1-117">Pointer to a structure that returns status information regarding last scans, active threats and various component status.</span></span> <span data-ttu-id="2beb1-118">Siehe [**mpstatus- \_ Informationen**](mpstatus-info.md).</span><span class="sxs-lookup"><span data-stu-id="2beb1-118">See [**MPSTATUS\_INFO**](mpstatus-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2beb1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2beb1-119">Return value</span></span>

<span data-ttu-id="2beb1-120">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2beb1-120">Type: **HRESULT**</span></span>

<span data-ttu-id="2beb1-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2beb1-121">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="2beb1-122">Dieser Funktions Aufrufvorgang ist garantiert auch dann erfolgreich, wenn kein antischadsoftwaredienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2beb1-122">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="2beb1-123">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="2beb1-123">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="2beb1-124">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2beb1-124">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2beb1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2beb1-125">Requirements</span></span>



| <span data-ttu-id="2beb1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2beb1-126">Requirement</span></span> | <span data-ttu-id="2beb1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2beb1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2beb1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2beb1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2beb1-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2beb1-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="2beb1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2beb1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2beb1-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2beb1-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2beb1-132">Header</span><span class="sxs-lookup"><span data-stu-id="2beb1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2beb1-133"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2beb1-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2beb1-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2beb1-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2beb1-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2beb1-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2beb1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2beb1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2beb1-137">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="2beb1-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="2beb1-138">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="2beb1-138">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="2beb1-139">**Mpmanagerstatus-QUERYEX**</span><span class="sxs-lookup"><span data-stu-id="2beb1-139">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="2beb1-140">**mpstatus- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="2beb1-140">**MPSTATUS\_INFO**</span></span>](mpstatus-info.md)
</dt> </dl>

 

 





