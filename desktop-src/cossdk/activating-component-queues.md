---
description: Komponenten Warteschlangen
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Komponenten Warteschlangen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393053"
---
# <a name="activating-component-queues"></a><span data-ttu-id="4fe3b-103">Komponenten Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="4fe3b-103">Activating Component Queues</span></span>

<span data-ttu-id="4fe3b-104">Durch das Ausführen von Methoden aufrufen für eine in der Warteschlange befindliche Komponente wird die Methode nicht direkt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-104">Making method calls on a queued component does not directly execute the method.</span></span> <span data-ttu-id="4fe3b-105">Stattdessen [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshallt und speichert Methodenaufrufe und Parameter in einer Warteschlange, in der Sie später von der in der Warteschlange befindlichen Komponente abgerufen und ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-105">Rather, [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) marshals and stores method calls and parameters in a queue where they are later retrieved and executed by the queued component.</span></span> <span data-ttu-id="4fe3b-106">Im Gegensatz zum Aktivieren eines Remote-DCOM-Objekts wird die in der Warteschlange befindliche Komponente nicht instanziiert, wenn eine-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-106">Unlike activating a remote DCOM object, the queued component is not instantiated when a method is called.</span></span> <span data-ttu-id="4fe3b-107">Dies ist die grundlegende Idee der Verwendung von in der Warteschlange befindlichen Komponenten – in der Warteschlange befindliche Komponenten müssen nicht gleichzeitig mit der aufrufenden Anwendung instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-107">This is the basic idea behind using queued components—queued components need not be instantiated at the same time as the calling application.</span></span>

> [!Note]  
> <span data-ttu-id="4fe3b-108">In den Beschreibungen zum Aktivieren einer Anwendung in der Warteschlange wird davon ausgegangen, dass die Anwendung als in die Warteschlange eingereiht und das Kontrollkästchen Listener aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-108">The descriptions for activating a queued application assume that the application is marked as queued and that the listener check box is enabled.</span></span>

 

<span data-ttu-id="4fe3b-109">Sie können Skripts verwenden, um eine Anwendung in der Warteschlange zu starten und zu starten.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-109">You can use scripting to start and stop a queued application.</span></span> <span data-ttu-id="4fe3b-110">Sie können das Skript unter dem Steuerelement des Aufgaben Planers ablegen, um es bei Bedarf auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-110">You can put the script under the control of the task scheduler to run it as required.</span></span> <span data-ttu-id="4fe3b-111">Beispielsweise kann das Skript bei einem Systemneustart ausgeführt werden, wenn die Anwendungen dauerhaft verfügbar sein sollen.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-111">For example, the script can be run on system reboot if the applications are to be permanently available.</span></span> <span data-ttu-id="4fe3b-112">Wenn die Anwendung Transaktionen im Batch Modus verarbeiten soll, kann das Skript zu einem bestimmten Zeitpunkt in Verbindung mit einem Skript zum Herunterfahren ausgeführt werden, um sicherzustellen, dass die Batch Verarbeitung zu einem bestimmten Zeitpunkt beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-112">If the application is to process transactions in batch mode, the script can be run at a certain time each day in conjunction with a shutdown script to be sure the batch processing stops at a specific time.</span></span>

## <a name="component-services-administrative-tool"></a><span data-ttu-id="4fe3b-113">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="4fe3b-113">Component Services Administrative Tool</span></span>

<span data-ttu-id="4fe3b-114">Führen Sie die folgenden Schritte aus, um eine Anwendung in der Warteschlange zu starten:</span><span class="sxs-lookup"><span data-stu-id="4fe3b-114">To start a queued application, use the following steps:</span></span>

1.  <span data-ttu-id="4fe3b-115">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-115">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="4fe3b-116">Klicken Sie mit der rechten Maustaste auf die Anwendung, deren Warteschlange Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-116">Right-click the application whose queue you want to activate.</span></span>

3.  <span data-ttu-id="4fe3b-117">Klicken Sie auf **Start**.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-117">Click **Start**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="4fe3b-118">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="4fe3b-118">Visual Basic</span></span>

<span data-ttu-id="4fe3b-119">Weitere Informationen finden Sie im Beispiel comadmincatalog. startapplikation.</span><span class="sxs-lookup"><span data-stu-id="4fe3b-119">See the COMAdminCatalog.StartApplication example.</span></span>

## <a name="cc"></a><span data-ttu-id="4fe3b-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="4fe3b-120">C/C++</span></span>

<span data-ttu-id="4fe3b-121">Weitere Informationen finden Sie im Beispiel [**icomadmincatalog:: startapplikation**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .</span><span class="sxs-lookup"><span data-stu-id="4fe3b-121">See the [**ICOMAdminCatalog::StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fe3b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fe3b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fe3b-123">Verwenden des Warteschlangen Monikers</span><span class="sxs-lookup"><span data-stu-id="4fe3b-123">Using the Queue Moniker</span></span>](using-the-queue-moniker.md)
</dt> </dl>

 

 



