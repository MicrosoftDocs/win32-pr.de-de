---
title: Mpmanageropen-Funktion (mpclient. h)
description: Stellt eine Verbindung mit dem Malware Schutz-Manager auf dem lokalen Computer her.
ms.assetid: 40513A74-AFCC-4E22-9B78-D46FEB575A00
keywords:
- Mpmanageropen-Funktion Legacy Funktionen der Windows-Umgebung
topic_type:
- apiref
api_name:
- MpManagerOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af432cc7d91530fd3d37176592f7f457b31b6314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743184"
---
# <a name="mpmanageropen-function"></a><span data-ttu-id="21b9d-104">Mpmanageropen-Funktion</span><span class="sxs-lookup"><span data-stu-id="21b9d-104">MpManagerOpen function</span></span>

<span data-ttu-id="21b9d-105">Stellt eine Verbindung mit dem Malware Schutz-Manager auf dem lokalen Computer her.</span><span class="sxs-lookup"><span data-stu-id="21b9d-105">Establishes a connection to the malware protection manager on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b9d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="21b9d-106">Syntax</span></span>


```C++
HRESULT WINAPI MpManagerOpen(
  _In_  DWORD     dwReserved,
  _Out_ PMPHANDLE phMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="21b9d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="21b9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21b9d-108">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21b9d-108">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21b9d-109">Typ: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="21b9d-109">Type: **DWORD**</span></span>

<span data-ttu-id="21b9d-110">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="21b9d-110">Reserved for future use.</span></span> <span data-ttu-id="21b9d-111">Muss auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="21b9d-111">Must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="21b9d-112">*phmphandle* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21b9d-112">*phMpHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21b9d-113">Typ: **pmphandle**</span><span class="sxs-lookup"><span data-stu-id="21b9d-113">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="21b9d-114">Handle für die Malware Protection Manager-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="21b9d-114">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="21b9d-115">Dieses Handle muss mit der [**mplenker close**](mphandleclose.md) -Funktion geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="21b9d-115">This handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21b9d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21b9d-116">Return value</span></span>

<span data-ttu-id="21b9d-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="21b9d-117">Type: **HRESULT**</span></span>

<span data-ttu-id="21b9d-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21b9d-118">If the function succeeds the return value is **S\_OK**.</span></span> <span data-ttu-id="21b9d-119">Dieser Funktions Aufrufvorgang ist garantiert auch dann erfolgreich, wenn kein antischadsoftwaredienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21b9d-119">This function call is guaranteed to succeed even if an AntiMalware service is not running.</span></span>

<span data-ttu-id="21b9d-120">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerhafter **HRESULT** -Code.</span><span class="sxs-lookup"><span data-stu-id="21b9d-120">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="21b9d-121">Der Aufrufer kann die [**mperrormessageformat**](mperrormessageformat.md) -Funktion verwenden, um eine generische Beschreibung der Fehlermeldung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="21b9d-121">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="21b9d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21b9d-122">Requirements</span></span>



| <span data-ttu-id="21b9d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21b9d-123">Requirement</span></span> | <span data-ttu-id="21b9d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="21b9d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="21b9d-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="21b9d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="21b9d-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21b9d-126">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="21b9d-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="21b9d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="21b9d-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="21b9d-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="21b9d-129">Header</span><span class="sxs-lookup"><span data-stu-id="21b9d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="21b9d-130"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="21b9d-130"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="21b9d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="21b9d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21b9d-132"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21b9d-132"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21b9d-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21b9d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21b9d-134">**Mperrormessageformat**</span><span class="sxs-lookup"><span data-stu-id="21b9d-134">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="21b9d-135">**Mplenker schließen**</span><span class="sxs-lookup"><span data-stu-id="21b9d-135">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> </dl>

 

 





