---
description: Konzepte der com+-Dienst Anwendung
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Konzepte der com+-Dienst Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483067"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="66b37-103">Konzepte der com+-Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="66b37-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="66b37-104">Sie können das Verwaltungs Programmkomponenten Dienste verwenden, um eine COM+-Serveranwendung als Dienst Anwendung zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="66b37-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="66b37-105">Das Ausführen einer COM+-Serveranwendung als Dienst bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="66b37-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="66b37-106">Wenn die Anwendung immer ausgeführt werden muss, kann der Server bei den Komponenten Diensten optional automatisch gestartet werden, und der Server kann bei einem Timeout ebenfalls neu gestartet werden. Wenn beispielsweise ein Computer, auf dem in der Warteschlange befindliche Komponenten Listener-Komponenten ausgeführt werden, neu gestartet wird, können die Listener der in der Warteschlange befindlichen Komponenten automatisch gestartet werden, wenn Sie als Dienst konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="66b37-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="66b37-107">Wenn Ihre Anwendung privilegierte Vorgänge ausführen muss, kann die Anwendung als lokales Systemkonto ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="66b37-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="66b37-108">Nur NT-Dienste können mit dieser Sicherheitsstufe ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="66b37-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="66b37-109">Die Anwendung wird mit dem Windows-Clusterdienst kompatibel sein, das Dienste während des System Failovers verwaltet.</span><span class="sxs-lookup"><span data-stu-id="66b37-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="66b37-110">Wenn andere Dienste als abhängig gekennzeichnet werden müssen, wird diese Option von den Komponenten Diensten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="66b37-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="66b37-111">Wenn Ihre Anwendung z. b. die von einem anderen Dienst bereitgestellte Funktionalität nutzt, wird der als "abhängig" markierte Dienst vor dem Start der Anwendung gestartet.</span><span class="sxs-lookup"><span data-stu-id="66b37-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="66b37-112">Automatisches Starten einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="66b37-112">Starting an Application Automatically</span></span>

<span data-ttu-id="66b37-113">Wenn die COM+-Serveranwendung automatisch gestartet wird, verhält sie sich wie ein Dienst, der es dem Entwickler erfordert, den Server mithilfe des Verwaltungs Tools "Dienste" zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="66b37-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="66b37-114">Sie können auf das Verwaltungs Programm Dienste zugreifen, indem Sie das Verwaltungs Programmkomponenten Dienste starten und dann auf **Dienste (lokal)** klicken.</span><span class="sxs-lookup"><span data-stu-id="66b37-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="66b37-115">Manuelles Starten einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="66b37-115">Starting an Application Manually</span></span>

<span data-ttu-id="66b37-116">Wenn die COM+-Serveranwendung manuell gestartet wird, verhält sie sich wie ein DLL-Host mit den Sicherheitseinstellungen eines Diensts.</span><span class="sxs-lookup"><span data-stu-id="66b37-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="66b37-117">Der Dienst wird manuell gestartet, wenn er aktiviert und automatisch heruntergefahren wird, wenn ein Timeout auftritt.</span><span class="sxs-lookup"><span data-stu-id="66b37-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="66b37-118">Dienstkonfigurationen</span><span class="sxs-lookup"><span data-stu-id="66b37-118">Service Configurations</span></span>

<span data-ttu-id="66b37-119">Unabhängig vom Starttyp kann die Anwendung so konfiguriert werden, dass Sie als lokales Systemkonto ausgeführt oder einem Benutzerkonto zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="66b37-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="66b37-120">Das lokale System und das Benutzerkonto können zum Zeitpunkt der Erstellung des Dienstanbieter konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="66b37-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="66b37-121">Zum Konfigurieren der Sicherheitseinstellungen muss das Verwaltungs Programm Dienste verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66b37-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="66b37-122">Abhängigkeiten können auch für den Dienst festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="66b37-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="66b37-123">Die Anwendung kann auch in einer bestimmten Reihenfolge gestartet werden, indem Abhängigkeiten aus einer Liste anderer Systemdienste ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="66b37-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="66b37-124">Die Systemdienste können z. b. als abhängig gekennzeichnet werden, und die Anwendung wird erst gestartet, wenn die Systemdienste in der angegebenen Reihenfolge gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="66b37-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="66b37-125">Dadurch wird die Dienst Anwendung ordnungsgemäß initialisiert, bevor Sie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66b37-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="66b37-126">Eine Schritt-für-Schritt-Anleitung zum Konfigurieren einer COM+-Anwendung, die als Dienst ausgeführt werden soll, finden Sie unter [Konfigurieren einer com+-Server Anwendung als Dienst Anwendung](configuring-a-com--server-application-as-a-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="66b37-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66b37-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66b37-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66b37-128">Aufgaben der com+-Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="66b37-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 



