---
title: RPC_BINDING_HANDLE (rpcdce. h)
description: Der Datentyp des RPC- \_ Bindungs Handles deklariert ein Bindungs handle, das Informationen enthält, die von der RPC-Lauf Zeit Bibliothek für den Zugriff auf Bindungs Informationen verwendet werden.
ms.assetid: 3e07d9e9-04d8-4f94-8104-cd0ee89a9407
keywords:
- RPC_BINDING_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e37d14bc5186f05815c10f538b0c90bdddd353
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743792"
---
# <a name="rpc_binding_handle"></a><span data-ttu-id="15c42-104">RPC- \_ Bindungs \_ handle</span><span class="sxs-lookup"><span data-stu-id="15c42-104">RPC\_BINDING\_HANDLE</span></span>

<span data-ttu-id="15c42-105">Der Datentyp des **RPC- \_ Bindungs Handles** deklariert ein Bindungs handle, das Informationen enthält, die von der RPC-Lauf Zeit Bibliothek für den Zugriff auf Bindungs Informationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15c42-105">The **RPC\_BINDING HANDLE** data type declares a binding handle containing information that the RPC run-time library uses to access binding information.</span></span>


```C++
typedef I_RPC_HANDLE RPC_BINDING_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="15c42-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15c42-106">Remarks</span></span>

<span data-ttu-id="15c42-107">Die-Lauf Zeit Bibliothek verwendet Bindungs Informationen, um eine Client/Server-Beziehung einzurichten, die die Ausführung von Remote Prozedur aufrufen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="15c42-107">The run-time library uses binding information to establish a client-server relationship that allows the execution of remote procedure calls.</span></span> <span data-ttu-id="15c42-108">Basierend auf dem Kontext, in dem ein Bindungs Handle erstellt wird, wird es als Server Bindungs handle oder Client Bindungs handle angesehen.</span><span class="sxs-lookup"><span data-stu-id="15c42-108">Based on the context in which a binding handle is created, it is considered a server-binding handle or a client-binding handle.</span></span>

<span data-ttu-id="15c42-109">Ein Server Bindungs Handle enthält die Informationen, die für einen Client erforderlich sind, um eine Beziehung zu einem bestimmten Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="15c42-109">A server-binding handle contains the information necessary for a client to establish a relationship with a specific server.</span></span> <span data-ttu-id="15c42-110">Eine beliebige Anzahl von RPC-API-Lauf Zeit Routinen gibt ein Server Bindungs Handle zurück, das zum Ausführen eines Remote Prozedur Aufrufs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="15c42-110">Any number of RPC API run-time routines return a server-binding handle that can be used for making a remote procedure call.</span></span>

<span data-ttu-id="15c42-111">Ein Client Bindungs Handle kann nicht verwendet werden, um einen Remote Prozedur aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="15c42-111">A client-binding handle cannot be used to make a remote procedure call.</span></span> <span data-ttu-id="15c42-112">Die RPC-Lauf Zeit Bibliothek erstellt und stellt ein Client Bindungs Handle für eine aufgerufene Server Prozedur (auch als Server-Manager-Routine bezeichnet) als Parameter für den RPC- \_ Bindungs \_ handle bereit.</span><span class="sxs-lookup"><span data-stu-id="15c42-112">The RPC run-time library creates and provides a client-binding handle to a called-server procedure (also called a server-manager routine) as the RPC\_BINDING\_HANDLE parameter.</span></span> <span data-ttu-id="15c42-113">Das Client Bindungs Handle enthält Informationen zum aufrufenden Client.</span><span class="sxs-lookup"><span data-stu-id="15c42-113">The client-binding handle contains information about the calling client.</span></span>

<span data-ttu-id="15c42-114">Die Funktionen **RpcBinding \** _ und _*rpcnsbinding \*\*_ geben den Statuscode RPC \_ S \_ falsch \_ an, \_ \_ Wenn eine Anwendung den falschen bindungshandlertyp bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="15c42-114">The **RpcBinding\** _ and _*RpcNsBinding\*\*_ functions return the status code RPC\_S\_WRONG\_KIND\_OF\_BINDING when an application provides the incorrect binding-handle type.</span></span>

<span data-ttu-id="15c42-115">Eine Anwendung kann ein einzelnes Bindungs Handle für mehrere Ausführungs Threads freigeben.</span><span class="sxs-lookup"><span data-stu-id="15c42-115">An application can share a single binding handle across multiple threads of execution.</span></span> <span data-ttu-id="15c42-116">Die RPC-Lauf Zeit Bibliothek verwaltet gleichzeitige Remote Prozedur Aufrufe, bei denen ein einzelnes Bindungs Handle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="15c42-116">The RPC run-time library manages concurrent remote procedure calls that use a single binding handle.</span></span> <span data-ttu-id="15c42-117">Die Anwendung ist jedoch für die Bindung der Parallelitäts Steuerung für Vorgänge zuständig, die ein Bindungs handle ändern.</span><span class="sxs-lookup"><span data-stu-id="15c42-117">However, the application is responsible for binding handle concurrency control for operations that modify a binding handle.</span></span> <span data-ttu-id="15c42-118">Diese Vorgänge umfassen die folgenden Routinen:</span><span class="sxs-lookup"><span data-stu-id="15c42-118">These operations include the following routines:</span></span>

-   [<span data-ttu-id="15c42-119">_ *Rpcbindingfree*\*</span><span class="sxs-lookup"><span data-stu-id="15c42-119">_ *RpcBindingFree*\*</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)
-   [<span data-ttu-id="15c42-120">**Rpcbindingreset**</span><span class="sxs-lookup"><span data-stu-id="15c42-120">**RpcBindingReset**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)
-   [<span data-ttu-id="15c42-121">**Rpcbindingsetauthinfo**</span><span class="sxs-lookup"><span data-stu-id="15c42-121">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
-   [<span data-ttu-id="15c42-122">**Rpcbindingsetobject**</span><span class="sxs-lookup"><span data-stu-id="15c42-122">**RpcBindingSetObject**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)

<span data-ttu-id="15c42-123">Wenn eine Anwendung z. b. ein Bindungs Handle für zwei Ausführungs Threads nutzt und den Bindungs handle-Endpunkt in einem der Threads durch Aufrufen von [**rpcbindingreset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)zurücksetzt, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="15c42-123">For example, if an application shares a binding handle across two threads of execution and resets the binding-handle endpoint in one of the threads by calling [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset), the results are undefined.</span></span> <span data-ttu-id="15c42-124">Das Bindungs Handle im anderen Thread kann ebenfalls zurückgesetzt werden, oder der Vorgang kann fehlschlagen, oder der Prozess stürzt ab.</span><span class="sxs-lookup"><span data-stu-id="15c42-124">The binding handle on the other thread may also be reset, or the operation may fail, or the process may crash.</span></span> <span data-ttu-id="15c42-125">Ein häufiger Fehler besteht darin, ein Bindungs Handle freizugeben, während ein-Vorgang ausgeführt wird. Dies stürzt normalerweise den aufrufenden Prozess ab.</span><span class="sxs-lookup"><span data-stu-id="15c42-125">A common error is freeing a binding handle while a call on it is in progress; this usually crashes the calling process.</span></span>

<span data-ttu-id="15c42-126">Wenn Sie keine Parallelität möchten, können Sie eine Anwendung so entwerfen, dass eine Kopie eines Bindungs Handles durch Aufrufen von [**rpcbindingcopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="15c42-126">If you do not want concurrency, you can design an application to create a copy of a binding handle by calling [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy).</span></span> <span data-ttu-id="15c42-127">In diesem Fall hat ein Vorgang für das erste Bindungs Handle keine Auswirkung auf das zweite Bindungs handle.</span><span class="sxs-lookup"><span data-stu-id="15c42-127">In this case, an operation to the first binding handle has no effect on the second binding handle.</span></span>

<span data-ttu-id="15c42-128">Routinen, die ein Bindungs Handle als Parameter erfordern, zeigen den Datentyp **RPC- \_ Bindungs \_ handle** an.</span><span class="sxs-lookup"><span data-stu-id="15c42-128">Routines requiring a binding handle as a parameter show a data type of **RPC\_BINDING\_HANDLE**.</span></span> <span data-ttu-id="15c42-129">Bindungs handle-Parameter werden als Wert übermittelt.</span><span class="sxs-lookup"><span data-stu-id="15c42-129">Binding-handle parameters are passed by value.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c42-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15c42-130">Requirements</span></span>



| <span data-ttu-id="15c42-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15c42-131">Requirement</span></span> | <span data-ttu-id="15c42-132">Wert</span><span class="sxs-lookup"><span data-stu-id="15c42-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c42-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15c42-133">Minimum supported client</span></span><br/> | <span data-ttu-id="15c42-134">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15c42-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="15c42-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15c42-135">Minimum supported server</span></span><br/> | <span data-ttu-id="15c42-136">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15c42-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15c42-137">Header</span><span class="sxs-lookup"><span data-stu-id="15c42-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="15c42-138"><dt>Rpcdce. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15c42-138"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



 

 





