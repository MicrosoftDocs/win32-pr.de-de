---
description: Ruft eine Computer unabhängige Beschreibung einer Ausnahme und Informationen zu dem Computer Zustand ab, der für den Thread vorhanden ist, wenn die Ausnahme auftritt. Diese Funktion kann nur innerhalb des Filter Ausdrucks eines Ausnahme Handlers aufgerufen werden.
ms.assetid: e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae
title: GetExceptionInformation-Makro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetExceptionInformation
api_type:
- NA
api_location: ''
ms.openlocfilehash: 243831a94a26b86df29d3a50413bfa9d6830a0e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748889"
---
# <a name="getexceptioninformation-macro"></a><span data-ttu-id="88628-104">GetExceptionInformation-Makro</span><span class="sxs-lookup"><span data-stu-id="88628-104">GetExceptionInformation macro</span></span>

<span data-ttu-id="88628-105">Ruft eine Computer unabhängige Beschreibung einer Ausnahme und Informationen zu dem Computer Zustand ab, der für den Thread vorhanden ist, wenn die Ausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="88628-105">Retrieves a computer-independent description of an exception, and information about the computer state that exists for the thread when the exception occurs.</span></span> <span data-ttu-id="88628-106">Diese Funktion kann nur innerhalb des Filter Ausdrucks eines Ausnahme Handlers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="88628-106">This function can be called only from within the filter expression of an exception handler.</span></span>

> [!Note]  
> <span data-ttu-id="88628-107">Der Microsoft C/C++-Optimierungs Compiler interpretiert diese Funktion als Schlüsselwort, und die Verwendung außerhalb der entsprechenden Syntax zur Ausnahmebehandlung generiert einen Compilerfehler.</span><span class="sxs-lookup"><span data-stu-id="88628-107">The Microsoft C/C++ Optimizing Compiler interprets this function as a keyword, and its use outside the appropriate exception-handling syntax generates a compiler error.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="88628-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="88628-108">Syntax</span></span>


```C++
LPEXCEPTION_POINTERS GetExceptionInformation(void);
```



## <a name="parameters"></a><span data-ttu-id="88628-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="88628-109">Parameters</span></span>

<span data-ttu-id="88628-110">Dieses Makro weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="88628-110">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88628-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88628-111">Return value</span></span>

<span data-ttu-id="88628-112">Ein Zeiger auf eine [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Struktur, die Zeiger auf die folgenden zwei-Strukturen enthält:</span><span class="sxs-lookup"><span data-stu-id="88628-112">A pointer to an [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) structure that contains pointers to the following two structures:</span></span>

-   <span data-ttu-id="88628-113">[**Ausnahme \_ Daten Satz**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Struktur, die eine Beschreibung der Ausnahme enthält.</span><span class="sxs-lookup"><span data-stu-id="88628-113">[**EXCEPTION\_RECORD**](/windows/desktop/api/WinNT/ns-winnt-exception_record) structure that contains a description of the exception.</span></span>
-   <span data-ttu-id="88628-114">Die [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Struktur, die die Computer Zustandsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="88628-114">[**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure that contains the computer state information.</span></span>

## <a name="remarks"></a><span data-ttu-id="88628-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88628-115">Remarks</span></span>

<span data-ttu-id="88628-116">Der Filter Ausdruck (von dem die Funktion aufgerufen wird) wird ausgewertet, wenn während der Ausführung des **\_ \_ try** -Blocks eine Ausnahme auftritt, und bestimmt, ob der **\_ \_ Ausnahme** Block ausgeführt wird oder nicht.</span><span class="sxs-lookup"><span data-stu-id="88628-116">The filter expression (from which the function is called) is evaluated if an exception occurs during execution of the **\_\_try** block, and it determines whether or not the **\_\_except** block is executed.</span></span>

<span data-ttu-id="88628-117">Der Filter Ausdruck kann eine Filterfunktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="88628-117">The filter expression can invoke a filter function.</span></span> <span data-ttu-id="88628-118">Die Filterfunktion kann **GetExceptionInformation** nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="88628-118">The filter function cannot call **GetExceptionInformation**.</span></span> <span data-ttu-id="88628-119">Der Rückgabewert von **GetExceptionInformation** kann jedoch als Parameter an eine Filterfunktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="88628-119">However, the return value of **GetExceptionInformation** can be passed as a parameter to a filter function.</span></span>

<span data-ttu-id="88628-120">Um die [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Informationen an den Ausnahmehandlerblock zu übergeben, muss der Filter Ausdruck oder die Filterfunktion den Zeiger oder die Daten in den sicheren Speicher kopieren, auf den der Handler später zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="88628-120">To pass the [**EXCEPTION\_POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) information to the exception-handler block, the filter expression or filter function must copy the pointer or the data to safe storage that the handler can later access.</span></span>

<span data-ttu-id="88628-121">Im Fall von schsted Handlern wird jeder Filter Ausdruck ausgewertet, bis ein Filter Ausdruck ausgewertet wird, wenn der **Ausnahme Ausführungs \_ \_ Handler** oder eine **Ausnahme \_ \_ Ausführung fortgesetzt** wird.</span><span class="sxs-lookup"><span data-stu-id="88628-121">In the case of nested handlers, each filter expression is evaluated until one is evaluated as **EXCEPTION\_EXECUTE\_HANDLER** or **EXCEPTION\_CONTINUE\_EXECUTION**.</span></span> <span data-ttu-id="88628-122">Jeder Filter Ausdruck kann **GetExceptionInformation** aufrufen, um Ausnahme Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="88628-122">Each filter expression can invoke **GetExceptionInformation** to get exception information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88628-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88628-123">Requirements</span></span>



| <span data-ttu-id="88628-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88628-124">Requirement</span></span> | <span data-ttu-id="88628-125">Wert</span><span class="sxs-lookup"><span data-stu-id="88628-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="88628-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88628-126">Minimum supported client</span></span><br/> | <span data-ttu-id="88628-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88628-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="88628-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88628-128">Minimum supported server</span></span><br/> | <span data-ttu-id="88628-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88628-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88628-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88628-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88628-131">**Kontext**</span><span class="sxs-lookup"><span data-stu-id="88628-131">**CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context)
</dt> <dt>

[<span data-ttu-id="88628-132">**Ausnahme \_ Zeiger**</span><span class="sxs-lookup"><span data-stu-id="88628-132">**EXCEPTION\_POINTERS**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_pointers)
</dt> <dt>

[<span data-ttu-id="88628-133">**Ausnahme \_ Daten Satz**</span><span class="sxs-lookup"><span data-stu-id="88628-133">**EXCEPTION\_RECORD**</span></span>](/windows/desktop/api/WinNT/ns-winnt-exception_record)
</dt> <dt>

[<span data-ttu-id="88628-134">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="88628-134">**GetExceptionCode**</span></span>](getexceptioncode.md)
</dt> <dt>

[<span data-ttu-id="88628-135">**Getxstatefeaturesmask**</span><span class="sxs-lookup"><span data-stu-id="88628-135">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)
</dt> <dt>

[<span data-ttu-id="88628-136">Funktionen für die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="88628-136">Structured Exception Handling Functions</span></span>](structured-exception-handling-functions.md)
</dt> <dt>

[<span data-ttu-id="88628-137">Übersicht über die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="88628-137">Structured Exception Handling Overview</span></span>](structured-exception-handling.md)
</dt> <dt>

[<span data-ttu-id="88628-138">Windows-Unterstützung für Intel AVX aktivieren</span><span class="sxs-lookup"><span data-stu-id="88628-138">Enable Windows Support for Intel AVX</span></span>](../win7appqual/enable-windows-7-support-for-intel-avx.md)
</dt> </dl>

 

 
