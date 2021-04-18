---
title: Mpmanagerversionquery-Funktion (mpclient. h)
description: Gibt Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.
ms.assetid: 47DE12BF-D7A4-468B-B0E7-79B5C27E56F5
keywords:
- Mpmanagerversionquery-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerVersionQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a841a83d8ceb828de0a5a9cd80f5f5bdc7f5c914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341409"
---
# <a name="mpmanagerversionquery-function"></a><span data-ttu-id="bb2cc-104">Mpmanagerversionquery-Funktion</span><span class="sxs-lookup"><span data-stu-id="bb2cc-104">MpManagerVersionQuery function</span></span>

<span data-ttu-id="bb2cc-105">Gibt Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers zurück.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-105">Returns version information about various components of the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2cc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb2cc-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerVersionQuery(
  _In_  MPHANDLE        hMpHandle,
  _Out_ PMPVERSION_INFO pVersionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bb2cc-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb2cc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb2cc-108">*hmphandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bb2cc-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2cc-109">Typ: **mphandle**</span><span class="sxs-lookup"><span data-stu-id="bb2cc-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="bb2cc-110">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="bb2cc-111">Dieses Handle wird von der [**mpmanageropen**](mpmanageropen.md) -Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bb2cc-112">*pversioninfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb2cc-112">*pVersionInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb2cc-113">Typ: **pmpversion \_ Info**</span><span class="sxs-lookup"><span data-stu-id="bb2cc-113">Type: **PMPVERSION\_INFO**</span></span>

<span data-ttu-id="bb2cc-114">Zeiger auf eine-Struktur, die Versionsinformationen zu verschiedenen Komponenten des Malware Schutz-Managers enthält.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-114">Pointer to a structure that contains version information about various components of the malware protection manager.</span></span> <span data-ttu-id="bb2cc-115">Siehe [**mpversion \_ Info**](mpversion-info.md).</span><span class="sxs-lookup"><span data-stu-id="bb2cc-115">See [**MPVERSION\_INFO**](mpversion-info.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb2cc-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb2cc-116">Return value</span></span>

<span data-ttu-id="bb2cc-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb2cc-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bb2cc-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-118">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="bb2cc-119">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-119">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="bb2cc-120">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bb2cc-120">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2cc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb2cc-121">Requirements</span></span>



| <span data-ttu-id="bb2cc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb2cc-122">Requirement</span></span> | <span data-ttu-id="bb2cc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bb2cc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2cc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb2cc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bb2cc-125">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb2cc-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="bb2cc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb2cc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bb2cc-127">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb2cc-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb2cc-128">Header</span><span class="sxs-lookup"><span data-stu-id="bb2cc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb2cc-129"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb2cc-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb2cc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bb2cc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb2cc-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb2cc-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2cc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb2cc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2cc-133">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="bb2cc-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="bb2cc-134">**Mpmanageropen**</span><span class="sxs-lookup"><span data-stu-id="bb2cc-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="bb2cc-135">**mpversion- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="bb2cc-135">**MPVERSION\_INFO**</span></span>](mpversion-info.md)
</dt> </dl>

 

 





