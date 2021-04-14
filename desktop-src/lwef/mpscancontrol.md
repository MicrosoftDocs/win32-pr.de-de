---
title: Mpscancontrol-Funktion (mpclient. h)
description: Ermöglicht das Steuern einer Überprüfung, die asynchron über mpscanstart initiiert wurde.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Mpscancontrol-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476497"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="1e423-104">Mpscancontrol-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e423-104">MpScanControl function</span></span>

<span data-ttu-id="1e423-105">Ermöglicht das Steuern einer Überprüfung, die asynchron über [**mpscanstart**](mpscanstart.md)initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1e423-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e423-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e423-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="1e423-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e423-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e423-108">*hscanhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e423-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e423-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="1e423-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="1e423-110">Handle für einen asynchronen Scanvorgang.</span><span class="sxs-lookup"><span data-stu-id="1e423-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="1e423-111">Dieses Handle wird von der [**mpscanstart**](mpscanstart.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e423-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="1e423-112">Dieser Parameter kann auch auf das von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegebene Malware Protection Manager-Schnittstellen handle festgelegt werden, um eine vom System initiierte Überprüfung zu steuern. in diesem Fall muss der Aufrufer über Administrator Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="1e423-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="1e423-113">*SCANcontrol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e423-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e423-114">Typ: **MPControl**</span><span class="sxs-lookup"><span data-stu-id="1e423-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="1e423-115">Gibt eine Scan Steuerungs Option an.</span><span class="sxs-lookup"><span data-stu-id="1e423-115">Specifies a scan control option.</span></span> <span data-ttu-id="1e423-116">Dieser Parameter muss eine der folgenden Steuerungs Optionen sein:</span><span class="sxs-lookup"><span data-stu-id="1e423-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="1e423-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1e423-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="1e423-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1e423-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="1e423-119"><dt>**Mpcontrol- \_ Abbruch**</dt></span><span class="sxs-lookup"><span data-stu-id="1e423-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="1e423-120">Abbrechen des Scanvorgangs.</span><span class="sxs-lookup"><span data-stu-id="1e423-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="1e423-121"><dt>**Mpcontrol- \_ Pause**</dt></span><span class="sxs-lookup"><span data-stu-id="1e423-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="1e423-122">Hält den Scanvorgang an.</span><span class="sxs-lookup"><span data-stu-id="1e423-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="1e423-123"><dt>**Mpcontrol-Fortsetzung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1e423-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="1e423-124">Setzen Sie den angehaltenen Scanvorgang fort.</span><span class="sxs-lookup"><span data-stu-id="1e423-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e423-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e423-125">Return value</span></span>

<span data-ttu-id="1e423-126">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1e423-126">Type: **HRESULT**</span></span>

<span data-ttu-id="1e423-127">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e423-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="1e423-128">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="1e423-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="1e423-129">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e423-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e423-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e423-130">Requirements</span></span>



| <span data-ttu-id="1e423-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e423-131">Requirement</span></span> | <span data-ttu-id="1e423-132">Wert</span><span class="sxs-lookup"><span data-stu-id="1e423-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e423-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e423-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1e423-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e423-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1e423-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e423-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1e423-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e423-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e423-137">Header</span><span class="sxs-lookup"><span data-stu-id="1e423-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e423-138"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e423-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e423-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1e423-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e423-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e423-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e423-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e423-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e423-142">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="1e423-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="1e423-143">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="1e423-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="1e423-144">**Mpscanstart**</span><span class="sxs-lookup"><span data-stu-id="1e423-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





