---
description: Wenn eine Handler-Funktion vom Verteilerthread aufgerufen wird, verarbeitet sie den im Opcode-Parameter übergebenen Steuerungscode und ruft dann die ReportSvcStatus-Funktion auf, um den Dienststatus zu aktualisieren.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Schreiben einer Steuerelementhandlerfunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bf8ab32edb73fdf11f3f0370a512b17b143b8af219a2bd539e59bdf062a00d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888061"
---
# <a name="writing-a-control-handler-function"></a>Schreiben einer Steuerelementhandlerfunktion

Wenn eine [**Handler-Funktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) vom Verteilerthread aufgerufen wird, verarbeitet sie den im *Opcode-Parameter* übergebenen Steuerungscode und ruft dann die ReportSvcStatus-Funktion auf, um den Dienststatus zu aktualisieren. Wenn eine [**Handler-Funktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) einen Steuerelementcode empfängt, sollte sie den Dienststatus nur melden, wenn die Behandlung des Steuerungscodes bewirkt, dass sich der Dienststatus ändert. Wenn der Dienst nicht auf das Steuerelement zusteuert, sollte er den Status nicht an den Dienststeuerungs-Manager melden. Den Quellcode für ReportSvcStatus finden Sie unter [Schreiben einer ServiceMain-Funktion.](writing-a-servicemain-function.md)

Im folgenden Beispiel ist die SvcCtrlHandler-Funktion ein Beispiel für eine [**Handler-Funktion.**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) Beachten Sie, dass die variable ghSvcStopEvent eine globale Variable ist, die initialisiert und verwendet werden sollte, wie unter [Schreiben einer ServiceMain-Funktion gezeigt.](writing-a-servicemain-function.md)


```C++
//
// Purpose: 
//   Called by SCM whenever a control code is sent to the service
//   using the ControlService function.
//
// Parameters:
//   dwCtrl - control code
// 
// Return value:
//   None
//
VOID WINAPI SvcCtrlHandler( DWORD dwCtrl )
{
   // Handle the requested control code. 

   switch(dwCtrl) 
   {  
      case SERVICE_CONTROL_STOP: 
         ReportSvcStatus(SERVICE_STOP_PENDING, NO_ERROR, 0);

         // Signal the service to stop.

         SetEvent(ghSvcStopEvent);
         ReportSvcStatus(gSvcStatus.dwCurrentState, NO_ERROR, 0);
         
         return;
 
      case SERVICE_CONTROL_INTERROGATE: 
         break; 
 
      default: 
         break;
   } 
   
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienststeuerungshandler-Funktion](service-control-handler-function.md)
</dt> <dt>

[Das vollständige Dienstbeispiel](the-complete-service-sample.md)
</dt> </dl>

 

 



