---
title: Freesystemhealthagentstate-Funktion (naputil. h)
description: Gibt eine systemhealthagentstate-Datenstruktur frei.
ms.assetid: e9bfa8ee-c335-416e-94cf-28646709d419
keywords:
- Freesystemhealthagentstate-Funktion NAP
topic_type:
- apiref
api_name:
- FreeSystemHealthAgentState
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce59135de1c8f47d84a07f01dbb5f2bbe697f9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103302"
---
# <a name="freesystemhealthagentstate-function"></a><span data-ttu-id="19ef6-104">Freesystemhealthagentstate-Funktion</span><span class="sxs-lookup"><span data-stu-id="19ef6-104">FreeSystemHealthAgentState function</span></span>

> [!Note]  
> <span data-ttu-id="19ef6-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19ef6-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19ef6-106">Die **freesystemhealthagentstate** -Funktion gibt eine [**systemhealthagentstate**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) -Datenstruktur frei.</span><span class="sxs-lookup"><span data-stu-id="19ef6-106">The **FreeSystemHealthAgentState** function frees a [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="19ef6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ef6-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeSystemHealthAgentState(
  _In_ SystemHealthAgentState *state
);
```



## <a name="parameters"></a><span data-ttu-id="19ef6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ef6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19ef6-109">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="19ef6-109">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19ef6-110">Ein Zeiger auf die Datenstruktur " [**systemhealthagentstate**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) ", die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="19ef6-110">A pointer to the [**SystemHealthAgentState**](/windows/win32/api/naptypes/ns-naptypes-systemhealthagentstate) data structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19ef6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19ef6-111">Remarks</span></span>

<span data-ttu-id="19ef6-112">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="19ef6-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="19ef6-113">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="19ef6-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="19ef6-114">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="19ef6-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="19ef6-115">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="19ef6-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="19ef6-116">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="19ef6-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="19ef6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19ef6-117">Requirements</span></span>



| <span data-ttu-id="19ef6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19ef6-118">Requirement</span></span> | <span data-ttu-id="19ef6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="19ef6-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="19ef6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19ef6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19ef6-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19ef6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="19ef6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19ef6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19ef6-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19ef6-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="19ef6-124">Header</span><span class="sxs-lookup"><span data-stu-id="19ef6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="19ef6-125"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="19ef6-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="19ef6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="19ef6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19ef6-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19ef6-127"><dt>Qutil.dll</dt></span></span> </dl> |



 

 





