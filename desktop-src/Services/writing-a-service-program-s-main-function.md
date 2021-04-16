---
description: Das folgende Beispiel kann als Einstiegspunkt für ein Dienstprogramm verwendet werden, das einen einzelnen Dienst unterstützt.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Schreiben einer Hauptfunktion für Dienstprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83aa743bfabbeafa2e05818c5bb068a949dce807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525808"
---
# <a name="writing-a-service-programs-main-function"></a>Schreiben der Hauptfunktion eines Dienstprogramms

Die **Haupt** Funktion eines [Dienstprogramms](service-programs.md) Ruft die [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) -Funktion auf, um eine Verbindung mit dem [Dienststeuerungs-Manager (Service Control Manager](service-control-manager.md) , SCM) herzustellen und den steuerungsdispatcherthread zu starten. Der Verteiler Thread Schleifen und wartet auf eingehende Steuerungsanforderungen für die Dienste, die in der dispatchtabelle angegeben sind. Dieser Thread gibt zurück, wenn ein Fehler aufgetreten ist oder alle Dienste im Prozess beendet wurden. Wenn alle Dienste im Prozess beendet wurden, sendet der SCM eine Steuerungs Anforderung an den Verteiler-Thread, der ihn zum Beenden auffordert. Dieser Thread gibt dann vom **StartServiceCtrlDispatcher** -Befehl zurück, und der Prozess kann beendet werden.

In diesem Beispiel werden die folgenden globalen Definitionen verwendet.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Das folgende Beispiel kann als Einstiegspunkt für ein Dienstprogramm verwendet werden, das einen einzelnen Dienst unterstützt. Wenn das Dienstprogramm mehrere Dienste unterstützt, fügen Sie die Namen der zusätzlichen Dienste der Verteilungs Tabelle hinzu, damit Sie vom Verteiler-Thread überwacht werden können.

Die \_ Tmain-Funktion ist der Einstiegspunkt. Die svkreportevent-Funktion schreibt Informationsmeldungen und Fehler in das Ereignisprotokoll. Weitere Informationen zum Schreiben der svcmain-Funktion finden Sie unter [Schreiben einer ServiceMain](writing-a-servicemain-function.md)-Funktion. Weitere Informationen zur svcinstall-Funktion finden Sie unter [Installieren eines Dienstanbieter](installing-a-service.md). Weitere Informationen zum Schreiben der svcctrlhandler-Funktion finden Sie unter [Schreiben einer Steuerelement Handler-Funktion](writing-a-control-handler-function.md). Den gesamten Beispiel Dienst, einschließlich der Quelle für die svdeportevent-Funktion, finden Sie unter [svc. cpp](svc-cpp.md).


```C++
//
// Purpose: 
//   Entry point for the process
//
// Parameters:
//   None
// 
// Return value:
//   None, defaults to 0 (zero)
//
int __cdecl _tmain(int argc, TCHAR *argv[])
{ 
    // If command-line parameter is "install", install the service. 
    // Otherwise, the service is probably being started by the SCM.

    if( lstrcmpi( argv[1], TEXT("install")) == 0 )
    {
        SvcInstall();
        return;
    }

    // TO_DO: Add any additional services for the process to this table.
    SERVICE_TABLE_ENTRY DispatchTable[] = 
    { 
        { SVCNAME, (LPSERVICE_MAIN_FUNCTION) SvcMain }, 
        { NULL, NULL } 
    }; 
 
    // This call returns when the service has stopped. 
    // The process should simply terminate when the call returns.

    if (!StartServiceCtrlDispatcher( DispatchTable )) 
    { 
        SvcReportEvent(TEXT("StartServiceCtrlDispatcher")); 
    } 
} 

```



Im folgenden finden Sie ein Beispiel für "Sample. h", wie vom Nachrichten Compiler generiert. Weitere Informationen finden Sie unter [Sample.MC](sample-mc.md).

``` syntax
 // The following are message definitions.
//
//  Values are 32 bit values layed out as follows:
//
//   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
//   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
//  +---+-+-+-----------------------+-------------------------------+
//  |Sev|C|R|     Facility          |               Code            |
//  +---+-+-+-----------------------+-------------------------------+
//
//  where
//
//      Sev - is the severity code
//
//          00 - Success
//          01 - Informational
//          10 - Warning
//          11 - Error
//
//      C - is the Customer code flag
//
//      R - is a reserved bit
//
//      Facility - is the facility code
//
//      Code - is the facility's status code
//
//
// Define the facility codes
//
#define FACILITY_SYSTEM                  0x0
#define FACILITY_STUBS                   0x3
#define FACILITY_RUNTIME                 0x2
#define FACILITY_IO_ERROR_CODE           0x4


//
// Define the severity codes
//
#define STATUS_SEVERITY_WARNING          0x2
#define STATUS_SEVERITY_SUCCESS          0x0
#define STATUS_SEVERITY_INFORMATIONAL    0x1
#define STATUS_SEVERITY_ERROR            0x3


//
// MessageId: SVC_ERROR
//
// MessageText:
//
//  An error has occurred (%2).
//  
//
#define SVC_ERROR                        ((DWORD)0xC0020001L)
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst Einstiegspunkt](service-entry-point.md)
</dt> <dt>

[Das Complete Service-Beispiel](the-complete-service-sample.md)
</dt> </dl>

 

 



