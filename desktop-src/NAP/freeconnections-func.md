---
title: Freeconnections-Funktion (naputil. h)
description: Gibt eine Verbindungsdaten Struktur frei.
ms.assetid: bb339d71-f8e3-48d8-834d-8b957e0cb5ec
keywords:
- Freeconnections-Funktion NAP
topic_type:
- apiref
api_name:
- FreeConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f840d02572af3e6382a06a1873573fc7a30420e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340397"
---
# <a name="freeconnections-function"></a><span data-ttu-id="de28e-104">Freeconnections-Funktion</span><span class="sxs-lookup"><span data-stu-id="de28e-104">FreeConnections function</span></span>

> [!Note]  
> <span data-ttu-id="de28e-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de28e-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="de28e-106">Die **freeconnections** -Funktion gibt eine [**Verbindungs**](connections-struct.md) Datenstruktur frei.</span><span class="sxs-lookup"><span data-stu-id="de28e-106">The **FreeConnections** function frees a [**Connections**](connections-struct.md) data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="de28e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de28e-107">Syntax</span></span>


```C++
NAPAPI VOID WINAPI FreeConnections(
  _In_ Connections *connections
);
```



## <a name="parameters"></a><span data-ttu-id="de28e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de28e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de28e-109">*Verbindungen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de28e-109">*connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de28e-110">Ein Zeiger auf die frei verfügbaren [**Verbindungs**](connections-struct.md) Struktur.</span><span class="sxs-lookup"><span data-stu-id="de28e-110">A pointer to the [**Connections**](connections-struct.md) structure to free.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de28e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de28e-111">Remarks</span></span>

<span data-ttu-id="de28e-112">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="de28e-112">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="de28e-113">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="de28e-113">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="de28e-114">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="de28e-114">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="de28e-115">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="de28e-115">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="de28e-116">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="de28e-116">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="de28e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de28e-117">Requirements</span></span>



| <span data-ttu-id="de28e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de28e-118">Requirement</span></span> | <span data-ttu-id="de28e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="de28e-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="de28e-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de28e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="de28e-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de28e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="de28e-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de28e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="de28e-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de28e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="de28e-124">Header</span><span class="sxs-lookup"><span data-stu-id="de28e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="de28e-125"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="de28e-125"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="de28e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="de28e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de28e-127"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de28e-127"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de28e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de28e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de28e-129">**Zuordnung von Verbindungen**</span><span class="sxs-lookup"><span data-stu-id="de28e-129">**AllocConnections**</span></span>](allocconnections-func.md)
</dt> </dl>

 

 





