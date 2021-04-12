---
title: Asynchrone Kontexte
description: Übersicht über asynchrone Kontexte und den asynchronen SSPI-Header.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e523112d35e0ddbc38c3374c67e3d81ba74a6dce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347298"
---
# <a name="asynchronous-contexts"></a>Asynchrone Kontexte

Asynchrone SSPI-Sicherheits Kontexte ermöglichen Aufrufern das fortfahren ohne Blockierung und Empfang von Benachrichtigungen, sobald der Aufruf abgeschlossen ist. Asynchrone Kontexte werden derzeit nur für TLS-Clients und-Server im Kernelmodus unterstützt. Die folgenden asynchronen SSPI-Funktionen werden in asynchronen Sicherheits Kontexten ausgeführt:

## <a name="async-context-management-types"></a>Asynchrone Kontext Verwaltungs Typen

| Objektname | BESCHREIBUNG |
|-------------|--------------|
| [Sspiasyncnotifycallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Rückruf, der zum Benachrichtigen des Abschlusses eines Async-SSPI-Aufrufs verwendet wird. |


## <a name="async-context-management-functions"></a>Asynchrone Kontext Verwaltungsfunktionen

| API-Name | BESCHREIBUNG |
|-------------|--------------|
| [Sspikreateasynccontext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Erstellt eine Instanz von sspiasynccontext, die zum Nachverfolgen des asynchronen Aufrufes verwendet wird. |
| [Sspireinitasynccontext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Markiert einen Async-Kontext für die Wiederverwendung. |
| [Sspisetasyncnotifycallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registriert einen Rückruf, der beim Abschluss des asynchronen Aufrufs benachrichtigt wird. |
| [Sspiasynccontextrequiresnotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Bestimmt, ob ein angegebener asynchroner Kontext eine Benachrichtigung über den Abschluss des Aufrufes erfordert. |
| [Sspigetasynccallstatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Ruft den aktuellen Status eines Async-Aufrufes ab, der dem bereitgestellten Kontext zugeordnet ist.  |
| [Sspifreasynccontext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Gibt einen kontextfrei, der im Aufrufen der sspikreateasynccontext-Funktion erstellt wurde. |

## <a name="async-sspi-functions"></a>Async-SSPI-Funktionen

Die folgenden Funktionen akzeptieren einen asynchronen Kontext zusätzlich zu denselben Parametern wie Ihre synchrone Entsprechung.

| API-Name | BESCHREIBUNG |
|-------------|--------------|
| [Sspiacquirecredentialshandleasync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Ruft asynchron ein Handle für bereits vorhandene Anmelde Informationen eines Sicherheits Prinzipals ab. |
| [Sspiaccept tsecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Ermöglicht der Serverkomponente einer Transport Anwendung das asynchrone Einrichten eines Sicherheits Kontexts zwischen dem Server und einem Remote Client. |
| [Sspiinitializesecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Initialisiert einen Async-Sicherheitskontext. |
| [Sspidelta etesecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Löscht die lokalen Datenstrukturen, die dem angegebenen Sicherheitskontext zugeordnet sind, der durch einen vorherigen Aufrufen der sspiinitializesecuritycontextasync-Funktion oder der sspiaccept-securitycontextasync-Funktion initiiert wurde. |
| [Sspifreecredentialshandleasync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Gibt ein Anmelde Informationen-Handle frei. |

## <a name="api-sample"></a>API-Beispiel

Ein typischer callflow funktioniert wie folgt:
1) Sspiasynccontext-Kontext zum Nachverfolgen des Aufrufes mithilfe von [sspikreateasynccontext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) erstellen
2) Registrieren eines [sspiasyncnotifycallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) für den Kontext
3) Asynchronen Aufrufen mithilfe von [sspiaccept tsecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) Bei Rückruf das Ergebnis mithilfe von [sspigetasynccallstatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) abrufen
5) Löschen Sie sspiasynccontext mithilfe von [sspidelta etesecuritycontextasync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync). Wenn Sie den Kontext mit [sspireinitasynccontext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)wieder verwenden, gehen Sie zurück zu Schritt 2.

Das folgende Beispiel veranschaulicht den Aufruf von sspiaccept tsecuritycontextasync. Das Beispiel wartet auf den Abschluss des Aufrufes und ruft das Ergebnis ab.

Bei einem vollständigen SSPI-Handshake werden "sspiaccept tsecuritycontextasync" und "sspiinitializesecuritycontextasync" mehrmals aufgerufen, bis SEC_E_OK zurückgegeben wird. Sspireinitasynccontext wurde bereitgestellt, um die Benutzerfreundlichkeit zu vereinfachen und die Leistung in diesem Fall zu vereinfachen.

Assertionen werden verwendet, um hervorzuheben, was wir bei Erfolg erwarten.

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

## <a name="see-also"></a>Weitere Informationen

[SSPI. h-Header](/windows/win32/api/sspi/)

[SSPI-Funktionen](/windows/win32/api/sspi/#functions)

[SSPI-Strukturen](/windows/win32/api/sspi/#structures)


