---
description: Um Steuerungsanforderungen an einen laufenden Dienst zu senden, verwendet ein Dienst Steuerungsprogramm die ControlService-Funktion.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Dienst Steuerungsanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346508"
---
# <a name="service-control-requests"></a><span data-ttu-id="4121a-103">Dienst Steuerungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="4121a-103">Service Control Requests</span></span>

<span data-ttu-id="4121a-104">Um Steuerungsanforderungen an einen laufenden Dienst zu senden, verwendet ein Dienst Steuerungsprogramm die [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4121a-104">To send control requests to a running service, a service control program uses the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="4121a-105">Diese Funktion gibt einen Steuerelement Wert an, der an die [**handlerex**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) -Funktion des angegebenen Dienstanbieter übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="4121a-105">This function specifies a control value that is passed to the [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) function of the specified service.</span></span> <span data-ttu-id="4121a-106">Bei diesem Steuerungs Wert kann es sich um einen benutzerdefinierten Code handeln, oder es kann sich um einen der Standard Codes handeln, die dem aufrufenden Programm das Ausführen der folgenden Aktionen ermöglichen:</span><span class="sxs-lookup"><span data-stu-id="4121a-106">This control value can be a user-defined code, or it can be one of the standard codes that enable the calling program to perform the following actions:</span></span>

-   <span data-ttu-id="4121a-107">Beendet einen Dienst (Dienst \_ Steuerungs \_ Ende).</span><span class="sxs-lookup"><span data-stu-id="4121a-107">Stop a service (SERVICE\_CONTROL\_STOP).</span></span>
-   <span data-ttu-id="4121a-108">Hält einen Dienst an (Anhalten der Dienst \_ Steuerung \_ ).</span><span class="sxs-lookup"><span data-stu-id="4121a-108">Pause a service (SERVICE\_CONTROL\_PAUSE).</span></span>
-   <span data-ttu-id="4121a-109">Fortsetzen der Ausführung eines angehaltenen Dienstanbieter (Dienst \_ Steuerung \_ fortsetzen).</span><span class="sxs-lookup"><span data-stu-id="4121a-109">Resume executing a paused service (SERVICE\_CONTROL\_CONTINUE).</span></span>
-   <span data-ttu-id="4121a-110">Abrufen aktualisierter Statusinformationen von einem Dienst ( \_ Dienststeuerungs- \_ Abfrage).</span><span class="sxs-lookup"><span data-stu-id="4121a-110">Retrieve updated status information from a service (SERVICE\_CONTROL\_INTERROGATE).</span></span>

<span data-ttu-id="4121a-111">Jeder Dienst gibt die Steuerungs Werte an, die er akzeptiert und verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4121a-111">Each service specifies the control values that it will accept and process.</span></span> <span data-ttu-id="4121a-112">Wenn Sie bestimmen möchten, welche der Standard Steuerelement Werte von einem Dienst akzeptiert werden, verwenden Sie die Funktion [**QueryServiceStatus usex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) , oder geben Sie den \_ Wert des Dienststeuerungs- \_ Abfrage Steuer Elements in einem Aufrufen der [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) -Funktion an.</span><span class="sxs-lookup"><span data-stu-id="4121a-112">To determine which of the standard control values are accepted by a service, use the [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function or specify the SERVICE\_CONTROL\_INTERROGATE control value in a call to the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function.</span></span> <span data-ttu-id="4121a-113">Der **dwcontrolsaccepted** -Member der [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur, die von diesen Funktionen zurückgegeben wird, gibt an, ob der Dienst beendet, angehalten oder fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4121a-113">The **dwControlsAccepted** member of the [**SERVICE\_STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) structure returned by these functions indicates whether the service can be stopped, paused, or resumed.</span></span> <span data-ttu-id="4121a-114">Alle Dienste akzeptieren den \_ Wert der Dienststeuerungs- \_ Abfrage Steuerung.</span><span class="sxs-lookup"><span data-stu-id="4121a-114">All services accept the SERVICE\_CONTROL\_INTERROGATE control value.</span></span>

<span data-ttu-id="4121a-115">Die Funktion [**queryservicestatusex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) meldet den aktuellen Status für einen angegebenen Dienst, erhält aber keinen aktualisierten Status vom Dienst selbst.</span><span class="sxs-lookup"><span data-stu-id="4121a-115">The [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function reports the most recent status for a specified service, but does not get an updated status from the service itself.</span></span> <span data-ttu-id="4121a-116">Durch die Verwendung des Dienstkontroll-Steuerelement-Steuerelement- \_ \_ Steuer Elements in einem Befehl von [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) wird sichergestellt, dass die zurückgegebenen Statusinformationen aktuell</span><span class="sxs-lookup"><span data-stu-id="4121a-116">Using the SERVICE\_CONTROL\_INTERROGATE control value in a call to [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) ensures that the status information returned is current.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4121a-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4121a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4121a-118">Steuern eines Dienstanbieter mit SC</span><span class="sxs-lookup"><span data-stu-id="4121a-118">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



