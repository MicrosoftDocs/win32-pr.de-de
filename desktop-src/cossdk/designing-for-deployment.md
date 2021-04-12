---
description: Entwerfen für die Bereitstellung
ms.assetid: 31244998-34f5-4fd8-95f6-adcc134bcaf3
title: Entwerfen für die Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e60ac561bd05d08253433e52c7f00c2def54df3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483046"
---
# <a name="designing-for-deployment"></a><span data-ttu-id="2dce6-103">Entwerfen für die Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="2dce6-103">Designing for Deployment</span></span>

<span data-ttu-id="2dce6-104">Die Planung des Umfangs der com+-Anwendungen ist eine wichtige Entwurfs Aufgabe, die Sie frühzeitig in Erwägung gezogen sollten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-104">Planning the scope of COM+ applications is an important design task you should consider early on.</span></span> <span data-ttu-id="2dce6-105">Verteilte Systeme, die mit com+ ausgeführt werden sollen, sollten für die Bereitstellung mit der geringsten Menge an einzelner Konfiguration und der optimalen Verwendung der einzelnen Prozesse konzipiert werden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-105">Distributed systems that are intended to run using COM+ should be designed for deployment with the least amount of individual configuration and to most efficiently use each process.</span></span> <span data-ttu-id="2dce6-106">Es gibt auch Techniken, die Sie verwenden können, mit denen Sie bei der Bereitstellung einer COM+-Anwendung eine optimale Leistung erzielen können.</span><span class="sxs-lookup"><span data-stu-id="2dce6-106">There are also techniques you can use that will enable you to achieve optimal performance when deploying a COM+ application.</span></span> <span data-ttu-id="2dce6-107">(Weitere Informationen finden Sie unter Bereitstellen [für schnellere Kommunikation](deploying-for-faster-communication.md).)</span><span class="sxs-lookup"><span data-stu-id="2dce6-107">(For more information, see [Deploying for Faster Communication](deploying-for-faster-communication.md).)</span></span>

<span data-ttu-id="2dce6-108">Wenn die COM+-Anwendung mit dem Verwaltungs Programmkomponenten Dienste angezeigt wird, wird Sie als Ordner angezeigt, in dem Gruppen von Komponenten logisch gruppiert sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-108">When viewed with the Component Services administrative tool, each COM+ application appears as a folder within which sets of components are logically grouped.</span></span> <span data-ttu-id="2dce6-109">Während Sie einzelne Komponenten zwischen com+-Anwendungs **Komponenten** Ordnern (also von einer Anwendung in eine andere Anwendung) verschieben können, können sich mehrere auf der com+-Anwendungsebene festgelegte Dienste, wie z. b. die Sicherheit, unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="2dce6-109">While you can move individual components between COM+ application **Components** folders (in other words, from one application to another), several services set at the COM+ application level, such as security, may differ.</span></span> <span data-ttu-id="2dce6-110">Diese Dienst Einstellungen können die Portabilität beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-110">These service settings can affect portability.</span></span>

## <a name="a-com-server-application-defines-a-process-boundary"></a><span data-ttu-id="2dce6-111">Eine com+-Server Anwendung definiert eine Prozess Grenze.</span><span class="sxs-lookup"><span data-stu-id="2dce6-111">A COM+ Server Application Defines a Process Boundary</span></span>

<span data-ttu-id="2dce6-112">Wenn Sie eine neue COM+-Serveranwendung erstellen, definieren Sie wirklich eine neue Prozess Grenze.</span><span class="sxs-lookup"><span data-stu-id="2dce6-112">When you create a new COM+ server application, you are really defining a new process boundary.</span></span> <span data-ttu-id="2dce6-113">(Beachten Sie die Ausnahme für Bibliotheksanwendungen, die unten erläutert werden.) Dieser Prozess wird zur steuernden Anwendungs Instanz für die Komponenten, die in der com+-Anwendung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-113">(Note the exception for library applications explained below.) This process becomes the controlling application instance for the components that are contained in the COM+ application.</span></span> <span data-ttu-id="2dce6-114">Diese Komponenten werden alle Prozess Weise in einer neuen Instanz des ausführbaren com+-Programms ausgeführt, wenn ein Programm zum ersten Mal eine COM+-Anwendung aufruft.</span><span class="sxs-lookup"><span data-stu-id="2dce6-114">These components all run in-process in a new instance of the COM+ executable program whenever a program calls into a COM+ application for the first time.</span></span> <span data-ttu-id="2dce6-115">Dies bedeutet, dass alle Komponenten innerhalb eines **bestimmten Ordners der** com+-Anwendung in einem einzelnen Prozessbereich ausgeführt werden, der als DCOM-Server fungiert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-115">This means that all of the components within a given COM+ application's **Components** folder run in a single process space that serves as the DCOM server.</span></span> <span data-ttu-id="2dce6-116">In der com+-Anwendung verwaltet com+ den Arbeitsspeicher, die Koordination mit dem Distributed Transaction Coordinator (DTC), die Just-in-Time-Komponenten Instanzen Aktivierung, die Absturz Erkennung und-Wiederherstellung sowie die rollenbasierte Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="2dce6-116">Within the COM+ application, COM+ manages memory, coordination with the Distributed Transaction Coordinator (DTC), just-in-time component instance activation, crash detection and recovery, and role-based security.</span></span>

## <a name="calling-across-com-application-boundaries"></a><span data-ttu-id="2dce6-117">Aufrufen über com+-Anwendungsgrenzen hinweg</span><span class="sxs-lookup"><span data-stu-id="2dce6-117">Calling Across COM+ Application Boundaries</span></span>

<span data-ttu-id="2dce6-118">Da jede com+-Anwendung normalerweise als separate ausführbare Datei implementiert ist, führt die Aufteilung einer verteilten Anwendung über mehrere COM+-Anwendungen zu Prozess externen com-aufrufen, wenn Komponenten in einer COM+-Anwendung die Komponenten in einer anderen COM+-Anwendung aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-118">Because each COM+ application normally is implemented as a separate executable, the effect of splitting a distributed application across multiple COM+ applications introduces out-of-process COM calls when components in one COM+ application call the components in another COM+ application.</span></span> <span data-ttu-id="2dce6-119">Dadurch wird die Leistungsminderung aufgrund der zusätzlichen Belastung durch das Marshalling von com-Parametern in Prozessen beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="2dce6-119">This introduces performance degradation due to the extra burden that marshaling COM parameters across processes imposes.</span></span>

> [!Note]  
> <span data-ttu-id="2dce6-120">Es gibt keinerlei falsche Probleme mit dieser Leistungs Einbuße. Sie müssen nur beachten, dass es passiert.</span><span class="sxs-lookup"><span data-stu-id="2dce6-120">There is nothing inherently wrong with incurring this performance penalty; you just need to be aware that it is going to occur.</span></span> <span data-ttu-id="2dce6-121">Abhängig von der erforderlichen Antwortzeit, der Anzahl der Benutzer, die gleichzeitig Unternehmens Dienste anfordern, und der zusätzlichen Start Belastung, die jede Komponente zu den einzelnen com+-Anwendungen hinzufügt, können Sie feststellen, dass die Leistungseinbußen, die auf Anwendungsübergreifende Aufrufe zurückzuführen sind, akzeptabel sind.</span><span class="sxs-lookup"><span data-stu-id="2dce6-121">Depending on the required response time, the number of users that will simultaneously request business services, and the added start-up burden that each component adds to each COM+ application, you may find that the performance hit attributable to cross-application calls is acceptable.</span></span>

 

<span data-ttu-id="2dce6-122">Eine Möglichkeit, mit der die Leistungseinbußen beim Aufrufen von com+-Anwendungsgrenzen vermieden werden, besteht darin, eine bestimmte COM+-Anwendung als Bibliotheks Anwendung zu markieren.</span><span class="sxs-lookup"><span data-stu-id="2dce6-122">One possibility that eliminates the performance penalty of calling across COM+ application boundaries is to mark a given COM+ application as a library application.</span></span> <span data-ttu-id="2dce6-123">Eine COM+-Bibliotheks Anwendung wird im Prozess des Clients ausgeführt, von dem Sie erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2dce6-123">A COM+ library application runs in the process of the client that creates it.</span></span> <span data-ttu-id="2dce6-124">Natürlich hat keine Leistungssteigerung Kosten.</span><span class="sxs-lookup"><span data-stu-id="2dce6-124">Of course, no performance gain has zero cost.</span></span> <span data-ttu-id="2dce6-125">In diesem Fall umfasst der Kompromiss die Einschränkungen der COM+-Bibliotheksanwendungen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-125">In this case, the trade-off involves the limitations of COM+ library applications.</span></span> <span data-ttu-id="2dce6-126">Obwohl eine Bibliotheks Anwendung rollenbasierte Sicherheit verwenden kann, kann Sie in der Warteschlange befindliche Komponenten oder den Remote Zugriff nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2dce6-126">While a library application can use role-based security, it cannot support queued components or remote access.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2dce6-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2dce6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2dce6-128">Bereitstellen für schnellere Kommunikation</span><span class="sxs-lookup"><span data-stu-id="2dce6-128">Deploying for Faster Communication</span></span>](deploying-for-faster-communication.md)
</dt> <dt>

[<span data-ttu-id="2dce6-129">Entwerfen für Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="2dce6-129">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="2dce6-130">Entwerfen von Skalierbarkeit</span><span class="sxs-lookup"><span data-stu-id="2dce6-130">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="2dce6-131">Entwerfen für Sicherheit</span><span class="sxs-lookup"><span data-stu-id="2dce6-131">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



