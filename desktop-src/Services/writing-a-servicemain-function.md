---
description: Die SvcMain-Funktion im folgenden Beispiel ist die ServiceMain-Funktion für den Beispieldienst.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Schreiben einer ServiceMain-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca28b09efdc228457ae85d8a3343f334a26f246b6e48e49208d7416551e7f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887973"
---
# <a name="writing-a-servicemain-function"></a>Schreiben einer ServiceMain-Funktion

Die SvcMain-Funktion im folgenden Beispiel ist die [**ServiceMain-Funktion**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) für den Beispieldienst. SvcMain hat Zugriff auf die Befehlszeilenargumente für den Dienst, wie es die **Hauptfunktion** einer Konsolenanwendung tut. Der erste Parameter enthält die Anzahl der Argumente, die im zweiten Parameter an den Dienst übergeben werden. Es gibt immer mindestens ein Argument. Der zweite Parameter ist ein Zeiger auf ein Array von Zeichenfolgenzeigern. Das erste Element im Array ist immer der Dienstname.

Die SvcMain-Funktion ruft zuerst die [**RegisterServiceCtrlHandler-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) auf, um die SvcCtrlHandler-Funktion als [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) des Diensts zu registrieren und mit der Initialisierung zu beginnen. **RegisterServiceCtrlHandler** sollte die erste nicht funktionsfähige Funktion in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) sein, damit der Dienst das von dieser Funktion zurückgegebene Statushandle verwenden kann, um [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit dem Status SERVICE \_ STOPPED aufzurufen, wenn ein Fehler auftritt.

Als Nächstes ruft die SvcMain-Funktion die ReportSvcStatus-Funktion auf, um anzugeben, dass ihr Anfangsstatus SERVICE \_ START \_ PENDING lautet. Während sich der Dienst in diesem Zustand befindet, werden keine Steuerelemente akzeptiert. Um die Logik des Diensts zu vereinfachen, wird empfohlen, dass der Dienst während der Initialisierung keine Steuerelemente akzeptiert.

Schließlich ruft die SvcMain-Funktion die SvcInit-Funktion auf, um die dienstspezifische Initialisierung durchzuführen und mit der Arbeit zu beginnen, die vom Dienst ausgeführt werden soll.

Die Beispielinitialisierungsfunktion SvcInit ist ein sehr einfaches Beispiel. sie führt keine komplexeren Initialisierungsaufgaben wie das Erstellen zusätzlicher Threads durch. Es wird ein Ereignis erstellt, das der Dienststeuerungshandler signalisieren kann, um anzugeben, dass der Dienst beendet werden soll, und dann ReportSvcStatus aufruft, um anzugeben, dass der Dienst den Status SERVICE RUNNING erreicht \_ hat. An diesem Punkt hat der Dienst seine Initialisierung abgeschlossen und ist bereit, Steuerelemente zu akzeptieren. Um eine optimale Systemleistung zu erzielen, sollte Ihre Anwendung innerhalb von 25 bis 100 Millisekunden in den Ausführungszustand übergehen.

Da dieser Beispieldienst keine echten Aufgaben abschließt, wartet SvcInit einfach, bis das Dienststoppereignis signalisiert wird, indem die [**WaitForSingleObject-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) aufgerufen wird, ruft ReportSvcStatus auf, um anzugeben, dass der Dienst den Status SERVICE STOPPED erreicht \_ hat, und gibt zurück. (Beachten Sie, dass es wichtig ist, dass die Funktion zurückgibt, anstatt die [**ExitThread-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) aufzurufen, da die Rückgabe eine Bereinigung des Speichers ermöglicht, der für die Argumente zugeordnet ist.) Sie können zusätzliche Bereinigungsaufgaben ausführen, indem Sie die [**RegisterWaitForSingleObject-Funktion**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) anstelle von **WaitForSingleObject** verwenden. Der Thread, der die [**ServiceMain-Funktion**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) ausführt, wird beendet, aber der Dienst selbst wird weiterhin ausgeführt. Wenn der Dienststeuerungshandler das Ereignis signalisiert, führt ein Thread aus dem Threadpool Ihren Rückruf aus, um die zusätzliche Bereinigung durchzuführen, einschließlich der Einstellung des Status auf SERVICE \_ STOPPED.

Beachten Sie, dass in diesem Beispiel SvcReportEvent verwendet wird, um Fehlerereignisse in das Ereignisprotokoll zu schreiben. Den Quellcode für SvcReportEvent finden Sie unter [Svc.cpp.](svc-cpp.md) Ein Beispiel für eine Steuerelementhandlerfunktion finden Sie unter [Schreiben einer Steuerelementhandlerfunktion.](writing-a-control-handler-function.md)

In diesem Beispiel werden die folgenden globalen Definitionen verwendet.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Das folgende Beispielfragment stammt aus dem vollständigen Dienstbeispiel.


```C++
//
// Purpose: 
//   Entry point for the service
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None.
//
VOID WINAPI SvcMain( DWORD dwArgc, LPTSTR *lpszArgv )
{
    // Register the handler function for the service

    gSvcStatusHandle = RegisterServiceCtrlHandler( 
        SVCNAME, 
        SvcCtrlHandler);

    if( !gSvcStatusHandle )
    { 
        SvcReportEvent(TEXT("RegisterServiceCtrlHandler")); 
        return; 
    } 

    // These SERVICE_STATUS members remain as set here

    gSvcStatus.dwServiceType = SERVICE_WIN32_OWN_PROCESS; 
    gSvcStatus.dwServiceSpecificExitCode = 0;    

    // Report initial status to the SCM

    ReportSvcStatus( SERVICE_START_PENDING, NO_ERROR, 3000 );

    // Perform service-specific initialization and work.

    SvcInit( dwArgc, lpszArgv );
}

//
// Purpose: 
//   The service code
//
// Parameters:
//   dwArgc - Number of arguments in the lpszArgv array
//   lpszArgv - Array of strings. The first string is the name of
//     the service and subsequent strings are passed by the process
//     that called the StartService function to start the service.
// 
// Return value:
//   None
//
VOID SvcInit( DWORD dwArgc, LPTSTR *lpszArgv)
{
    // TO_DO: Declare and set any required variables.
    //   Be sure to periodically call ReportSvcStatus() with 
    //   SERVICE_START_PENDING. If initialization fails, call
    //   ReportSvcStatus with SERVICE_STOPPED.

    // Create an event. The control handler function, SvcCtrlHandler,
    // signals this event when it receives the stop control code.

    ghSvcStopEvent = CreateEvent(
                         NULL,    // default security attributes
                         TRUE,    // manual reset event
                         FALSE,   // not signaled
                         NULL);   // no name

    if ( ghSvcStopEvent == NULL)
    {
        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }

    // Report running status when initialization is complete.

    ReportSvcStatus( SERVICE_RUNNING, NO_ERROR, 0 );

    // TO_DO: Perform work until service stops.

    while(1)
    {
        // Check whether to stop the service.

        WaitForSingleObject(ghSvcStopEvent, INFINITE);

        ReportSvcStatus( SERVICE_STOPPED, NO_ERROR, 0 );
        return;
    }
}

//
// Purpose: 
//   Sets the current service status and reports it to the SCM.
//
// Parameters:
//   dwCurrentState - The current state (see SERVICE_STATUS)
//   dwWin32ExitCode - The system error code
//   dwWaitHint - Estimated time for pending operation, 
//     in milliseconds
// 
// Return value:
//   None
//
VOID ReportSvcStatus( DWORD dwCurrentState,
                      DWORD dwWin32ExitCode,
                      DWORD dwWaitHint)
{
    static DWORD dwCheckPoint = 1;

    // Fill in the SERVICE_STATUS structure.

    gSvcStatus.dwCurrentState = dwCurrentState;
    gSvcStatus.dwWin32ExitCode = dwWin32ExitCode;
    gSvcStatus.dwWaitHint = dwWaitHint;

    if (dwCurrentState == SERVICE_START_PENDING)
        gSvcStatus.dwControlsAccepted = 0;
    else gSvcStatus.dwControlsAccepted = SERVICE_ACCEPT_STOP;

    if ( (dwCurrentState == SERVICE_RUNNING) ||
           (dwCurrentState == SERVICE_STOPPED) )
        gSvcStatus.dwCheckPoint = 0;
    else gSvcStatus.dwCheckPoint = dwCheckPoint++;

    // Report the status of the service to the SCM.
    SetServiceStatus( gSvcStatusHandle, &gSvcStatus );
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Service ServiceMain-Funktion](service-servicemain-function.md)
</dt> <dt>

[Beispiel für den vollständigen Dienst](the-complete-service-sample.md)
</dt> </dl>

 

 
