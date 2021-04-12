---
title: Mplenker Close-Funktion (mpclient. h)
description: Schließt das von mpmanageropen, mpscanstart, mporial Open oder mpupdatestart zurückgegebene Handle.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Mplenker Close-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518755"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="708d8-104">Mplenker Close-Funktion</span><span class="sxs-lookup"><span data-stu-id="708d8-104">MpHandleClose function</span></span>

<span data-ttu-id="708d8-105">Schließt das von [**mpmanageropen**](mpmanageropen.md), [**mpscanstart**](mpscanstart.md), [**mporial Open**](mpthreatopen.md)oder [**mpupdatestart**](mpupdatestart.md)zurückgegebene Handle.</span><span class="sxs-lookup"><span data-stu-id="708d8-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="708d8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="708d8-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="708d8-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="708d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708d8-108">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="708d8-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708d8-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="708d8-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="708d8-110">Handle, das geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="708d8-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708d8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="708d8-111">Return value</span></span>

<span data-ttu-id="708d8-112">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="708d8-112">Type: **HRESULT**</span></span>

<span data-ttu-id="708d8-113">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="708d8-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="708d8-114">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="708d8-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="708d8-115">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="708d8-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="708d8-116">Der folgende spezifische Fehler kann von der-Funktion zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="708d8-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="708d8-117">Rückgabe Code</span><span class="sxs-lookup"><span data-stu-id="708d8-117">Return Code</span></span>             | <span data-ttu-id="708d8-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="708d8-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="708d8-119">E \_ Win \_ ungültiges \_ handle</span><span class="sxs-lookup"><span data-stu-id="708d8-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="708d8-120">Das angegebene Handle ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="708d8-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="708d8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="708d8-121">Requirements</span></span>



| <span data-ttu-id="708d8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="708d8-122">Requirement</span></span> | <span data-ttu-id="708d8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="708d8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="708d8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="708d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="708d8-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="708d8-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="708d8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="708d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="708d8-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="708d8-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="708d8-128">Header</span><span class="sxs-lookup"><span data-stu-id="708d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="708d8-129"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="708d8-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="708d8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="708d8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="708d8-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="708d8-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="708d8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="708d8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="708d8-133">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="708d8-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="708d8-134">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="708d8-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="708d8-135">**Mpscanstart**</span><span class="sxs-lookup"><span data-stu-id="708d8-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="708d8-136">**Mpbedrohlich öffnen**</span><span class="sxs-lookup"><span data-stu-id="708d8-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





