---
description: Registriert den Anbieter und initialisiert die Indikatorensätze.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Counterinitialize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959769"
---
# <a name="counterinitialize-function"></a><span data-ttu-id="18783-103">Counterinitialize-Funktion</span><span class="sxs-lookup"><span data-stu-id="18783-103">CounterInitialize function</span></span>

<span data-ttu-id="18783-104">Registriert den Anbieter und initialisiert die Indikatorensätze.</span><span class="sxs-lookup"><span data-stu-id="18783-104">Registers the provider and initializes the counter sets.</span></span>

## <a name="syntax"></a><span data-ttu-id="18783-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="18783-105">Syntax</span></span>


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a><span data-ttu-id="18783-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="18783-106">Parameters</span></span>

<span data-ttu-id="18783-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="18783-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18783-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18783-108">Return value</span></span>

<span data-ttu-id="18783-109">Gibt \_ bei Erfolg einen Erfolg des Fehlers zurück, andernfalls einen Standard-Win32-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="18783-109">Returns ERROR\_SUCCESS on success; otherwise, a standard Win32 error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="18783-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="18783-110">Remarks</span></span>

<span data-ttu-id="18783-111">Der Anbieter ruft diese Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="18783-111">Your provider calls this function.</span></span> <span data-ttu-id="18783-112">Die Funktion enthält Aufrufe der Funktion [**perfstartprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) und der Funktion [**perfsetcountersetinfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="18783-112">The function includes calls to the [**PerfStartProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) function and the [**PerfSetCounterSetInfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) function.</span></span>

<span data-ttu-id="18783-113">Das [**ctrpp**](ctrpp.md) -Tool generiert diese Inline Funktion, wenn Sie das **-o-** Argument angeben.</span><span class="sxs-lookup"><span data-stu-id="18783-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="18783-114">Der Name der Funktion enthält eine *Präfix* Zeichenfolge, wenn Sie das **-prefix-** Argument angeben.</span><span class="sxs-lookup"><span data-stu-id="18783-114">The function's name include a *prefix* string if you specify the **-prefix** argument.</span></span>

<span data-ttu-id="18783-115">Wenn Sie die Argumente **-memoryroutinen** oder **-notificationcallback** angeben (oder das **Rückruf** Attribut für das [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) -Element angeben), ändert sich die **counterinitialize** -Signatur wie folgt:</span><span class="sxs-lookup"><span data-stu-id="18783-115">If you specify the **-MemoryRoutines** or **-NotificationCallback** arguments (or specify the **callback** attribute for the [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) element), the **CounterInitialize** signature changes to the following:</span></span>

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

<span data-ttu-id="18783-116">Erläuterungen:</span><span class="sxs-lookup"><span data-stu-id="18783-116">where,</span></span>

<dl> <dt>

<span data-ttu-id="18783-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>Notificationcallback</span><span class="sxs-lookup"><span data-stu-id="18783-117"><span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback</span></span>
</dt> <dd>

<span data-ttu-id="18783-118">Der Name der [*controlcallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) -Rückruffunktion, die Sie implementieren, um Benachrichtigungen über Consumer-Anforderungen zu empfangen (z. b. Anforderungen zum Hinzufügen oder Entfernen von Indikatoren aus der Abfrage).</span><span class="sxs-lookup"><span data-stu-id="18783-118">The name of your [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) callback function that you implement to receive notification of consumer requests (for example, requests to add or remove counters from the query).</span></span> <span data-ttu-id="18783-119">Legen Sie diesen Wert auf **null** fest, wenn Sie die *controlcallback* -Rückruffunktion nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="18783-119">Set to **NULL** if you do not implement the *ControlCallback* callback function.</span></span>

</dd> <dt>

<span data-ttu-id="18783-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>Memoryzuweisung-Funktion</span><span class="sxs-lookup"><span data-stu-id="18783-120"><span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction</span></span>
</dt> <dd>

<span data-ttu-id="18783-121">Der Name der [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) -Rückruffunktion, die von Perflib zum Zuordnen von Arbeitsspeicher aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="18783-121">The name of your [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) callback function that PERFLIB calls to allocate memory.</span></span> <span data-ttu-id="18783-122">Legen Sie diesen Wert auf **null** fest, wenn Sie das **-memoryroutinen-** Argument nicht angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="18783-122">Set to **NULL** if you did not specify the **-MemoryRoutines** argument.</span></span>

</dd> <dt>

<span data-ttu-id="18783-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>Memoryfrefunction</span><span class="sxs-lookup"><span data-stu-id="18783-123"><span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction</span></span>
</dt> <dd>

<span data-ttu-id="18783-124">Der Name der [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) -Rückruffunktion, die von Perflib aufgerufen wird, um den Speicher freizugeben, der mit der Funktion " [*belegcatememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) " belegt wird</span><span class="sxs-lookup"><span data-stu-id="18783-124">The name of your [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) callback function that PERFLIB calls to free the memory allocated using the [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) function.</span></span> <span data-ttu-id="18783-125">Auf **null** festgelegt, wenn *memoryzucationfunction* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="18783-125">Set to **NULL** if *MemoryAllocationFunction* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="18783-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>Memoryfunctioncontext</span><span class="sxs-lookup"><span data-stu-id="18783-126"><span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext</span></span>
</dt> <dd>

<span data-ttu-id="18783-127">Kontextinformationen, die an die Speicher Belegung und die freien Routinen übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="18783-127">Context information to pass to your memory allocation and free routines.</span></span> <span data-ttu-id="18783-128">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="18783-128">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18783-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18783-129">Requirements</span></span>



| <span data-ttu-id="18783-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18783-130">Requirement</span></span> | <span data-ttu-id="18783-131">Wert</span><span class="sxs-lookup"><span data-stu-id="18783-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="18783-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18783-132">Minimum supported client</span></span><br/> | <span data-ttu-id="18783-133">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18783-133">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="18783-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18783-134">Minimum supported server</span></span><br/> | <span data-ttu-id="18783-135">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18783-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

