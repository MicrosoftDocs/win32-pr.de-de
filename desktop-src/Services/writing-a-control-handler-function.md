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
# <a name="writing-a-control-handler-function"></a><span data-ttu-id="b4879-103">Schreiben einer Steuerelement Handler-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4879-103">Writing a Control Handler Function</span></span>

<span data-ttu-id="b4879-104">Wenn eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) vom Verteiler Thread aufgerufen wird, verarbeitet Sie den im *Opcode* -Parameter übergebenen Steuerungs Code und ruft dann die reportsvcstatus-Funktion auf, um den Dienststatus zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b4879-104">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function is called by the dispatcher thread, it handles the control code passed in the *Opcode* parameter and then calls the ReportSvcStatus function to update the service status.</span></span> <span data-ttu-id="b4879-105">Wenn eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) einen Steuerungs Code empfängt, sollte Sie den Dienststatus nur melden, wenn die Behandlung des Steuerungs Codes bewirkt, dass der Dienststatus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="b4879-105">When a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function receives a control code, it should report the service status only if handling the control code causes the service status to change.</span></span> <span data-ttu-id="b4879-106">Wenn der Dienst nicht auf das Steuerelement reagiert, sollte er dem Dienststeuerungs-Manager keinen Status melden.</span><span class="sxs-lookup"><span data-stu-id="b4879-106">If the service does not act on the control, it should not report status to the service control manager.</span></span> <span data-ttu-id="b4879-107">Den Quellcode für reportsvcstatus finden Sie unter [Schreiben einer ServiceMain-Funktion](writing-a-servicemain-function.md).</span><span class="sxs-lookup"><span data-stu-id="b4879-107">For the source code for ReportSvcStatus, see [Writing a ServiceMain Function](writing-a-servicemain-function.md).</span></span>

<span data-ttu-id="b4879-108">Im folgenden Beispiel ist die svcctrlhandler-Funktion ein Beispiel für eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) .</span><span class="sxs-lookup"><span data-stu-id="b4879-108">In the following example, the SvcCtrlHandler function is an example of a [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) function.</span></span> <span data-ttu-id="b4879-109">Beachten Sie, dass die Variable "ghsvcstopevent" eine globale Variable ist, die initialisiert und verwendet werden sollte, wie in [Schreiben einer ServiceMain-Funktion](writing-a-servicemain-function.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b4879-109">Note that the ghSvcStopEvent variable is a global variable that should be initialized and used as demonstrated in [Writing a ServiceMain function](writing-a-servicemain-function.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b4879-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b4879-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4879-111">Dienststeuerungshandler-Funktion</span><span class="sxs-lookup"><span data-stu-id="b4879-111">Service Control Handler Function</span></span>](service-control-handler-function.md)
</dt> <dt>

[<span data-ttu-id="b4879-112">Das Complete Service-Beispiel</span><span class="sxs-lookup"><span data-stu-id="b4879-112">The Complete Service Sample</span></span>](the-complete-service-sample.md)
</dt> </dl>

 

 



