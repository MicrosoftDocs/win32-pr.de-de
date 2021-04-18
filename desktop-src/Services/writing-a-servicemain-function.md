---
description: Die svcmain-Funktion im folgenden Beispiel ist die ServiceMain-Funktion für den Beispiel Dienst.
ms.assetid: 7aa9371d-676c-4633-9831-edf0e74d15f0
title: Schreiben einer ServiceMain-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad3e947c356bad6c6d54395a671aa192c93de1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339778"
---
# <a name="writing-a-servicemain-function"></a>Schreiben einer ServiceMain-Funktion

Die svcmain-Funktion im folgenden Beispiel ist die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion für den Beispiel Dienst. Svcmain hat Zugriff auf die Befehlszeilenargumente für den Dienst in der Art und Weise, wie die **Haupt** Funktion einer Konsolenanwendung funktioniert. Der erste Parameter enthält die Anzahl der Argumente, die im zweiten Parameter an den Dienst übergeben werden. Es gibt immer mindestens ein Argument. Der zweite Parameter ist ein Zeiger auf ein Array von Zeichen folgen Zeigern. Das erste Element im-Array ist immer der Dienst Name.

Die svcmain-Funktion ruft zuerst die [**registerservicectrlhandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) -Funktion auf, um die svcctrlhandler-Funktion als [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) des Diensts zu registrieren und die Initialisierung zu beginnen. **Registerservicectrlhandler** sollte die erste nicht fehlerhafte Funktion in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) sein, damit der Dienst das von dieser Funktion zurückgegebene Status Handle zum Aufrufen von [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit dem Status "beendet" aufrufen kann, \_ Wenn ein Fehler auftritt.

Als nächstes Ruft die svcmain-Funktion die reportsvcstatus-Funktion auf, um anzugeben, dass der anfängliche Status Service \_ Start \_ Pending lautet. Während sich der Dienst in diesem Zustand befindet, werden keine Steuerelemente akzeptiert. Um die Logik des Diensts zu vereinfachen, wird empfohlen, dass der Dienst während der Initialisierung keine Steuerelemente akzeptiert.

Schließlich ruft die svcmain-Funktion die svcinit-Funktion auf, um die Dienst spezifische Initialisierung durchzuführen und die vom Dienst auszuführenden Aufgaben zu starten.

Die Beispiel Initialisierungsfunktion svcinit ist ein sehr einfaches Beispiel. Es führt keine komplexeren Initialisierungs Aufgaben aus, z. b. das Erstellen zusätzlicher Threads. Es wird ein Ereignis erstellt, das der Dienst Steuerungs Handler signalisieren kann, um anzugeben, dass der Dienst beendet werden soll. Anschließend wird reportsvcstatus aufgerufen, um anzugeben, dass der Dienst den Zustand "wird ausgeführt" aufweist \_ . An diesem Punkt hat der Dienst seine Initialisierung abgeschlossen und ist bereit, Steuerelemente zu akzeptieren. Um eine optimale Systemleistung zu erzielen, sollte Ihre Anwendung innerhalb von 25-100 Millisekunden den Status "wird ausgeführt" aufweisen.

Da dieser Beispiel Dienst keine echten Aufgaben durchführt, wartet svcinit einfach darauf, dass das Dienst Beendigungs Ereignis signalisiert wird, indem die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion aufgerufen wird, und ruft reportsvcstatus auf, um anzugeben, dass der Dienst den Status "beendet" eingegeben hat \_ , und gibt zurück. (Beachten Sie, dass es wichtig ist, dass die Funktion zurückgegeben wird, anstatt die [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) -Funktion aufzurufen, da die Rückgabe von die Bereinigung des für die Argumente zugeordneten Arbeitsspeichers ermöglicht.) Sie können zusätzliche Bereinigungs Aufgaben ausführen, indem Sie die [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) -Funktion anstelle von **WaitForSingleObject** verwenden. Der Thread, der die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion ausgeführt wird, wird beendet, der Dienst selbst wird jedoch weiterhin ausgeführt. Wenn der Dienst Steuerungs Handler das Ereignis signalisiert, führt ein Thread aus dem Thread Pool ihren Rückruf aus, um den zusätzlichen Cleanup auszuführen, einschließlich der Einstellung, dass der Dienst \_ beendet wurde.

Beachten Sie, dass in diesem Beispiel svkreportevent verwendet wird, um Fehlerereignisse in das Ereignisprotokoll zu schreiben. Den Quellcode für svkreportevent finden Sie unter [svc. cpp](svc-cpp.md). Ein Beispiel für eine Steuerelement Handler-Funktion finden Sie unter [Schreiben einer steuerungshandlerfunktion](writing-a-control-handler-function.md).

In diesem Beispiel werden die folgenden globalen Definitionen verwendet.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Das folgende Beispiel Fragment stammt aus dem Complete Service Sample.


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

[ServiceMain-Dienstfunktion](service-servicemain-function.md)
</dt> <dt>

[Das Complete Service-Beispiel](the-complete-service-sample.md)
</dt> </dl>

 

 
