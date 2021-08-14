---
title: Asynchrone SSPI
description: Übersicht über den asynchronen SSPI-Header.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e2fe4e6cc8358ec39c402bccdf8562d613ac952547687142cb3553d04c8f0ce6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917165"
---
# <a name="asynchronous-sspi"></a>Asynchrone SSPI

Der asynchrone SSPI-Header enthält Funktionen, die asynchrone Kontextobjekte unterstützen, sodass Aufrufer über einen asynchronen SSPI-Aufruflebenszyklus gleichzeitig Sicherheitskontexte zwischen Server- und Remoteclients einrichten können.

## <a name="async-context-management-types"></a>Asynchrone Kontextverwaltungstypen

| Objektname | BESCHREIBUNG |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Rückruf, der zum Benachrichtigen des Abschlusses eines asynchronen SSPI-Aufrufs verwendet wird. |


## <a name="async-context-management-functions"></a>Asynchrone Kontextverwaltungsfunktionen

| API-Name | BESCHREIBUNG |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Erstellt eine Instanz von SspiAsyncContext, die zum Nachverfolgen des asynchronen Aufrufs verwendet wird. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Markiert einen asynchronen Kontext für die Wiederverwendung. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registriert einen Rückruf, der bei abschluss des asynchronen Aufrufs benachrichtigt wird. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Bestimmt, ob für einen bestimmten asynchronen Kontext eine Benachrichtigung beim Abschluss des Aufrufs erforderlich ist. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Ruft den aktuellen Status eines asynchronen Aufrufs ab, der dem bereitgestellten Kontext zugeordnet ist.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Gibt einen Kontext frei, der im Aufruf der SspiCreateAsyncContext-Funktion erstellt wurde. |

## <a name="async-sspi-functions"></a>Asynchrone SSPI-Funktionen

Die folgenden Funktionen akzeptieren einen asynchronen Kontext zusätzlich zu den gleichen Parametern wie ihre synchrone Entsprechung.

| API-Name | BESCHREIBUNG |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Übernimmt asynchron ein Handle für bereits vorhandene Anmeldeinformationen eines Sicherheitsprinzipals. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Ermöglicht der Serverkomponente einer Transportanwendung das asynchrone Einrichten eines Sicherheitskontexts zwischen dem Server und einem Remoteclient. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Initialisiert einen asynchronen Sicherheitskontext. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Löscht die lokalen Datenstrukturen, die dem angegebenen Sicherheitskontext zugeordnet sind, der durch einen vorherigen Aufruf der SspiInitializeSecurityContextAsync-Funktion oder der SspiAcceptSecurityContextAsync-Funktion initiiert wurde. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Gibt ein Anmeldeinformationshand handle frei. |

## <a name="api-sample"></a>API-Beispiel

Ein typischer Aufruffluss funktioniert wie folgt:
1) Erstellen eines SspiAsyncContext-Kontexts zum Nachverfolgen eines [Aufrufs mithilfe von SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Registrieren eines [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) für den Kontext
3) Führen Sie den asynchronen Aufruf [mithilfe von SspiAcceptSecurityContextAsync aus.](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) Rufen Sie beim Rückruf das Ergebnis mithilfe von [SspiGetAsyncCallStatus ab.](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Löschen Sie SspiAsyncContext [mithilfe von SspiDeleteSecurityContextAsync.](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) Wenn Sie den Kontext mit [SspiReinitAsyncContext wiederverwenden,](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)fahren Sie mit Schritt 2 fort.

Das folgende Beispiel veranschaulicht einen Aufruf von SspiAcceptSecurityContextAsync. Das Beispiel wartet auf den Abschluss des Aufrufs und ruft das Ergebnis ab.

In einem vollständigen SSPI-Handshake werden SspiAcceptSecurityContextAsync und SspiInitializeSecurityContextAsync mehrmals aufgerufen, bis SEC_E_OK zurückgegeben wird. SspiReinitAsyncContext wurde bereitgestellt, um die Benutzerfreundlichkeit zu erleichtern und die Leistung in diesem Fall zu erleichtern.

Asserts werden verwendet, um hervorzuheben, was wir bei einem Erfolg erwarten würden.

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

[sspi.h-Header](/windows/win32/api/sspi/)

[SSPI-Funktionen](/windows/win32/api/sspi/#functions)

[SSPI-Strukturen](/windows/win32/api/sspi/#structures)


