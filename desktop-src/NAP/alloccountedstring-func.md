---
title: "\"Zuweisung\"-Funktion (\"naputil. h\")"
description: Ordnet Speicher für eine NULL-terminierte Zeichenfolge zu und gibt Sie in einer rattedstring-Struktur zurück.
ms.assetid: 6dd503bf-8853-499b-adcd-54de696f01d6
keywords:
- Zuweisung der "Zuweisung"-Funktion
topic_type:
- apiref
api_name:
- AllocCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab2980ce5eefdd7743907bdcc947cdce1c74823
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340766"
---
# <a name="alloccountedstring-function"></a><span data-ttu-id="c992c-104">' Zuweisung '-Funktion</span><span class="sxs-lookup"><span data-stu-id="c992c-104">AllocCountedString function</span></span>

> [!Note]  
> <span data-ttu-id="c992c-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c992c-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c992c-106">Die " **belegczähltedstring** "-Funktion ordnet Arbeitsspeicher für eine auf NULL endenden Zeichenfolge zu und gibt Sie in einer " [**count String**](/windows/win32/api/naptypes/ns-naptypes-countedstring) "-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="c992c-106">The **AllocCountedString** function allocates memory for a null-terminated string and returns it in a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="c992c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c992c-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocCountedString(
  _Inout_       CountedString **countedString,
  _In_    const WCHAR         *string
);
```



## <a name="parameters"></a><span data-ttu-id="c992c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c992c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c992c-109">" *zählzeichen Folge* \[ " in, out\]</span><span class="sxs-lookup"><span data-stu-id="c992c-109">*countedString* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c992c-110">Ein Zeiger auf die Adresse einer neu zugeordneten [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="c992c-110">A pointer to the address of a newly allocated [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c992c-111">*Zeichenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c992c-111">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c992c-112">Ein Zeiger auf die auf NULL endende Zeichenfolge, die in der " *zähltedstring*" zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c992c-112">A pointer to the null-terminated string that is to be returned in *countedString*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c992c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c992c-113">Return value</span></span>



| <span data-ttu-id="c992c-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c992c-114">Return code</span></span>                                                                                   | <span data-ttu-id="c992c-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c992c-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c992c-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c992c-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c992c-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c992c-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="c992c-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c992c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c992c-119">Ein ungültiges Argument wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="c992c-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c992c-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c992c-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c992c-121">Das System verfügt nicht über den virtuellen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c992c-121">The system is out of virtual memory.</span></span> <span data-ttu-id="c992c-122">Bei diesem Vorgang ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c992c-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c992c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c992c-123">Remarks</span></span>

<span data-ttu-id="c992c-124">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="c992c-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="c992c-125">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c992c-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="c992c-126">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c992c-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="c992c-127">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c992c-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="c992c-128">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c992c-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="c992c-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c992c-129">Requirements</span></span>



| <span data-ttu-id="c992c-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c992c-130">Requirement</span></span> | <span data-ttu-id="c992c-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c992c-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c992c-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c992c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c992c-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c992c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c992c-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c992c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c992c-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c992c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c992c-136">Header</span><span class="sxs-lookup"><span data-stu-id="c992c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c992c-137"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="c992c-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="c992c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="c992c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c992c-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c992c-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c992c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c992c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c992c-141">**Freizähltedstring**</span><span class="sxs-lookup"><span data-stu-id="c992c-141">**FreeCountedString**</span></span>](freecountedstring-func.md)
</dt> </dl>

 

 





