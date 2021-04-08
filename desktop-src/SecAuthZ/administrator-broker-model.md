---
description: Die Anwendung ist in zwei Programme unterteilt. Eines der Programme wird als Standardbenutzer ausgeführt, und die andere wird mit Administrator Berechtigungen ausgeführt.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Administrator Broker Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865999"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="f633a-104">Administrator Broker Modell</span><span class="sxs-lookup"><span data-stu-id="f633a-104">Administrator Broker Model</span></span>

<span data-ttu-id="f633a-105">Im Administrator Broker Modell ist die Anwendung in zwei Programme unterteilt.</span><span class="sxs-lookup"><span data-stu-id="f633a-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="f633a-106">Eines der Programme wird als Standardbenutzer ausgeführt, und die andere wird mit Administrator Berechtigungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f633a-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="f633a-107">Markieren Sie mithilfe eines Anwendungs Manifests das Standardbenutzer Programm mit dem **requestedExecutionLevel-Wert** **asInvoker** , und markieren Sie das administrative Programm mit dem **requestedExecutionLevel-Wert** " **requilesministrator**".</span><span class="sxs-lookup"><span data-stu-id="f633a-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="f633a-108">Ein Benutzer wird zuerst das Standardbenutzer Programm starten.</span><span class="sxs-lookup"><span data-stu-id="f633a-108">A user launches the standard user program first.</span></span> <span data-ttu-id="f633a-109">Wenn der Benutzer versucht, einen Vorgang auszuführen, der ein vollständiges Administrator Zugriffs Token erfordert, ruft das Standardbenutzer Programm die [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) -Funktion auf, um das administrative Programm zu starten.</span><span class="sxs-lookup"><span data-stu-id="f633a-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="f633a-110">Die **ShellExecute** -Funktion fordert den Benutzer zur Genehmigung auf, bevor die Anwendung mit dem vollständigen Administrator Zugriffs Token des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f633a-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="f633a-111">Das administrative Programm kann dann Aufgaben ausführen, für die Administratorrechte erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f633a-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="f633a-112">Das administrative Programm ist nicht vollständig vom Standardbenutzer Programm isoliert.</span><span class="sxs-lookup"><span data-stu-id="f633a-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="f633a-113">Das administrative Programm kann die prozessübergreifende Kommunikation mit dem Standardbenutzer Programm aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f633a-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="f633a-114">Diese Kommunikation wird jedoch durch die standardmäßige obligatorische Integritätsrichtlinie eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="f633a-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="f633a-115">Informationen zu obligatorischen Integritäts Überlegungen finden [Sie unter Entwerfen von Anwendungen für die Durchführung mit niedriger Integritäts Stufe](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="f633a-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="f633a-116">Für das Modell des Administrator Brokers können folgende Verwendungsmöglichkeiten verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f633a-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="f633a-117">Entwickeln von Assistenten.</span><span class="sxs-lookup"><span data-stu-id="f633a-117">Developing wizards.</span></span> <span data-ttu-id="f633a-118">Wenn ein Hardware-Assistent feststellt, dass ein erforderlicher Treiber nicht auf dem Computer installiert ist oder sich am genehmigten Standort des Unternehmens befindet, wird eine Anwendung mit erhöhten Rechten aufgerufen, die die Möglichkeit zum Verschieben eines Treibers in den Computerspeicher hat.</span><span class="sxs-lookup"><span data-stu-id="f633a-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="f633a-119">Autorun.exe Aufrufen von Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="f633a-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="f633a-120">Wenn ein Benutzer die Software von einer CD ausführt, wird Autorun.exe, der als Standardbenutzer ausgeführt wird, Setup.exe, der als Administrator ausgeführt wird, gestartet, um die Software auf dem Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="f633a-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="f633a-121">Die Verwendung des Administrator Broker Modells hat folgende Nachteile:</span><span class="sxs-lookup"><span data-stu-id="f633a-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="f633a-122">Die Übergänge von Anwendung zu Anwendung können für den Benutzer verwirrend sein.</span><span class="sxs-lookup"><span data-stu-id="f633a-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="f633a-123">Es kann schwierig sein, den Benutzer zu informieren, warum eine neue Anwendung auf dem Monitor angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f633a-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="f633a-124">Es kann schwierig sein, Zustandsinformationen zwischen den beiden Anwendungen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="f633a-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="f633a-125">Beispielsweise können Sie dieses Modell nicht verwenden, um Zustandsinformationen zwischen einer Standardbenutzer-Systemsteuerung (CPL) und Ihrem Administrator Pendant zu übergeben, um der gleichen cpl die Administrator-und Standardbenutzer Funktionalität zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f633a-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="f633a-126">Der Standardbenutzer-cpl muss seinen Zustand irgendwo speichern.</span><span class="sxs-lookup"><span data-stu-id="f633a-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="f633a-127">Beim Aufteilen der Funktionalität zwischen zwei Programmen kann viel replizierter Code vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f633a-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f633a-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f633a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f633a-129">Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="f633a-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="f633a-130">COM-Objektmodell für Administratoren</span><span class="sxs-lookup"><span data-stu-id="f633a-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="f633a-131">Betriebs System-Dienstmodell</span><span class="sxs-lookup"><span data-stu-id="f633a-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="f633a-132">Modell mit erhöhten Rechten</span><span class="sxs-lookup"><span data-stu-id="f633a-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
