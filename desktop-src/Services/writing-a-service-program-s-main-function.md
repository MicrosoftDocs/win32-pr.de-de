---
description: Das folgende Beispiel kann als Einstiegspunkt für ein Dienstprogramm verwendet werden, das einen einzelnen Dienst unterstützt.
ms.assetid: 7fdfc20a-9148-4ae1-8101-7a387c0d0edc
title: Schreiben einer Hauptfunktion für Dienstprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e3c519650957f4f27b00ff54864f558cafba3db960f30c0dd20517328f1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117966611"
---
# <a name="writing-a-service-programs-main-function"></a>Schreiben der Hauptfunktion eines Dienstprogramms

Die **Hauptfunktion** eines [Dienstprogramms](service-programs.md) ruft die [**StartServiceCtrlDispatcher-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) auf, um eine Verbindung mit dem [Dienststeuerungs-Manager](service-control-manager.md) (Service Control Manager, SCM) herzustellen und den Steuerungsverteilungsthread zu starten. Der Verteilerthread wartet auf eingehende Steuerungsanforderungen für die in der Dispatchtabelle angegebenen Dienste. Dieser Thread gibt zurück, wenn ein Fehler auftritt oder wenn alle Dienste im Prozess beendet wurden. Wenn alle Dienste im Prozess beendet wurden, sendet der SCM eine Steuerungsanforderung an den Verteilerthread, der ihn angibt, dass er beendet werden soll. Dieser Thread gibt dann vom **StartServiceCtrlDispatcher-Aufruf** zurück, und der Prozess kann beendet werden.

In diesem Beispiel werden die folgenden globalen Definitionen verwendet.


```C++
#define SVCNAME TEXT("SvcName")

SERVICE_STATUS          gSvcStatus; 
SERVICE_STATUS_HANDLE   gSvcStatusHandle; 
HANDLE                  ghSvcStopEvent = NULL;
```



Das folgende Beispiel kann als Einstiegspunkt für ein Dienstprogramm verwendet werden, das einen einzelnen Dienst unterstützt. Wenn Ihr Dienstprogramm mehrere Dienste unterstützt, fügen Sie der Dispatchtabelle die Namen der zusätzlichen Dienste hinzu, damit sie vom Verteilerthread überwacht werden können.

Die \_ tmain-Funktion ist der Einstiegspunkt. Die SvcReportEvent-Funktion schreibt Informationsmeldungen und Fehler in das Ereignisprotokoll. Informationen zum Schreiben der SvcMain-Funktion finden Sie unter [Schreiben einer ServiceMain-Funktion.](writing-a-servicemain-function.md) Weitere Informationen zur SvcInstall-Funktion finden Sie unter [Installieren eines Diensts.](installing-a-service.md) Informationen zum Schreiben der SvcCtrlHandler-Funktion finden Sie unter [Schreiben einer Steuerelementhandlerfunktion.](writing-a-control-handler-function.md) Den vollständigen Beispieldienst, einschließlich der Quelle für die SvcReportEvent-Funktion, finden Sie unter [Svc.cpp.](svc-cpp.md)


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



Es folgt ein Beispiel für "Sample.h", das vom Nachrichtencompiler generiert wird. Weitere Informationen finden Sie unter [Sample.mc](sample-mc.md).

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

[Diensteinstiegspunkt](service-entry-point.md)
</dt> <dt>

[Beispiel für den vollständigen Dienst](the-complete-service-sample.md)
</dt> </dl>

 

 



