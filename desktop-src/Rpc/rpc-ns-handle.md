---
title: RPC_NS_HANDLE (rpcnsi. h)
description: Der RPC \_ -NS-Datentyp \_ definiert ein Name-Service-handle.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518719"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="30042-104">RPC- \_ NS- \_ handle</span><span class="sxs-lookup"><span data-stu-id="30042-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="30042-105">Der RPC- **\_ NS \_** -Datentyp definiert ein Name-Service-handle.</span><span class="sxs-lookup"><span data-stu-id="30042-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="30042-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30042-106">Remarks</span></span>

<span data-ttu-id="30042-107">Ein Name-Dienst-Handle ist eine nicht transparente Variable mit Informationen, die von der RPC-Lauf Zeit Bibliothek verwendet werden, um die folgenden RPC-Daten aus der Name-Service-Datenbank zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="30042-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="30042-108">Server Bindungs Handles</span><span class="sxs-lookup"><span data-stu-id="30042-108">Server-binding handles</span></span>
-   <span data-ttu-id="30042-109">UUIDs von Ressourcen, die von Serverprofil Mitgliedern angeboten werden</span><span class="sxs-lookup"><span data-stu-id="30042-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="30042-110">Gruppenmitglieder</span><span class="sxs-lookup"><span data-stu-id="30042-110">Group members</span></span>

<span data-ttu-id="30042-111">Der Gültigkeitsbereich eines Namensdienst Handles erfolgt über die entsprechende "Done"-Routine.</span><span class="sxs-lookup"><span data-stu-id="30042-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="30042-112">Anwendungen sind verantwortlich für die Parallelitäts Steuerung von Name-Service-Handles über Threads hinweg.</span><span class="sxs-lookup"><span data-stu-id="30042-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="30042-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30042-113">Requirements</span></span>



| <span data-ttu-id="30042-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30042-114">Requirement</span></span> | <span data-ttu-id="30042-115">Wert</span><span class="sxs-lookup"><span data-stu-id="30042-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30042-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30042-116">Minimum supported client</span></span><br/> | <span data-ttu-id="30042-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30042-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="30042-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30042-118">Minimum supported server</span></span><br/> | <span data-ttu-id="30042-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30042-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30042-120">Header</span><span class="sxs-lookup"><span data-stu-id="30042-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="30042-121"><dt>Rpcnsi. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30042-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30042-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30042-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30042-123">**Rpcnsbindingimportbegin**</span><span class="sxs-lookup"><span data-stu-id="30042-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="30042-124">**Rpcnsbindingimportdone**</span><span class="sxs-lookup"><span data-stu-id="30042-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="30042-125">**Rpcnsbindingimportnext**</span><span class="sxs-lookup"><span data-stu-id="30042-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="30042-126">**Rpcnsbindinglookupbegin**</span><span class="sxs-lookup"><span data-stu-id="30042-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="30042-127">**Rpcnsbindinglookupdone**</span><span class="sxs-lookup"><span data-stu-id="30042-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="30042-128">**Rpcnsbindinglookupnext**</span><span class="sxs-lookup"><span data-stu-id="30042-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





