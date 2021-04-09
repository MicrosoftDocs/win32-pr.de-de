---
title: "\"Zuweisung\"-Funktion (\"naputil. h\")"
description: Weist Arbeitsspeicher für eine fixupinfo-Struktur der angegebenen Größe zu.
ms.assetid: e0b66a08-9714-4451-a22d-3822153c6a36
keywords:
- "' Zuweisung ' der Funktion ' ' der Funktion ' NAP '"
topic_type:
- apiref
api_name:
- AllocFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dffda7e5e44302173ac06e460414455eb19c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858700"
---
# <a name="allocfixupinfo-function"></a><span data-ttu-id="f9c37-104">' Zuweisung '-Funktion</span><span class="sxs-lookup"><span data-stu-id="f9c37-104">AllocFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="f9c37-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f9c37-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f9c37-106">Die Funktion " **belegcfixupinfo** " weist Speicher für eine [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur der angegebenen Größe zu.</span><span class="sxs-lookup"><span data-stu-id="f9c37-106">The **AllocFixupInfo** function allocates memory for a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure of the specified size.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c37-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9c37-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocFixupInfo(
  _Inout_ FixupInfo **fixupInfo,
  _In_    UINT16    countResultCodes
);
```



## <a name="parameters"></a><span data-ttu-id="f9c37-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9c37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c37-109">*fixupinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f9c37-109">*fixupInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c37-110">Ein Zeiger auf die Adresse einer neu zugewiesenen [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f9c37-110">A pointer to the address of a newly allocated [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9c37-111">*countrytresultcodes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9c37-111">*countResultCodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c37-112">Die Anzahl der der *fixupinfo* zuzuordnenden Ergebnis Codes.</span><span class="sxs-lookup"><span data-stu-id="f9c37-112">The number of result codes to allocate to *fixupInfo*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c37-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9c37-113">Return value</span></span>



| <span data-ttu-id="f9c37-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f9c37-114">Return code</span></span>                                                                                   | <span data-ttu-id="f9c37-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9c37-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9c37-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9c37-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f9c37-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f9c37-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="f9c37-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="f9c37-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f9c37-119">Ein ungültiges Argument wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="f9c37-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f9c37-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="f9c37-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f9c37-121">Das System verfügt nicht über den virtuellen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="f9c37-121">The system is out of virtual memory.</span></span> <span data-ttu-id="f9c37-122">Bei diesem Vorgang ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f9c37-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9c37-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9c37-123">Remarks</span></span>

<span data-ttu-id="f9c37-124">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="f9c37-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="f9c37-125">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f9c37-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="f9c37-126">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f9c37-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="f9c37-127">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f9c37-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="f9c37-128">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f9c37-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c37-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9c37-129">Requirements</span></span>



| <span data-ttu-id="f9c37-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9c37-130">Requirement</span></span> | <span data-ttu-id="f9c37-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f9c37-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c37-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9c37-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c37-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9c37-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f9c37-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9c37-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c37-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9c37-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f9c37-136">Header</span><span class="sxs-lookup"><span data-stu-id="f9c37-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c37-137"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9c37-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f9c37-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c37-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c37-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c37-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9c37-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9c37-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c37-141">**"Freifixupinfo"**</span><span class="sxs-lookup"><span data-stu-id="f9c37-141">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
</dt> </dl>

 

 





