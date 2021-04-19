---
title: Mpbedrohlich Query-Funktion (mpclient. h)
description: Wird verwendet, um statische (z. b. Schweregrad und Kategorie) oder lokalisierte Informationen zu einer bestimmten Bedrohung (z. b. Kategorien Beschreibung und Ratschläge) abzufragen.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Mpbedrohlich Query-Funktion Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338721"
---
# <a name="mpthreatquery-function"></a><span data-ttu-id="c4ab0-104">Mpbedrohlich Query-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4ab0-104">MpThreatQuery function</span></span>

<span data-ttu-id="c4ab0-105">Wird verwendet, um statische (z. b. Schweregrad und Kategorie) oder lokalisierte Informationen zu einer bestimmten Bedrohung (z. b. Kategorien Beschreibung und Ratschläge) abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-105">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ab0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ab0-106">Syntax</span></span>


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c4ab0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ab0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ab0-108">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4ab0-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab0-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="c4ab0-110">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="c4ab0-111">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="c4ab0-112">*Threatid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4ab0-112">*ThreatID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab0-113">Typ: **mpthreat- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-113">Type: **MPTHREAT\_ID**</span></span>

<span data-ttu-id="c4ab0-114">Der Bedrohungs Bezeichner, für den Informationen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-114">Threat identifier for which information is requested.</span></span>

</dd> <dt>

<span data-ttu-id="c4ab0-115">*ppbedrohlich Info* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4ab0-115">*ppThreatInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab0-116">Typ: \**pmpthreat \_ Info \** _</span><span class="sxs-lookup"><span data-stu-id="c4ab0-116">Type: \**PMPTHREAT\_INFO\** _</span></span>

<span data-ttu-id="c4ab0-117">Gibt einen Zeiger auf eine Bedrohungs Informationsstruktur zurück, [_ *mpthreat \_ Info* \*](mpthreat-info.md).</span><span class="sxs-lookup"><span data-stu-id="c4ab0-117">Returns a pointer to a threat information structure, [_ *MPTHREAT\_INFO*\*](mpthreat-info.md).</span></span> <span data-ttu-id="c4ab0-118">Die Struktur enthält Informationen wie die Bedrohungs-ID, den Namen und den Schweregrad.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-118">The structure contains information such as threat id, name, and severity.</span></span>

</dd> <dt>

<span data-ttu-id="c4ab0-119">*ppbedrohlich localizedinfo* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="c4ab0-119">*ppThreatLocalizedInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ab0-120">Geben Sie Folgendes ein: \**pmpthreat \_ lokalisierte \_ \* Info* _</span><span class="sxs-lookup"><span data-stu-id="c4ab0-120">Type: \**PMPTHREAT\_LOCALIZED\_INFO\** _</span></span>

<span data-ttu-id="c4ab0-121">Gibt einen Zeiger auf eine-Struktur zurück, die lokalisierte Informationen über die Bedrohung enthält.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-121">Returns a pointer to a structure containing localized information about the threat.</span></span> <span data-ttu-id="c4ab0-122">Sie können _ *null*\* übergeben, wenn Sie nicht an lokalisierten Informationen über die Bedrohung interessiert sind.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-122">You can pass _ *NULL*\* if you are not interested in localized information about the threat.</span></span> <span data-ttu-id="c4ab0-123">Siehe " [**mpthreat \_ lokalisierte \_ Informationen**](mpthreat-localized-info.md)".</span><span class="sxs-lookup"><span data-stu-id="c4ab0-123">See [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ab0-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4ab0-124">Return value</span></span>

<span data-ttu-id="c4ab0-125">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-125">Type: **HRESULT**</span></span>

<span data-ttu-id="c4ab0-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-126">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="c4ab0-127">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-127">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="c4ab0-128">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c4ab0-128">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ab0-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4ab0-129">Requirements</span></span>



| <span data-ttu-id="c4ab0-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4ab0-130">Requirement</span></span> | <span data-ttu-id="c4ab0-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c4ab0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ab0-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4ab0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ab0-133">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4ab0-133">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c4ab0-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4ab0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ab0-135">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4ab0-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4ab0-136">Header</span><span class="sxs-lookup"><span data-stu-id="c4ab0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4ab0-137"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ab0-137"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4ab0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c4ab0-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4ab0-139"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4ab0-139"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4ab0-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4ab0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ab0-141">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-141">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="c4ab0-142">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-142">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="c4ab0-143">**mpthreat- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-143">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="c4ab0-144">**lokalisierte mpthreat- \_ \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="c4ab0-144">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





