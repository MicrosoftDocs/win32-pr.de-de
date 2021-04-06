---
title: Die Funktion "Zuweisung" ("naputil. h")
description: Weist Arbeitsspeicher für eine angegebene Anzahl von Verbindungsstrukturen zu.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- Funktion "Zuweisung von Verbindungen"
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e29521d2fea6eec3765a3a34210b896f1baa4db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743897"
---
# <a name="allocconnections-function"></a><span data-ttu-id="be112-104">Funktion "Zuweisung"</span><span class="sxs-lookup"><span data-stu-id="be112-104">AllocConnections function</span></span>

> [!Note]  
> <span data-ttu-id="be112-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="be112-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="be112-106">Die Funktion " **belegcconnections** " weist Arbeitsspeicher für eine angegebene Anzahl von [**Verbindungs**](connections-struct.md) Strukturen zu.</span><span class="sxs-lookup"><span data-stu-id="be112-106">The **AllocConnections** function allocates memory for a specified number of [**Connections**](connections-struct.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="be112-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be112-107">Syntax</span></span>


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a><span data-ttu-id="be112-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be112-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be112-109">*Verbindungen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="be112-109">*connections* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be112-110">Ein Zeiger auf ein Array neu zugewiesener [**Verbindungs**](connections-struct.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="be112-110">A pointer to an array of newly allocated [**Connections**](connections-struct.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="be112-111">*connectionsanzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="be112-111">*connectionsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be112-112">Die Anzahl der Strukturen, die *Verbindungen* zuzuordnen sind.</span><span class="sxs-lookup"><span data-stu-id="be112-112">The number of structures to allocate to *connections*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be112-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be112-113">Return value</span></span>



| <span data-ttu-id="be112-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="be112-114">Return code</span></span>                                                                                   | <span data-ttu-id="be112-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be112-115">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="be112-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be112-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="be112-117">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="be112-117">The operation has completed successfully.</span></span><br/>                       |
| <dl> <span data-ttu-id="be112-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="be112-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="be112-119">Ein ungültiges Argument wurde übergeben.</span><span class="sxs-lookup"><span data-stu-id="be112-119">An invalid argument was passed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="be112-120"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="be112-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="be112-121">Das System verfügt nicht über den virtuellen Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="be112-121">The system is out of virtual memory.</span></span> <span data-ttu-id="be112-122">Bei diesem Vorgang ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="be112-122">This operation has failed.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="be112-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be112-123">Remarks</span></span>

<span data-ttu-id="be112-124">Alle vom NAP-System unterstützten com-Schnittstellen verwenden Standard-com-Speicher Verwaltungsregeln und die com-Speicher Belegungs Funktion (**cotaskmembelegc** und **CoTaskMemFree**):</span><span class="sxs-lookup"><span data-stu-id="be112-124">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocators (**CoTaskMemAlloc** and **CoTaskMemFree**):</span></span>

-   <span data-ttu-id="be112-125">**In** -Parameter werden vom Aufrufer zugeordnet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="be112-125">**In** parameters are allocated and freed by the caller.</span></span>
-   <span data-ttu-id="be112-126">Out-Parameter werden vom **aufgerufenen** zugeordnet und vom Aufrufer mithilfe von **cotaskmem** freigegeben.</span><span class="sxs-lookup"><span data-stu-id="be112-126">**Out** parameters are allocated by the callee and freed by the caller using **CoTaskMem**.</span></span>
-   <span data-ttu-id="be112-127">**In/out-** Parameter werden vom Aufrufer zugeordnet, vom aufgerufenen freigegeben und neu zugeordnet und schließlich mit **cotaskmem** vom Aufrufer freigegeben.</span><span class="sxs-lookup"><span data-stu-id="be112-127">**In/out** parameters are allocated by the caller, freed and reallocated by the callee, and ultimately freed by the caller, using **CoTaskMem**.</span></span>

<span data-ttu-id="be112-128">Alle NAP-Funktionen zum Freigeben von Speicher freigeben auch alle eingebetteten Zeiger.</span><span class="sxs-lookup"><span data-stu-id="be112-128">All NAP functions for freeing memory also free all embedded pointers.</span></span>

## <a name="requirements"></a><span data-ttu-id="be112-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be112-129">Requirements</span></span>



| <span data-ttu-id="be112-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be112-130">Requirement</span></span> | <span data-ttu-id="be112-131">Wert</span><span class="sxs-lookup"><span data-stu-id="be112-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="be112-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="be112-132">Minimum supported client</span></span><br/> | <span data-ttu-id="be112-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be112-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be112-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="be112-134">Minimum supported server</span></span><br/> | <span data-ttu-id="be112-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="be112-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="be112-136">Header</span><span class="sxs-lookup"><span data-stu-id="be112-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="be112-137"><dt>Naputil. h</dt></span><span class="sxs-lookup"><span data-stu-id="be112-137"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="be112-138">DLL</span><span class="sxs-lookup"><span data-stu-id="be112-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be112-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be112-139"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be112-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be112-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be112-141">**Freeconnections**</span><span class="sxs-lookup"><span data-stu-id="be112-141">**FreeConnections**</span></span>](freeconnections-func.md)
</dt> </dl>

 

 





