---
description: Eine Anwendung, die mindestens eine in der Warteschlange befindliche Komponente enthält, kann mithilfe des Verwaltungs Programms Komponenten Dienste als in die Warteschlange eingereiht gekennzeichnet werden.
ms.assetid: 7d9fec63-0bb7-45f3-9d40-736a60d69185
title: Komponenten Warteschlangen erstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc6f6731144a1744a7648d2d3d2bd5c3c4b217b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343171"
---
# <a name="creating-component-queues"></a><span data-ttu-id="2d82d-103">Komponenten Warteschlangen erstellen</span><span class="sxs-lookup"><span data-stu-id="2d82d-103">Creating Component Queues</span></span>

<span data-ttu-id="2d82d-104">Eine Anwendung, die mindestens eine in der Warteschlange befindliche Komponente enthält, kann mithilfe des Verwaltungs Programms Komponenten Dienste als in die Warteschlange eingereiht gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="2d82d-104">An application that contains at least one queuable component can be marked as queued using the component services administrative tool.</span></span>

<span data-ttu-id="2d82d-105">Wenn eine Anwendung als in die Warteschlange eingereiht markiert ist, erstellt com+ automatisch eine Message queuingwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="2d82d-105">When an application is marked as queued, COM+ automatically creates a message queuing queue for it.</span></span> <span data-ttu-id="2d82d-106">Der Warteschlangen Name ist der Name der Anwendung. Wenn der Name der Warteschlange mit dem Namen einer vorhandenen Warteschlange übereinstimmt, verwendet com+ die vorhandene Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2d82d-106">The queue name is the name of the application; if the queue name matches the name of an existing queue, COM+ will use the existing queue.</span></span>

> [!Note]  
> <span data-ttu-id="2d82d-107">Der Message Queuing *pathname* -Parameter ist eine Kombination aus Remote Server Name (RSN) und dem Namen der com+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2d82d-107">The Message Queuing *PathName* parameter is a combination of the Remote Server Name (RSN) and the COM+ application name.</span></span> <span data-ttu-id="2d82d-108">Die RSN bezieht sich auf das Ziel einer Remote Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="2d82d-108">The RSN refers to the target of a remote activation.</span></span> <span data-ttu-id="2d82d-109">Sie geben eine RSN während der Installation einer exportierbaren Client Anwendung auf einem Client Computer an.</span><span class="sxs-lookup"><span data-stu-id="2d82d-109">You specify an RSN during the installation of a client exportable application on a client computer.</span></span> <span data-ttu-id="2d82d-110">Bei der Installation wird die RSN verwendet, um die Aktivierung an einen angegebenen Client Computer weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="2d82d-110">The installation procedure uses the RSN to direct activation to a specified client computer.</span></span> <span data-ttu-id="2d82d-111">Weitere Informationen zu Warteschlangen Namen finden Sie in der Tabelle mit Parametern im Abschnitt "Queue Moniker Parameters" unter [using the Queue Moniker](using-the-queue-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="2d82d-111">For more information about queue names, refer to the table of parameters in the "Queue Moniker Parameters" section in [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="2d82d-112">Verwaltungs Tool für Komponenten Dienste</span><span class="sxs-lookup"><span data-stu-id="2d82d-112">Component Services Administrative Tool</span></span>

<span data-ttu-id="2d82d-113">Führen Sie die folgenden Schritte aus, um eine COM+-Anwendung in der Warteschlange anzugeben:</span><span class="sxs-lookup"><span data-stu-id="2d82d-113">To specify a COM+ application as queued, use the following steps:</span></span>

1.  <span data-ttu-id="2d82d-114">Öffnen Sie in der Konsolen Struktur des Verwaltungs Programms Komponenten Dienste unter **Komponenten Dienste** den Ordner **com+-Anwendungen** , der dem Computer zugeordnet ist, den Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="2d82d-114">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="2d82d-115">Klicken Sie mit der rechten Maustaste auf die Anwendung, für die Sie eine Warteschlange erstellen möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="2d82d-115">Right-click the application for which you wish to create a queue, and then click **Properties**.</span></span>

3.  <span data-ttu-id="2d82d-116">Wählen Sie **im Dialog** Feldeigenschaften die Registerkarte Queue aus.</span><span class="sxs-lookup"><span data-stu-id="2d82d-116">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="2d82d-117">Aktivieren Sie das Kontrollkästchen mit der Bezeichnung Queue **– diese Anwendung kann durch MSMQ-Warteschlangen erreicht werden**.</span><span class="sxs-lookup"><span data-stu-id="2d82d-117">Activate the check box labeled **Queued – This application can be reached by MSMQ queues**.</span></span>

    > [!Note]  
    > <span data-ttu-id="2d82d-118">Wenn das Kontrollkästchen in der Warteschlange deaktiviert ist, enthält die Anwendung keine Komponenten, die in die Warteschlange **eingereiht** werden können.</span><span class="sxs-lookup"><span data-stu-id="2d82d-118">If the **Queued** check box is grayed out, the application contains no queuable components.</span></span>

     

5.  <span data-ttu-id="2d82d-119">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d82d-119">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="2d82d-120">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2d82d-120">Visual Basic</span></span>

<span data-ttu-id="2d82d-121">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2d82d-121">Does not apply.</span></span>

## <a name="cc"></a><span data-ttu-id="2d82d-122">C/C++</span><span class="sxs-lookup"><span data-stu-id="2d82d-122">C/C++</span></span>

<span data-ttu-id="2d82d-123">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2d82d-123">Does not apply.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d82d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d82d-124">Remarks</span></span>

<span data-ttu-id="2d82d-125">Warteschlangen, die von der com+-Verwaltungs Bibliothek oder dem Verwaltungs Programmkomponenten Dienste erstellt wurden, sind mit dem Message Queuing Transaktions Attribut markiert.</span><span class="sxs-lookup"><span data-stu-id="2d82d-125">Queues created by the COM+ Administration Library or the Component Services administrative tool are marked with the Message Queuing transactional attribute.</span></span>

<span data-ttu-id="2d82d-126">Nachdem eine in der Warteschlange befindliche Anwendung auf dem Server installiert wurde, kann Sie den Clients durch Exportieren der Anwendung und anschließendes Importieren der Anwendung auf jedem Client zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2d82d-126">After a queued application is installed at the server, it can be made available to clients by exporting the application and then importing the application at each client.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d82d-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d82d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d82d-128">Erstellen von Warteschlangen fähigen Komponenten</span><span class="sxs-lookup"><span data-stu-id="2d82d-128">Creating Queuable Components</span></span>](creating-queuable-components.md)
</dt> <dt>

[<span data-ttu-id="2d82d-129">Architektur der Warteschlangen Komponenten</span><span class="sxs-lookup"><span data-stu-id="2d82d-129">Queued Components Architecture</span></span>](queued-components-architecture.md)
</dt> </dl>

 

 



