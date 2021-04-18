---
title: Frefixupinfo-Funktion (naputil. h)
description: Gibt eine fixupinfo-Datenstruktur frei.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Funktion "frefixupinfo" NAP
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3abf1fe07557ac786a9f0cb8e8e06a30408f6d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343869"
---
# <a name="freefixupinfo-function"></a><span data-ttu-id="f5704-104">Frefixupinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="f5704-104">FreeFixupInfo function</span></span>

> [!Note]  
> <span data-ttu-id="f5704-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f5704-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f5704-106">Die Funktion " **frefixupinfo** " gibt eine [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Datenstruktur frei.</span><span class="sxs-lookup"><span data-stu-id="f5704-106">The **FreeFixupInfo** function frees a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5704-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5704-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f5704-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5704-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5704-109">*fixupinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5704-109">*fixupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5704-110">Ein Zeiger auf die Datenstruktur " [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) ", die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5704-110">A pointer to the [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5704-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5704-111">Remarks</span></span>

<span data-ttu-id="f5704-112">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="f5704-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="f5704-113">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f5704-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="f5704-114">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f5704-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="f5704-115">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f5704-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="f5704-116">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="f5704-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5704-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5704-117">Requirements</span></span>



| <span data-ttu-id="f5704-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5704-118">Requirement</span></span> | <span data-ttu-id="f5704-119">Wert</span><span class="sxs-lookup"><span data-stu-id="f5704-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f5704-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f5704-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5704-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5704-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f5704-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f5704-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5704-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f5704-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f5704-124">Header</span><span class="sxs-lookup"><span data-stu-id="f5704-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5704-125"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5704-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="f5704-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f5704-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5704-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5704-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5704-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5704-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5704-129">**Zuordnung von "Zuweisung"**</span><span class="sxs-lookup"><span data-stu-id="f5704-129">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
</dt> </dl>

 

 





