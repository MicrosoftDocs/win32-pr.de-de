---
description: Wenn eine Handlerfunktion vom Verteiler Thread aufgerufen wird, verarbeitet Sie den im Opcode-Parameter übergebenen Steuerungs Code und ruft dann die reportsvcstatus-Funktion auf, um den Dienststatus zu aktualisieren.
ms.assetid: bf1932bd-496b-46a1-95f4-1581da98299f
title: Schreiben einer Steuerelement Handler-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724a04aa20143d2c4a506da7ac17119388a8c82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346922"
---
# <a name="writing-a-control-handler-function"></a>Schreiben einer Steuerelement Handler-Funktion

Wenn eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) vom Verteiler Thread aufgerufen wird, verarbeitet Sie den im *Opcode* -Parameter übergebenen Steuerungs Code und ruft dann die reportsvcstatus-Funktion auf, um den Dienststatus zu aktualisieren. Wenn eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) einen Steuerungs Code empfängt, sollte Sie den Dienststatus nur melden, wenn die Behandlung des Steuerungs Codes bewirkt, dass der Dienststatus geändert wird. Wenn der Dienst nicht auf das Steuerelement reagiert, sollte er dem Dienststeuerungs-Manager keinen Status melden. Den Quellcode für reportsvcstatus finden Sie unter [Schreiben einer ServiceMain-Funktion](writing-a-servicemain-function.md).

Im folgenden Beispiel ist die svcctrlhandler-Funktion ein Beispiel für eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) . Beachten Sie, dass die Variable "ghsvcstopevent" eine globale Variable ist, die initialisiert und verwendet werden sollte, wie in [Schreiben einer ServiceMain-Funktion](writing-a-servicemain-function.md)veranschaulicht.


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

[Das Complete Service-Beispiel](the-complete-service-sample.md)
</dt> </dl>

 

 



