---
title: Mperate Enumerate-Funktion (mpclient. h)
description: Gibt Informationen über die nächste Bedrohung in der Enumerationsliste zurück. Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen vollständig ist.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Mpenenumerate-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956835"
---
# <a name="mpthreatenumerate-function"></a><span data-ttu-id="b9adc-105">Mpbedrohlich Enumerate-Funktion</span><span class="sxs-lookup"><span data-stu-id="b9adc-105">MpThreatEnumerate function</span></span>

<span data-ttu-id="b9adc-106">Gibt Informationen über die nächste Bedrohung in der Enumerationsliste zurück.</span><span class="sxs-lookup"><span data-stu-id="b9adc-106">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="b9adc-107">Diese Funktion kann wiederholt aufgerufen werden, bis die Enumeration aller Bedrohungen vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="b9adc-107">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9adc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9adc-108">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b9adc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9adc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9adc-110">*hbedrohlich-enumhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9adc-110">*hThreatEnumHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9adc-111">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="b9adc-111">Type: **MPHANDLE**</span></span>

<span data-ttu-id="b9adc-112">Handle für einen Bedrohungs enumerationskontext, der von [**mpbedrohlich Open**](mpthreatopen.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b9adc-112">Handle to a threat enumeration context returned by [**MpThreatOpen**](mpthreatopen.md).</span></span>

</dd> <dt>

<span data-ttu-id="b9adc-113">*ppbedrohlich Info* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b9adc-113">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9adc-114">Typ: \**pmpthreat \_ Info \** _</span><span class="sxs-lookup"><span data-stu-id="b9adc-114">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="b9adc-115">Gibt einen Zeiger auf eine Bedrohungs Informationsstruktur zurück, [_ *mpthreat \_ Info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="b9adc-115">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="b9adc-116">Die Struktur enthält Informationen wie die Bedrohungs-ID, den Namen und den Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="b9adc-116">The structure contains information such as threat id, name, and severity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9adc-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9adc-117">Return value</span></span>

<span data-ttu-id="b9adc-118">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b9adc-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b9adc-119">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9adc-119">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="b9adc-120">Wenn keine weiteren Elemente vorhanden sind, die zurückgegeben werden sollen, ist der Rückgabewert **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b9adc-120">If there are no more items to return the return value is **S\_FALSE**.</span></span>

<span data-ttu-id="b9adc-121">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="b9adc-121">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="b9adc-122">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b9adc-122">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9adc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9adc-123">Requirements</span></span>



| <span data-ttu-id="b9adc-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9adc-124">Requirement</span></span> | <span data-ttu-id="b9adc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="b9adc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9adc-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9adc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b9adc-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9adc-127">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="b9adc-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9adc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b9adc-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9adc-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9adc-130">Header</span><span class="sxs-lookup"><span data-stu-id="b9adc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9adc-131"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9adc-131"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9adc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b9adc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9adc-133"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9adc-133"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9adc-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9adc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9adc-135">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="b9adc-135">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="b9adc-136">**Mpbedrohlich öffnen**</span><span class="sxs-lookup"><span data-stu-id="b9adc-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> <dt>

[<span data-ttu-id="b9adc-137">**mpthreat- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="b9adc-137">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> </dl>

 

 





