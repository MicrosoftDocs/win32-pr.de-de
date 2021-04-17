---
title: Freenetworksoh-Funktion (naputil. h)
description: Gibt eine networksoh-Datenstruktur frei.
ms.assetid: a27d54a0-8b9c-4bf7-909c-1de5db55f429
keywords:
- Freenetworksoh-Funktion NAP
topic_type:
- apiref
api_name:
- FreeNetworkSoH
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ea2b72011332939aa0c814203d0004949c8341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478453"
---
# <a name="freenetworksoh-function"></a><span data-ttu-id="3216a-104">Freenetworksoh-Funktion</span><span class="sxs-lookup"><span data-stu-id="3216a-104">FreeNetworkSoH function</span></span>

> [!Note]  
> <span data-ttu-id="3216a-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3216a-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3216a-106">Die **freenetworksoh** -Funktion gibt eine [**networksoh**](/windows/win32/api/naptypes/ns-naptypes-networksoh) -Datenstruktur frei.</span><span class="sxs-lookup"><span data-stu-id="3216a-106">The **FreeNetworkSoH** function frees a [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3216a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3216a-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeNetworkSoH(
  _In_ NetworkSoH *networkSoh
);
```



## <a name="parameters"></a><span data-ttu-id="3216a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3216a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3216a-109">*Network SoH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3216a-109">*networkSoh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3216a-110">Ein Zeiger auf die Datenstruktur von [**networksoh**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3216a-110">A pointer to the [**NetworkSoH**](/windows/win32/api/naptypes/ns-naptypes-networksoh) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3216a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3216a-111">Remarks</span></span>

<span data-ttu-id="3216a-112">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="3216a-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="3216a-113">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3216a-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="3216a-114">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3216a-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="3216a-115">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3216a-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="3216a-116">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3216a-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="3216a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3216a-117">Requirements</span></span>



| <span data-ttu-id="3216a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3216a-118">Requirement</span></span> | <span data-ttu-id="3216a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3216a-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3216a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3216a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3216a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3216a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3216a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3216a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3216a-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3216a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3216a-124">Header</span><span class="sxs-lookup"><span data-stu-id="3216a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3216a-125"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="3216a-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="3216a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3216a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3216a-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3216a-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





