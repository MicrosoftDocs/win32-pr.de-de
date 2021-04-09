---
description: Gibt an, ob der \_ \_ try-Block eines Beendigungs Handlers normal beendet wurde. Die-Funktion kann nur innerhalb des letzten \_ \_ Blocks eines Beendigungs Handlers aufgerufen werden.
ms.assetid: 0ddaef1f-03f0-45fc-9c5e-8d6a26a73245
title: Abnormalbeendigung-Makro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AbnormalTermination
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7c4869f36d8ba70c8dcd8ca526949d489f455e8c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958534"
---
# <a name="abnormaltermination-macro"></a><span data-ttu-id="929a5-104">Abnormalbeendigung-Makro</span><span class="sxs-lookup"><span data-stu-id="929a5-104">AbnormalTermination macro</span></span>

<span data-ttu-id="929a5-105">Gibt an, ob der **\_ \_ try** -Block eines Beendigungs Handlers normal beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="929a5-105">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span> <span data-ttu-id="929a5-106">Die-Funktion kann nur innerhalb des **\_ \_ letzten Blocks eines** Beendigungs Handlers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="929a5-106">The function can be called only from within the **\_\_finally** block of a termination handler.</span></span>

> [!Note]  
> <span data-ttu-id="929a5-107">Der Microsoft C/C++-Optimierungs Compiler interpretiert diese Funktion als Schlüsselwort, und die Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler.</span><span class="sxs-lookup"><span data-stu-id="929a5-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="929a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="929a5-108">Syntax</span></span>


```C++
BOOL AbnormalTermination(void);
```



## <a name="parameters"></a><span data-ttu-id="929a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="929a5-109">Parameters</span></span>

<span data-ttu-id="929a5-110">Dieses Makro weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="929a5-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="929a5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="929a5-111">Return value</span></span>

<span data-ttu-id="929a5-112">Wenn der **\_ \_ try** -Block nicht ordnungsgemäß beendet wurde, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="929a5-112">If the **\_\_try** block terminated abnormally, the return value is nonzero.</span></span>

<span data-ttu-id="929a5-113">Wenn der **\_ \_ try** -Block normal beendet wurde, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="929a5-113">If the **\_\_try** block terminated normally, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="929a5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="929a5-114">Remarks</span></span>

<span data-ttu-id="929a5-115">Der **\_ \_ try** -Block wird nur dann normal beendet, wenn die Ausführung den Block sequenziell verlässt, nachdem die letzte Anweisung im-Block ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="929a5-115">The **\_\_try** block terminates normally only if execution leaves the block sequentially after executing the last statement in the block.</span></span> <span data-ttu-id="929a5-116">Anweisungen (z. b. **Return**, **goto**, **Continue** oder **break**), die bewirken, dass die Ausführung den **\_ \_ try** -Block verlässt, führen zu einem nicht ordnungsgemäßen Beenden des Blocks.</span><span class="sxs-lookup"><span data-stu-id="929a5-116">Statements (such as **return**, **goto**, **continue**, or **break**) that cause execution to leave the **\_\_try** block result in abnormal termination of the block.</span></span> <span data-ttu-id="929a5-117">Dies ist auch dann der Fall, wenn eine solche-Anweisung die letzte Anweisung im **\_ \_ try** -Block ist.</span><span class="sxs-lookup"><span data-stu-id="929a5-117">This is the case even if such a statement is the last statement in the **\_\_try** block.</span></span>

<span data-ttu-id="929a5-118">Die nicht ordnungsgemäße Beendigung eines **\_ \_ try** -Blocks bewirkt, dass das System alle Stapel Rahmen durchsucht, um zu bestimmen, ob Beendigungs Handler aufgerufen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="929a5-118">Abnormal termination of a **\_\_try** block causes the system to search backward through all stack frames to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="929a5-119">Dies kann dazu führen, dass Hunderte von Anweisungen ausgeführt werden. Daher ist es wichtig, eine nicht ordnungsgemäße Beendigung eines **\_ \_ try** -Blocks aufgrund einer **Rückgabe**-, **goto**-, **Continue**-oder **break** -Anweisung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="929a5-119">This can result in the execution of hundreds of instructions, so it is important to avoid abnormal termination of a **\_\_try** block due to a **return**, **goto**, **continue**, or **break** statement.</span></span> <span data-ttu-id="929a5-120">Beachten Sie, dass diese Anweisungen keine Ausnahme generieren, auch wenn die Beendigung nicht normal ist.</span><span class="sxs-lookup"><span data-stu-id="929a5-120">Note that these statements do not generate an exception, even though the termination is abnormal.</span></span>

<span data-ttu-id="929a5-121">Um eine ungewöhnliche Beendigung zu vermeiden, sollte die Ausführung bis zum Ende des Blocks fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="929a5-121">To avoid abnormal termination, execution should continue to the end of the block.</span></span> <span data-ttu-id="929a5-122">Sie können auch die **\_ \_ Leave** -Anweisung ausführen.</span><span class="sxs-lookup"><span data-stu-id="929a5-122">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="929a5-123">Mit der **\_ \_ Leave** -Anweisung kann der **\_ \_ try** -Block sofort beendet werden, ohne dass eine ungewöhnliche Beendigung und die Leistungseinbußen entstehen.</span><span class="sxs-lookup"><span data-stu-id="929a5-123">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="929a5-124">Überprüfen Sie in der Compilerdokumentation, ob die **\_ \_ Leave** -Anweisung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="929a5-124">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="929a5-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="929a5-125">Requirements</span></span>



| <span data-ttu-id="929a5-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="929a5-126">Requirement</span></span> | <span data-ttu-id="929a5-127">Wert</span><span class="sxs-lookup"><span data-stu-id="929a5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="929a5-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="929a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="929a5-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="929a5-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="929a5-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="929a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="929a5-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="929a5-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="929a5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="929a5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929a5-133">Funktionen für die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="929a5-133">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="929a5-134">Übersicht über die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="929a5-134">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> </dl>

 

 




