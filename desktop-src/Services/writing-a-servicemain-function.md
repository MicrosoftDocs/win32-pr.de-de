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
# <a name="writing-a-servicemain-function"></a><span data-ttu-id="4994a-103">Schreiben einer ServiceMain-Funktion</span><span class="sxs-lookup"><span data-stu-id="4994a-103">Writing a ServiceMain Function</span></span>

<span data-ttu-id="4994a-104">Die svcmain-Funktion im folgenden Beispiel ist die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion für den Beispiel Dienst.</span><span class="sxs-lookup"><span data-stu-id="4994a-104">The SvcMain function in the following example is the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function for the example service.</span></span> <span data-ttu-id="4994a-105">Svcmain hat Zugriff auf die Befehlszeilenargumente für den Dienst in der Art und Weise, wie die **Haupt** Funktion einer Konsolenanwendung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="4994a-105">SvcMain has access to the command-line arguments for the service in the way that the **main** function of a console application does.</span></span> <span data-ttu-id="4994a-106">Der erste Parameter enthält die Anzahl der Argumente, die im zweiten Parameter an den Dienst übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="4994a-106">The first parameter contains the number of arguments being passed to the service in the second parameter.</span></span> <span data-ttu-id="4994a-107">Es gibt immer mindestens ein Argument.</span><span class="sxs-lookup"><span data-stu-id="4994a-107">There will always be at least one argument.</span></span> <span data-ttu-id="4994a-108">Der zweite Parameter ist ein Zeiger auf ein Array von Zeichen folgen Zeigern.</span><span class="sxs-lookup"><span data-stu-id="4994a-108">The second parameter is a pointer to an array of string pointers.</span></span> <span data-ttu-id="4994a-109">Das erste Element im-Array ist immer der Dienst Name.</span><span class="sxs-lookup"><span data-stu-id="4994a-109">The first item in the array is always the service name.</span></span>

<span data-ttu-id="4994a-110">Die svcmain-Funktion ruft zuerst die [**registerservicectrlhandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) -Funktion auf, um die svcctrlhandler-Funktion als [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) des Diensts zu registrieren und die Initialisierung zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="4994a-110">The SvcMain function first calls the [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) function to register the SvcCtrlHandler function as the service's [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function and begin initialization.</span></span> <span data-ttu-id="4994a-111">**Registerservicectrlhandler** sollte die erste nicht fehlerhafte Funktion in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) sein, damit der Dienst das von dieser Funktion zurückgegebene Status Handle zum Aufrufen von [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) mit dem Status "beendet" aufrufen kann, \_ Wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="4994a-111">**RegisterServiceCtrlHandler** should be the first nonfailing function in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) so the service can use the status handle returned by this function to call [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) with the SERVICE\_STOPPED state if an error occurs.</span></span>

<span data-ttu-id="4994a-112">Als nächstes Ruft die svcmain-Funktion die reportsvcstatus-Funktion auf, um anzugeben, dass der anfängliche Status Service \_ Start \_ Pending lautet.</span><span class="sxs-lookup"><span data-stu-id="4994a-112">Next, the SvcMain function calls the ReportSvcStatus function to indicate that its initial status is SERVICE\_START\_PENDING.</span></span> <span data-ttu-id="4994a-113">Während sich der Dienst in diesem Zustand befindet, werden keine Steuerelemente akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4994a-113">While the service is in this state, no controls are accepted.</span></span> <span data-ttu-id="4994a-114">Um die Logik des Diensts zu vereinfachen, wird empfohlen, dass der Dienst während der Initialisierung keine Steuerelemente akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="4994a-114">To simplify the logic of the service, it is recommended that the service not accept any controls while it is performing its initialization.</span></span>

<span data-ttu-id="4994a-115">Schließlich ruft die svcmain-Funktion die svcinit-Funktion auf, um die Dienst spezifische Initialisierung durchzuführen und die vom Dienst auszuführenden Aufgaben zu starten.</span><span class="sxs-lookup"><span data-stu-id="4994a-115">Finally, the SvcMain function calls the SvcInit function to perform the service-specific initialization and begin the work to be performed by the service.</span></span>

<span data-ttu-id="4994a-116">Die Beispiel Initialisierungsfunktion svcinit ist ein sehr einfaches Beispiel. Es führt keine komplexeren Initialisierungs Aufgaben aus, z. b. das Erstellen zusätzlicher Threads.</span><span class="sxs-lookup"><span data-stu-id="4994a-116">The sample initialization function, SvcInit, is a very simple example; it does not perform more complex initialization tasks such as creating additional threads.</span></span> <span data-ttu-id="4994a-117">Es wird ein Ereignis erstellt, das der Dienst Steuerungs Handler signalisieren kann, um anzugeben, dass der Dienst beendet werden soll. Anschließend wird reportsvcstatus aufgerufen, um anzugeben, dass der Dienst den Zustand "wird ausgeführt" aufweist \_ .</span><span class="sxs-lookup"><span data-stu-id="4994a-117">It creates an event that the service control handler can signal to indicate that the service should stop, then calls ReportSvcStatus to indicate that the service has entered the SERVICE\_RUNNING state.</span></span> <span data-ttu-id="4994a-118">An diesem Punkt hat der Dienst seine Initialisierung abgeschlossen und ist bereit, Steuerelemente zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="4994a-118">At this point, the service has completed its initialization and is ready to accept controls.</span></span> <span data-ttu-id="4994a-119">Um eine optimale Systemleistung zu erzielen, sollte Ihre Anwendung innerhalb von 25-100 Millisekunden den Status "wird ausgeführt" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4994a-119">For best system performance, your application should enter the running state within 25-100 milliseconds.</span></span>

<span data-ttu-id="4994a-120">Da dieser Beispiel Dienst keine echten Aufgaben durchführt, wartet svcinit einfach darauf, dass das Dienst Beendigungs Ereignis signalisiert wird, indem die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion aufgerufen wird, und ruft reportsvcstatus auf, um anzugeben, dass der Dienst den Status "beendet" eingegeben hat \_ , und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="4994a-120">Because this sample service does not complete any real tasks, SvcInit simply waits for the service stop event to be signaled by calling the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function, calls ReportSvcStatus to indicate that the service has entered the SERVICE\_STOPPED state, and returns.</span></span> <span data-ttu-id="4994a-121">(Beachten Sie, dass es wichtig ist, dass die Funktion zurückgegeben wird, anstatt die [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) -Funktion aufzurufen, da die Rückgabe von die Bereinigung des für die Argumente zugeordneten Arbeitsspeichers ermöglicht.) Sie können zusätzliche Bereinigungs Aufgaben ausführen, indem Sie die [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) -Funktion anstelle von **WaitForSingleObject** verwenden.</span><span class="sxs-lookup"><span data-stu-id="4994a-121">(Note that it is important for the function to return, rather than call the [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) function, because returning allows for cleanup of the memory allocated for the arguments.) You can perform additional cleanup tasks by using the [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) function instead of **WaitForSingleObject**.</span></span> <span data-ttu-id="4994a-122">Der Thread, der die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion ausgeführt wird, wird beendet, der Dienst selbst wird jedoch weiterhin ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4994a-122">The thread that is running the [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function terminates, but the service itself continues to run.</span></span> <span data-ttu-id="4994a-123">Wenn der Dienst Steuerungs Handler das Ereignis signalisiert, führt ein Thread aus dem Thread Pool ihren Rückruf aus, um den zusätzlichen Cleanup auszuführen, einschließlich der Einstellung, dass der Dienst \_ beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="4994a-123">When the service control handler signals the event, a thread from the thread pool executes your callback to perform the additional cleanup, including setting the status to SERVICE\_STOPPED.</span></span>

<span data-ttu-id="4994a-124">Beachten Sie, dass in diesem Beispiel svkreportevent verwendet wird, um Fehlerereignisse in das Ereignisprotokoll zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="4994a-124">Note that this example uses SvcReportEvent to write error events to the event log.</span></span> <span data-ttu-id="4994a-125">Den Quellcode für svkreportevent finden Sie unter [svc. cpp](svc-cpp.md).</span><span class="sxs-lookup"><span data-stu-id="4994a-125">For the source code for SvcReportEvent, see [Svc.cpp](svc-cpp.md).</span></span> <span data-ttu-id="4994a-126">Ein Beispiel für eine Steuerelement Handler-Funktion finden Sie unter [Schreiben einer steuerungshandlerfunktion](writing-a-control-handler-function.md).</span><span class="sxs-lookup"><span data-stu-id="4994a-126">For an example control handler function, see [Writing a Control Handler Function](writing-a-control-handler-function.md).</span></span>

<span data-ttu-id="4994a-127">In diesem Beispiel werden die folgenden globalen Definitionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4994a-127">The following global definitions are used in this sample.</span></span>


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



<span data-ttu-id="4994a-128">Das folgende Beispiel Fragment stammt aus dem Complete Service Sample.</span><span class="sxs-lookup"><span data-stu-id="4994a-128">The following sample fragment is taken from the complete service sample.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4994a-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4994a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4994a-130">ServiceMain-Dienstfunktion</span><span class="sxs-lookup"><span data-stu-id="4994a-130">Service ServiceMain Function</span></span>](service-servicemain-function.md)
</dt> <dt>

[<span data-ttu-id="4994a-131">Das Complete Service-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4994a-131">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 
