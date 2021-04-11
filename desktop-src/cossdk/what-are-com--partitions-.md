---
description: Eine COM+-Partition ist ein logischer Container, der es ermöglicht, Anwendungen unabhängig von anderen Konfigurationen dieser Anwendungen auszuführen.
ms.assetid: c1290d10-968f-44f0-8099-d69c9e706c9e
title: Was sind COM+-Partitionen?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69acdae724bb0c9211d147a985f7571c5e7c052f
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104132125"
---
# <a name="what-are-com-partitions"></a><span data-ttu-id="b1649-103">Was sind COM+-Partitionen?</span><span class="sxs-lookup"><span data-stu-id="b1649-103">What Are COM+ Partitions?</span></span>

<span data-ttu-id="b1649-104">Eine COM+-Partition ist ein logischer Container, der es ermöglicht, Anwendungen unabhängig von anderen Konfigurationen dieser Anwendungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b1649-104">A COM+ partition is a logical container that allows applications to run independently of other configurations of those applications.</span></span> <span data-ttu-id="b1649-105">Jede Konfiguration einer Anwendung wird in einer separaten Partition installiert und kann gemäß den spezifischen Anforderungen Ihrer Benutzer separat verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b1649-105">Each configuration of an application is installed into a separate partition and can be separately managed, according to the specific needs of its users.</span></span>

<span data-ttu-id="b1649-106">Während der Aktivierung einer COM+-Komponente bestimmt der Partitions Dienst, welche Konfiguration der Komponente aktiviert werden soll, basierend auf der Identität des Benutzers, der die Komponenten Aktivierung anfordert.</span><span class="sxs-lookup"><span data-stu-id="b1649-106">During activation of a COM+ component, the partitions service determines which configuration of the component to activate, based on the identity of the user requesting the component activation.</span></span> <span data-ttu-id="b1649-107">Beispielsweise könnte eine einzelne Organisation mit zwei separaten Gruppen, Produktion und Schulung, com+-Partitionen implementieren, damit die beiden Gruppen unterschiedliche Konfigurationen einer COM+-Anwendung auf demselben Computer verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b1649-107">For example, a single organization that has two separate groups, Production and Training, could implement COM+ partitions as a way to allow the two groups to use different configurations of a COM+ application on the same computer.</span></span>

<span data-ttu-id="b1649-108">**Windows XP:** Die Möglichkeit, com+-Partitionen zu erstellen, zu konfigurieren oder zu delegieren, ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1649-108">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="b1649-109">Die globale Partition ist die einzige verfügbare com+-Partition.</span><span class="sxs-lookup"><span data-stu-id="b1649-109">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="b1649-110">**Windows 2000:** Der com+-Partitions Dienst ist in Windows 2000 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1649-110">**Windows 2000:** The COM+ partitions service is not available in Windows 2000.</span></span>

## <a name="benefits-of-using-com-partitions"></a><span data-ttu-id="b1649-111">Vorteile der Verwendung von COM+-Partitionen</span><span class="sxs-lookup"><span data-stu-id="b1649-111">Benefits of Using COM+ Partitions</span></span>

<span data-ttu-id="b1649-112">Die Verwendung von COM+-Partitionen bietet verschiedene Vorteile, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="b1649-112">The use of COM+ partitions offers several advantages, including the following:</span></span>

-   <span data-ttu-id="b1649-113">Organisationen können Ihre Gesamtbetriebskosten (TCO) senken, indem Sie weniger physische Anwendungsserver verwenden, um Benutzer zu unterstützen, die mehrere Anwendungs Konfigurationen benötigen.</span><span class="sxs-lookup"><span data-stu-id="b1649-113">Organizations can lower their total cost of ownership (TCO) by using fewer physical application servers to support users who need multiple application configurations.</span></span>
-   <span data-ttu-id="b1649-114">Der Verwaltungsaufwand wird reduziert.</span><span class="sxs-lookup"><span data-stu-id="b1649-114">Administrative overhead is reduced.</span></span> <span data-ttu-id="b1649-115">Anstatt mehrere Computer konfigurieren und verwalten zu müssen, müssen Administratoren nur mehrere Partitionen auf demselben Computer konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="b1649-115">Instead of having to configure and manage multiple computers, administrators need only configure and manage multiple partitions on the same computer.</span></span> <span data-ttu-id="b1649-116">Darüber hinaus können Partitionen Programm gesteuert durch Hinzufügen einer neuen com+-Programmierschnittstelle verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b1649-116">Furthermore, partitions can be managed programmatically through the addition of a new COM+ programming interface.</span></span>
-   <span data-ttu-id="b1649-117">Die Sicherheit kann für lokale Benutzer, Domänen Benutzer und Organisationseinheiten (OUs) auf Partitions Basis implementiert und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="b1649-117">Security can be implemented and managed on a partition-by-partition basis for local users, domain users, and organizational units (OUs).</span></span>
-   <span data-ttu-id="b1649-118">Programmierer und Administratoren können die Entwicklungs-und Verwaltungs Tools von Microsoft – wie z. b. die Windows SDK, Active Directory Benutzer und Computer und das Verwaltungs Programmkomponenten Dienste – zum Verwalten von COM+-Partitionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1649-118">Programmers and administrators can use Microsoft's development and administrative tools—such as the Windows SDK, Active Directory Users and Computers, and Component Services administrative tool—to manage COM+ partitions.</span></span> <span data-ttu-id="b1649-119">Die Partitions Funktion ist vollständig in diese Tools integriert.</span><span class="sxs-lookup"><span data-stu-id="b1649-119">The partitions feature is fully integrated into these tools.</span></span>

## <a name="primary-usage-scenario"></a><span data-ttu-id="b1649-120">Primäres Verwendungs Szenario</span><span class="sxs-lookup"><span data-stu-id="b1649-120">Primary Usage Scenario</span></span>

<span data-ttu-id="b1649-121">Ein Hauptgrund für die Bereitstellung der com+-Partitions Funktion besteht darin, webbasierte Anwendungen zu hosten.</span><span class="sxs-lookup"><span data-stu-id="b1649-121">A primary reason for customers to deploy the COM+ partitions feature is to host Web-based applications.</span></span> <span data-ttu-id="b1649-122">Nehmen wir beispielsweise an, ein kleines Softwareunternehmen entwickelt eine COM+-Anwendung für die Verwendung durch Krankenhausmitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="b1649-122">For example, suppose a small software company develops a COM+ application for use by hospital personnel.</span></span> <span data-ttu-id="b1649-123">Die Anwendung, die eine verteilte webbasierte Anwendung ist, ermöglicht es Krankenhäusern, Patientendaten Sätze mit einer SQL Server Datenbank zu speichern und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b1649-123">The application, which is a distributed Web-based application, provides a way for hospitals to store and retrieve patient medical records using a SQL Server database.</span></span>

<span data-ttu-id="b1649-124">Angenommen, das Softwareunternehmen hat drei Kunden: Krankenhaus a, Krankenhaus B und Krankenhaus C. Obwohl jeder Kunde die Clientseite der com+-Anwendung lokal auf seinen Desktop Computern ausführt, befindet sich die Serverseite der com+-Anwendung auf dem internen Webserver des Softwareunternehmens und wird von seinen Kunden über das Web aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b1649-124">Suppose the software company has three customers: Hospital A, Hospital B, and Hospital C. While each customer runs the client side of the COM+ application locally on its desktop computers, the server side of the COM+ application resides on the software company's in-house web server and is accessed by its customers via the Web.</span></span>

<span data-ttu-id="b1649-125">Da jedes Krankenhaus über einen eigenen Satz an Speicher-und Abruf Anforderungen und seinen eigenen Satz angepasster Patientendaten verfügt, muss das Softwareunternehmen eine Methode bereitstellen, mit der mehrere Konfigurationen des Server Teils der Anwendung gleichzeitig auf dem Webserver ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b1649-125">Because each hospital has its own set of storage and retrieval requirements and its own set of customized patient data, the software company must provide a way for multiple configurations of the server part of the application to be executed simultaneously on the web server.</span></span> <span data-ttu-id="b1649-126">Com+-Partitionen stellen eine Lösung für dieses Problem dar.</span><span class="sxs-lookup"><span data-stu-id="b1649-126">COM+ partitions provide a solution to this problem.</span></span>

<span data-ttu-id="b1649-127">Die folgende Abbildung zeigt das Partitions Szenario für die COM+-Anwendung des Softwareunternehmens.</span><span class="sxs-lookup"><span data-stu-id="b1649-127">The following illustration shows the partitions scenario for the software company's COM+ application.</span></span>

![Diagramm, das ein Partitions Szenario für eine COM+-Anwendung anzeigt, mit einer Client Anwendung zu Serveranwendung für die SQL Server-Datenbank.](images/c4a96ff9-9afd-43c7-807c-4593cb77f51b.png)

## <a name="related-topics"></a><span data-ttu-id="b1649-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b1649-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1649-130">Einschränkungen beim Anwendungs Entwurf</span><span class="sxs-lookup"><span data-stu-id="b1649-130">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="b1649-131">Komponenten und Partitionen in der com+-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="b1649-131">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="b1649-132">Partitions Implementierung</span><span class="sxs-lookup"><span data-stu-id="b1649-132">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="b1649-133">Registrieren und Aktivieren von Komponenten in Partitionen</span><span class="sxs-lookup"><span data-stu-id="b1649-133">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> </dl>

 

 



