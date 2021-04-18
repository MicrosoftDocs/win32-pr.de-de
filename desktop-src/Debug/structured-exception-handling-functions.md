---
description: Die folgenden Funktionen werden bei der strukturierten Ausnahmebehandlung verwendet.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funktionen für die strukturierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343590"
---
# <a name="structured-exception-handling-functions"></a><span data-ttu-id="7dc53-103">Funktionen für die strukturierte Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="7dc53-103">Structured Exception Handling Functions</span></span>

<span data-ttu-id="7dc53-104">Die folgenden Funktionen werden bei der strukturierten Ausnahmebehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7dc53-104">The following functions are used in structured exception handling.</span></span>

-   [<span data-ttu-id="7dc53-105">**AbnormalTermination**</span><span class="sxs-lookup"><span data-stu-id="7dc53-105">**AbnormalTermination**</span></span>](abnormaltermination.md)

    <span data-ttu-id="7dc53-106">Gibt an, ob der **\_ \_ try** -Block eines Beendigungs Handlers normal beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7dc53-106">Indicates whether the **\_\_try** block of a termination handler terminated normally.</span></span>

-   [<span data-ttu-id="7dc53-107">**Addvector edcontinuehandler**</span><span class="sxs-lookup"><span data-stu-id="7dc53-107">**AddVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    <span data-ttu-id="7dc53-108">Registriert einen Vektoren Continue-Handler.</span><span class="sxs-lookup"><span data-stu-id="7dc53-108">Registers a vectored continue handler.</span></span>

-   [<span data-ttu-id="7dc53-109">**Addvector edexceptionhandler**</span><span class="sxs-lookup"><span data-stu-id="7dc53-109">**AddVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    <span data-ttu-id="7dc53-110">Registriert einen Vektor Ausnahmehandler.</span><span class="sxs-lookup"><span data-stu-id="7dc53-110">Registers a vectored exception handler.</span></span>

-   [<span data-ttu-id="7dc53-111">**GetExceptionCode**</span><span class="sxs-lookup"><span data-stu-id="7dc53-111">**GetExceptionCode**</span></span>](getexceptioncode.md)

    <span data-ttu-id="7dc53-112">Ruft einen Code ab, der den Typ der aufgetretenen Ausnahme identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7dc53-112">Retrieves a code that identifies the type of exception that occurred.</span></span>

-   [<span data-ttu-id="7dc53-113">**GetExceptionInformation**</span><span class="sxs-lookup"><span data-stu-id="7dc53-113">**GetExceptionInformation**</span></span>](getexceptioninformation.md)

    <span data-ttu-id="7dc53-114">Ruft eine Computer unabhängige Beschreibung einer Ausnahme und Informationen zum Computer Zustand ab, der für den Thread vorhanden war, als die Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="7dc53-114">Retrieves a machine-independent description of an exception, and information about the machine state that existed for the thread when the exception occurred.</span></span>

-   [<span data-ttu-id="7dc53-115">**RaiseException**</span><span class="sxs-lookup"><span data-stu-id="7dc53-115">**RaiseException**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    <span data-ttu-id="7dc53-116">Löst eine Ausnahme im aufrufenden Thread aus.</span><span class="sxs-lookup"><span data-stu-id="7dc53-116">Raises an exception in the calling thread.</span></span>

-   [<span data-ttu-id="7dc53-117">**Removevector edcontinuehandler**</span><span class="sxs-lookup"><span data-stu-id="7dc53-117">**RemoveVectoredContinueHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    <span data-ttu-id="7dc53-118">Hebt die Registrierung eines vektorcontinue Continue-Handlers auf.</span><span class="sxs-lookup"><span data-stu-id="7dc53-118">Unregisters a vectored continue handler.</span></span>

-   [<span data-ttu-id="7dc53-119">**Removevector edexceptionhandler**</span><span class="sxs-lookup"><span data-stu-id="7dc53-119">**RemoveVectoredExceptionHandler**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    <span data-ttu-id="7dc53-120">Hebt die Registrierung eines Vektoren Ausnahme Handlers auf.</span><span class="sxs-lookup"><span data-stu-id="7dc53-120">Unregisters a vectored exception handler.</span></span>

-   [<span data-ttu-id="7dc53-121">**Rtladdgrowablefunctiontable**</span><span class="sxs-lookup"><span data-stu-id="7dc53-121">**RtlAddGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    <span data-ttu-id="7dc53-122">Informiert das System über eine dynamische Funktions Tabelle, die einen Bereich des Arbeitsspeichers darstellt, der Code enthält.</span><span class="sxs-lookup"><span data-stu-id="7dc53-122">Informs the system of a dynamic function table representing a region of memory containing code.</span></span>

-   [<span data-ttu-id="7dc53-123">**Rtldeletegrowablefunctiontable**</span><span class="sxs-lookup"><span data-stu-id="7dc53-123">**RtlDeleteGrowableFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    <span data-ttu-id="7dc53-124">Informiert das System darüber, dass eine zuvor gemeldete dynamische Funktions Tabelle nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7dc53-124">Informs the system that a previously reported dynamic function table is no longer in use.</span></span>

-   [<span data-ttu-id="7dc53-125">**Rtlgrowfunctiontable**</span><span class="sxs-lookup"><span data-stu-id="7dc53-125">**RtlGrowFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    <span data-ttu-id="7dc53-126">Meldet, dass eine dynamische Funktions Tabelle die Größe übersteigt.</span><span class="sxs-lookup"><span data-stu-id="7dc53-126">Reports that a dynamic function table has increased in size.</span></span>

-   [<span data-ttu-id="7dc53-127">**"Set"-Filter**</span><span class="sxs-lookup"><span data-stu-id="7dc53-127">**SetUnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    <span data-ttu-id="7dc53-128">Ermöglicht es einer Anwendung, den Ausnahmehandler der obersten Ebene jedes Threads und Prozesses zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7dc53-128">Enables an application to supersede the top-level exception handler of each thread and process.</span></span>

-   [<span data-ttu-id="7dc53-129">**UnhandledExceptionFilter "**</span><span class="sxs-lookup"><span data-stu-id="7dc53-129">**UnhandledExceptionFilter**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    <span data-ttu-id="7dc53-130">Übergibt nicht behandelte Ausnahmen an den Debugger, wenn der Prozess gedebuggt wird.</span><span class="sxs-lookup"><span data-stu-id="7dc53-130">Passes unhandled exceptions to the debugger, if the process is being debugged.</span></span>

-   [<span data-ttu-id="7dc53-131">**Vectoriedhandler**</span><span class="sxs-lookup"><span data-stu-id="7dc53-131">**VectoredHandler**</span></span>](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    <span data-ttu-id="7dc53-132">Eine Anwendungs definierte Funktion, die als ein Vektoren-Ausnahmehandler fungiert.</span><span class="sxs-lookup"><span data-stu-id="7dc53-132">An application-defined function that serves as a vectored exception handler.</span></span>

<span data-ttu-id="7dc53-133">Die folgenden Funktionen werden nur für 64-Bit-Fenster verwendet.</span><span class="sxs-lookup"><span data-stu-id="7dc53-133">The following functions are used only on 64-bit Windows.</span></span>

-   [<span data-ttu-id="7dc53-134">**RtlAddFunctionTable**</span><span class="sxs-lookup"><span data-stu-id="7dc53-134">**RtlAddFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    <span data-ttu-id="7dc53-135">Fügt der Liste der dynamischen Funktionstabellen eine dynamische Funktions Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7dc53-135">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="7dc53-136">**Rtlcapturecontext**</span><span class="sxs-lookup"><span data-stu-id="7dc53-136">**RtlCaptureContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    <span data-ttu-id="7dc53-137">Ruft einen Kontext Daten Satz im Kontext des Aufrufers ab.</span><span class="sxs-lookup"><span data-stu-id="7dc53-137">Retrieves a context record in the context of the caller.</span></span>

-   [<span data-ttu-id="7dc53-138">**Rtldeletefunctiontable**</span><span class="sxs-lookup"><span data-stu-id="7dc53-138">**RtlDeleteFunctionTable**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    <span data-ttu-id="7dc53-139">Entfernt eine dynamische Funktions Tabelle aus der Liste der dynamischen Funktionstabellen.</span><span class="sxs-lookup"><span data-stu-id="7dc53-139">Removes a dynamic function table from the dynamic function table list.</span></span>

-   [<span data-ttu-id="7dc53-140">**Rtlinstallfunctiontablecallback**</span><span class="sxs-lookup"><span data-stu-id="7dc53-140">**RtlInstallFunctionTableCallback**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    <span data-ttu-id="7dc53-141">Fügt der Liste der dynamischen Funktionstabellen eine dynamische Funktions Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7dc53-141">Adds a dynamic function table to the dynamic function table list.</span></span>

-   [<span data-ttu-id="7dc53-142">**Rtlrestorecontext**</span><span class="sxs-lookup"><span data-stu-id="7dc53-142">**RtlRestoreContext**</span></span>](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    <span data-ttu-id="7dc53-143">Stellt den Kontext des Aufrufers für den angegebenen Kontext Daten Satz wieder her.</span><span class="sxs-lookup"><span data-stu-id="7dc53-143">Restores the context of the caller to the specified context record.</span></span>

 

 
