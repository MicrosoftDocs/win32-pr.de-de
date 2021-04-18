---
title: Asynchrone SSPI
description: Übersicht über den asynchronen SSPI-Header.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: acd1fedff605706dc5b20c3c2604a51d5cead27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352243"
---
# <a name="asynchronous-sspi"></a><span data-ttu-id="d9866-103">Asynchrone SSPI</span><span class="sxs-lookup"><span data-stu-id="d9866-103">Asynchronous SSPI</span></span>

<span data-ttu-id="d9866-104">Der asynchrone SSPI-Header enthält Funktionen, die Async-Kontext Objekte unterstützen, sodass Aufrufer über einen asynchronen SSPI-Aufruf Lebenszyklus gleichzeitig Sicherheits Kontexte zwischen Server-und Remote Clients einrichten können.</span><span class="sxs-lookup"><span data-stu-id="d9866-104">The asynchronous SSPI header includes functions that support async context objects, allowing callers to establish security contexts between server and remote clients concurrently through an async SSPI call lifecycle.</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="d9866-105">Asynchrone Kontext Verwaltungs Typen</span><span class="sxs-lookup"><span data-stu-id="d9866-105">Async context management types</span></span>

| <span data-ttu-id="d9866-106">Objektname</span><span class="sxs-lookup"><span data-stu-id="d9866-106">Object Name</span></span> | <span data-ttu-id="d9866-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9866-107">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="d9866-108">Sspiasyncnotifycallback</span><span class="sxs-lookup"><span data-stu-id="d9866-108">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="d9866-109">Rückruf, der zum Benachrichtigen des Abschlusses eines Async-SSPI-Aufrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9866-109">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="d9866-110">Asynchrone Kontext Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="d9866-110">Async context management functions</span></span>

| <span data-ttu-id="d9866-111">API-Name</span><span class="sxs-lookup"><span data-stu-id="d9866-111">API Name</span></span> | <span data-ttu-id="d9866-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9866-112">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="d9866-113">Sspikreateasynccontext</span><span class="sxs-lookup"><span data-stu-id="d9866-113">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="d9866-114">Erstellt eine Instanz von sspiasynccontext, die zum Nachverfolgen des asynchronen Aufrufes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9866-114">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="d9866-115">Sspireinitasynccontext</span><span class="sxs-lookup"><span data-stu-id="d9866-115">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="d9866-116">Markiert einen Async-Kontext für die Wiederverwendung.</span><span class="sxs-lookup"><span data-stu-id="d9866-116">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="d9866-117">Sspisetasyncnotifycallback</span><span class="sxs-lookup"><span data-stu-id="d9866-117">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="d9866-118">Registriert einen Rückruf, der beim Abschluss des asynchronen Aufrufs benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="d9866-118">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="d9866-119">Sspiasynccontextrequiresnotify</span><span class="sxs-lookup"><span data-stu-id="d9866-119">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="d9866-120">Bestimmt, ob ein angegebener asynchroner Kontext eine Benachrichtigung über den Abschluss des Aufrufes erfordert.</span><span class="sxs-lookup"><span data-stu-id="d9866-120">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="d9866-121">Sspigetasynccallstatus</span><span class="sxs-lookup"><span data-stu-id="d9866-121">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="d9866-122">Ruft den aktuellen Status eines Async-Aufrufes ab, der dem bereitgestellten Kontext zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9866-122">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="d9866-123">Sspifreasynccontext</span><span class="sxs-lookup"><span data-stu-id="d9866-123">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="d9866-124">Gibt einen kontextfrei, der im Aufrufen der sspikreateasynccontext-Funktion erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9866-124">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="d9866-125">Async-SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d9866-125">Async SSPI functions</span></span>

<span data-ttu-id="d9866-126">Die folgenden Funktionen akzeptieren einen asynchronen Kontext zusätzlich zu denselben Parametern wie Ihre synchrone Entsprechung.</span><span class="sxs-lookup"><span data-stu-id="d9866-126">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="d9866-127">API-Name</span><span class="sxs-lookup"><span data-stu-id="d9866-127">API Name</span></span> | <span data-ttu-id="d9866-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9866-128">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="d9866-129">Sspiacquirecredentialshandleasync</span><span class="sxs-lookup"><span data-stu-id="d9866-129">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="d9866-130">Ruft asynchron ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab.</span><span class="sxs-lookup"><span data-stu-id="d9866-130">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="d9866-131">Sspiaccept tsecuritycontextasync</span><span class="sxs-lookup"><span data-stu-id="d9866-131">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="d9866-132">Ermöglicht der Serverkomponente einer Transport Anwendung das asynchrone Einrichten eines Sicherheits Kontexts zwischen dem Server und einem Remote Client.</span><span class="sxs-lookup"><span data-stu-id="d9866-132">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="d9866-133">Sspiinitializesecuritycontextasync</span><span class="sxs-lookup"><span data-stu-id="d9866-133">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="d9866-134">Initialisiert einen Async-Sicherheitskontext.</span><span class="sxs-lookup"><span data-stu-id="d9866-134">Initializes an async security context.</span></span> |
| [<span data-ttu-id="d9866-135">Sspidelta etesecuritycontextasync</span><span class="sxs-lookup"><span data-stu-id="d9866-135">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="d9866-136">Löscht die lokalen Datenstrukturen, die dem angegebenen Sicherheitskontext zugeordnet sind, der durch einen vorherigen Aufrufen der sspiinitializesecuritycontextasync-Funktion oder der sspiaccept-securitycontextasync-Funktion initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9866-136">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="d9866-137">Sspifreecredentialshandleasync</span><span class="sxs-lookup"><span data-stu-id="d9866-137">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="d9866-138">Gibt ein Anmelde Informationen-Handle frei.</span><span class="sxs-lookup"><span data-stu-id="d9866-138">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="d9866-139">API-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d9866-139">API Sample</span></span>

<span data-ttu-id="d9866-140">Ein typischer callflow funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d9866-140">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="d9866-141">Sspiasynccontext-Kontext zum Nachverfolgen des Aufrufes mithilfe von [sspikreateasynccontext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) erstellen</span><span class="sxs-lookup"><span data-stu-id="d9866-141">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="d9866-142">Registrieren eines [sspiasyncnotifycallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) für den Kontext</span><span class="sxs-lookup"><span data-stu-id="d9866-142">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="d9866-143">Asynchronen Aufrufen mithilfe von [sspiaccept tsecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="d9866-143">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="d9866-144">Bei Rückruf das Ergebnis mithilfe von [sspigetasynccallstatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) abrufen</span><span class="sxs-lookup"><span data-stu-id="d9866-144">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="d9866-145">Löschen Sie sspiasynccontext mithilfe von [sspidelta etesecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="d9866-145">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="d9866-146">Wenn Sie den Kontext mit [sspireinitasynccontext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)wieder verwenden, gehen Sie zurück zu Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="d9866-146">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="d9866-147">Das folgende Beispiel veranschaulicht den Aufruf von sspiaccept tsecuritycontextasync.</span><span class="sxs-lookup"><span data-stu-id="d9866-147">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="d9866-148">Das Beispiel wartet auf den Abschluss des Aufrufes und ruft das Ergebnis ab.</span><span class="sxs-lookup"><span data-stu-id="d9866-148">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="d9866-149">Bei einem vollständigen SSPI-Handshake werden "sspiaccept tsecuritycontextasync" und "sspiinitializesecuritycontextasync" mehrmals aufgerufen, bis SEC_E_OK zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d9866-149">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="d9866-150">Sspireinitasynccontext wurde bereitgestellt, um die Benutzerfreundlichkeit zu vereinfachen und die Leistung in diesem Fall zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="d9866-150">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="d9866-151">Assertionen werden verwendet, um hervorzuheben, was wir bei Erfolg erwarten.</span><span class="sxs-lookup"><span data-stu-id="d9866-151">Asserts are used to highlight what we would expect in the case of success.</span></span>

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a><span data-ttu-id="d9866-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d9866-152">See Also</span></span>

[<span data-ttu-id="d9866-153">SSPI. h-Header</span><span class="sxs-lookup"><span data-stu-id="d9866-153">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="d9866-154">SSPI-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d9866-154">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="d9866-155">SSPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d9866-155">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


