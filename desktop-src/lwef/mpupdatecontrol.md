---
title: Mpupdatecontrol-Funktion (mpclient. h)
description: Ermöglicht das Steuern eines Signatur Aktualisierungs Vorgangs, der asynchron über mpupdatestart initiiert wurde.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Mpupdatecontrol-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477655"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="ee48f-104">Mpupdatecontrol-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee48f-104">MpUpdateControl function</span></span>

<span data-ttu-id="ee48f-105">Ermöglicht das Steuern eines Signatur Aktualisierungs Vorgangs, der asynchron über [**mpupdatestart**](mpupdatestart.md)initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ee48f-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="ee48f-106">Zum Aufrufen dieser Funktion ist Administrator Berechtigung erforderlich, da Sie den Abbruch eines systemweiten Signatur Updates zulässt.</span><span class="sxs-lookup"><span data-stu-id="ee48f-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee48f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee48f-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="ee48f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee48f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee48f-109">*hupdatehandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee48f-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee48f-110">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="ee48f-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="ee48f-111">Handle für einen asynchronen Signatur Aktualisierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ee48f-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="ee48f-112">Dieses Handle wird von der [**mpscanstart**](mpscanstart.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee48f-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ee48f-113">*Updatecontrol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee48f-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee48f-114">Typ: **MPControl**</span><span class="sxs-lookup"><span data-stu-id="ee48f-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="ee48f-115">Gibt die Option zum Aktualisieren der Signatur Aktualisierung an.</span><span class="sxs-lookup"><span data-stu-id="ee48f-115">Specifies the signature update control option.</span></span> <span data-ttu-id="ee48f-116">Er muss den folgenden Wert aufweisen:</span><span class="sxs-lookup"><span data-stu-id="ee48f-116">It must be the following value:</span></span>



| <span data-ttu-id="ee48f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ee48f-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="ee48f-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ee48f-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="ee48f-119"><dt>**Mpcontrol- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="ee48f-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="ee48f-120">Brechen Sie den Signatur Aktualisierungs Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="ee48f-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee48f-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee48f-121">Return value</span></span>

<span data-ttu-id="ee48f-122">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee48f-122">Type: **HRESULT**</span></span>

<span data-ttu-id="ee48f-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ee48f-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="ee48f-124">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="ee48f-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="ee48f-125">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee48f-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee48f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee48f-126">Requirements</span></span>



| <span data-ttu-id="ee48f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee48f-127">Requirement</span></span> | <span data-ttu-id="ee48f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="ee48f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee48f-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee48f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ee48f-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee48f-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ee48f-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee48f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ee48f-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ee48f-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee48f-133">Header</span><span class="sxs-lookup"><span data-stu-id="ee48f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee48f-134"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee48f-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ee48f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ee48f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee48f-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee48f-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee48f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee48f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee48f-138">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="ee48f-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="ee48f-139">**Mpscanstart**</span><span class="sxs-lookup"><span data-stu-id="ee48f-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





