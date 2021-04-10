---
description: Dienste werden im Allgemeinen als Konsolen Anwendungen geschrieben.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Dienst Einstiegspunkt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958864"
---
# <a name="service-entry-point"></a><span data-ttu-id="409af-103">Dienst Einstiegspunkt</span><span class="sxs-lookup"><span data-stu-id="409af-103">Service Entry Point</span></span>

<span data-ttu-id="409af-104">Dienste werden im Allgemeinen als Konsolen Anwendungen geschrieben.</span><span class="sxs-lookup"><span data-stu-id="409af-104">Services are generally written as console applications.</span></span> <span data-ttu-id="409af-105">Der Einstiegspunkt einer Konsolenanwendung ist die **Haupt** Funktion.</span><span class="sxs-lookup"><span data-stu-id="409af-105">The entry point of a console application is its **main** function.</span></span> <span data-ttu-id="409af-106">Die **Main** -Funktion empfängt Argumente aus dem **ImagePath** -Wert aus dem Registrierungsschlüssel für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="409af-106">The **main** function receives arguments from the **ImagePath** value from the registry key for the service.</span></span> <span data-ttu-id="409af-107">Weitere Informationen finden Sie im Abschnitt "Hinweise" der Funktion "| [**ateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ".</span><span class="sxs-lookup"><span data-stu-id="409af-107">For more information, see the Remarks section of the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span>

<span data-ttu-id="409af-108">Wenn der SCM ein Dienstprogramm startet, wartet er darauf, dass er die Funktion " [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="409af-108">When the SCM starts a service program, it waits for it to call the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function.</span></span> <span data-ttu-id="409af-109">Verwenden Sie die folgenden Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="409af-109">Use the following guidelines.</span></span>

-   <span data-ttu-id="409af-110">Ein Dienst vom Typ "Dienst \_ Win32- \_ eigener Prozess" \_ sollte [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) direkt aus seinem Haupt Thread aufrufen.</span><span class="sxs-lookup"><span data-stu-id="409af-110">A service of type SERVICE\_WIN32\_OWN\_PROCESS should call [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) immediately, from its main thread.</span></span> <span data-ttu-id="409af-111">Sie können nach dem Starten des Diensts eine beliebige Initialisierung ausführen, wie in der [Service Main-Funktion des Diensts](service-servicemain-function.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="409af-111">You can perform any initialization after the service starts, as described in [Service ServiceMain Function](service-servicemain-function.md).</span></span>
-   <span data-ttu-id="409af-112">Wenn der Diensttyp ein \_ Win32-Freigabeprozess des Diensts ist \_ \_ und eine allgemeine Initialisierung für alle Dienste im Programm vorhanden ist, können Sie die Initialisierung im Haupt Thread ausführen, bevor Sie [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)aufrufen, solange Sie weniger als 30 Sekunden benötigt.</span><span class="sxs-lookup"><span data-stu-id="409af-112">If the service type is SERVICE\_WIN32\_SHARE\_PROCESS and there is common initialization for all services in the program, you can perform the initialization in the main thread before calling [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera), as long as it takes less than 30 seconds.</span></span> <span data-ttu-id="409af-113">Andernfalls müssen Sie einen weiteren Thread erstellen, um die allgemeine Initialisierung durchzuführen, während der Haupt Thread **StartServiceCtrlDispatcher** aufruft.</span><span class="sxs-lookup"><span data-stu-id="409af-113">Otherwise, you must create another thread to do the common initialization, while the main thread calls **StartServiceCtrlDispatcher**.</span></span> <span data-ttu-id="409af-114">Nach dem Starten des Diensts sollten Sie weiterhin eine beliebige Dienst spezifische Initialisierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="409af-114">You should still perform any service-specific initialization after the service starts.</span></span>

<span data-ttu-id="409af-115">Die [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) -Funktion nimmt für jeden Dienst, der im Prozess enthalten ist, eine [**Dienst \_ Tabellen \_ Eintrags**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) Struktur.</span><span class="sxs-lookup"><span data-stu-id="409af-115">The [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function takes a [**SERVICE\_TABLE\_ENTRY**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) structure for each service contained in the process.</span></span> <span data-ttu-id="409af-116">Jede Struktur gibt den Dienstnamen und den Einstiegspunkt für den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="409af-116">Each structure specifies the service name and the entry point for the service.</span></span> <span data-ttu-id="409af-117">Ein Beispiel finden Sie unter [Schreiben der Hauptfunktion eines Dienstprogramms](writing-a-service-program-s-main-function.md).</span><span class="sxs-lookup"><span data-stu-id="409af-117">For an example, see [Writing a Service Program's main Function](writing-a-service-program-s-main-function.md).</span></span>

<span data-ttu-id="409af-118">Wenn [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) erfolgreich ist, gibt der aufrufende Thread erst dann zurück, wenn alle laufenden Dienste im Prozess den Status "beendet" eingegeben haben \_ .</span><span class="sxs-lookup"><span data-stu-id="409af-118">If [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) succeeds, the calling thread does not return until all running services in the process have entered the SERVICE\_STOPPED state.</span></span> <span data-ttu-id="409af-119">Der SCM sendet Steuerungsanforderungen über eine Named Pipe an diesen Thread.</span><span class="sxs-lookup"><span data-stu-id="409af-119">The SCM sends control requests to this thread through a named pipe.</span></span> <span data-ttu-id="409af-120">Der Thread fungiert als Steuerelement Verteiler und führt die folgenden Aufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="409af-120">The thread acts as a control dispatcher, performing the following tasks:</span></span>

-   <span data-ttu-id="409af-121">Erstellen Sie einen neuen Thread, um den entsprechenden Einstiegspunkt aufzurufen, wenn ein neuer Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="409af-121">Create a new thread to call the appropriate entry point when a new service is started.</span></span>
-   <span data-ttu-id="409af-122">Ruft die entsprechende [Handlerfunktion](service-control-handler-function.md) auf, um Dienst Steuerungsanforderungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="409af-122">Call the appropriate [handler function](service-control-handler-function.md) to handle service control requests.</span></span>

## <a name="related-topics"></a><span data-ttu-id="409af-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="409af-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="409af-124">Schreiben der Hauptfunktion eines Dienstprogramms</span><span class="sxs-lookup"><span data-stu-id="409af-124">Writing a Service Program's main Function</span></span>](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



