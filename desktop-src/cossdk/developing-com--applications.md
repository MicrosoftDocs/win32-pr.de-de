---
description: Beim Entwickeln von com+-Anwendungen umfassen die Hauptaufgaben das Entwerfen von COM-Komponenten, um Anwendungslogik zu kapseln und diese Komponenten in eine COM+-Anwendung zu integrieren, die COM+-Anwendung zu erstellen und die Anwendung durch Bereitstellung und Wartung zu verwalten.
ms.assetid: 8c6ec901-1eeb-46b0-8a3a-26d8eff99f6d
title: Entwickeln von com+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee6495b7d8f7b2cc059b113f4250042cfd59b99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523243"
---
# <a name="developing-com-applications"></a><span data-ttu-id="63b51-103">Entwickeln von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="63b51-103">Developing COM+ Applications</span></span>

<span data-ttu-id="63b51-104">Beim Entwickeln von com+-Anwendungen umfassen die Hauptaufgaben das Entwerfen von COM-Komponenten, um Anwendungslogik zu kapseln und diese Komponenten in eine COM+-Anwendung zu integrieren, die COM+-Anwendung zu erstellen und die Anwendung durch Bereitstellung und Wartung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="63b51-104">When developing COM+ applications, the principal tasks include designing COM components to encapsulate application logic and integrating these components into a COM+ application, creating the COM+ application, and administering the application through deployment and maintenance.</span></span>

## <a name="designing-com-components"></a><span data-ttu-id="63b51-105">Entwerfen von COM-Komponenten</span><span class="sxs-lookup"><span data-stu-id="63b51-105">Designing COM Components</span></span>

<span data-ttu-id="63b51-106">In den folgenden Schritten wird ein allgemeines Verfahren für einen guten Komponenten Entwurf beschrieben:</span><span class="sxs-lookup"><span data-stu-id="63b51-106">The following steps describe a general procedure for good component design:</span></span>

1.  <span data-ttu-id="63b51-107">Definieren Sie die com-Klassen und Implementierungsklassen.</span><span class="sxs-lookup"><span data-stu-id="63b51-107">Define the COM classes and implementation classes.</span></span>
2.  <span data-ttu-id="63b51-108">Gruppieren Sie die Klassen in Komponenten.</span><span class="sxs-lookup"><span data-stu-id="63b51-108">Group the classes into components.</span></span>
3.  <span data-ttu-id="63b51-109">Wählen Sie den Satz der com+-Dienste für die Komponente aus, auch wenn Sie beim Entwickeln der Komponente nicht alle angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="63b51-109">Select the set of COM+ services for your component, even if you do not specify all of them when developing the component.</span></span> <span data-ttu-id="63b51-110">Diese Dienste können später mithilfe des Verwaltungs Programms Komponenten Dienste oder des com+-Verwaltungs Objektmodells angegeben werden (Weitere Informationen zum com+-Verwaltungs Objektmodell finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md) ).</span><span class="sxs-lookup"><span data-stu-id="63b51-110">These services can later be specified using the Component Services administrative tool or the COM+ administration object model (See [Automating COM+ Administration](automating-com--administration.md) for more information about the COM+ administration object model.)</span></span>

## <a name="creating-the-com-application"></a><span data-ttu-id="63b51-111">Erstellen der com+-Anwendung</span><span class="sxs-lookup"><span data-stu-id="63b51-111">Creating the COM+ Application</span></span>

<span data-ttu-id="63b51-112">Nach dem Entwerfen der COM-Komponenten integriert der Entwickler die Komponenten in eine COM+-Anwendung und konfiguriert die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="63b51-112">After designing the COM components, the developer integrates the components into a COM+ application and configures the application.</span></span> <span data-ttu-id="63b51-113">Die folgenden Schritte beschreiben den Prozess:</span><span class="sxs-lookup"><span data-stu-id="63b51-113">The following steps describe the process:</span></span>

1.  <span data-ttu-id="63b51-114">Integrieren Sie die Komponenten in eine COM+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="63b51-114">Integrate the components into a COM+ application.</span></span> <span data-ttu-id="63b51-115">Sie können die Komponenten in eine vorhandene COM+-Anwendung integrieren oder eine neue (leere) Anwendung für die Komponenten erstellen.</span><span class="sxs-lookup"><span data-stu-id="63b51-115">You can integrate the components into an existing COM+ application or create a new (empty) application for the components.</span></span> <span data-ttu-id="63b51-116">(Siehe [Erstellen von com+-Anwendungen](creating-com--applications.md).)</span><span class="sxs-lookup"><span data-stu-id="63b51-116">(See [Creating COM+ Applications](creating-com--applications.md).)</span></span>
2.  <span data-ttu-id="63b51-117">Geben Sie den richtigen Satz von Attributen für jede der Klassen an (sofern vorhanden, und, wenn Sie im Entwicklungs Tool nicht angegeben sind).</span><span class="sxs-lookup"><span data-stu-id="63b51-117">Specify the correct set of attributes for each of the classes (if any, and if not specified in the development tool).</span></span> <span data-ttu-id="63b51-118">Diese Attribute geben die Komponenten Abhängigkeiten von allen COM+-Diensten, die ihre Implementierung unterstützen könnte (z. b. Transaktionen, in der Warteschlange befindliche Komponenten, Sicherheit, Objekt Pooling und Just-in-Time-Aktivierung), aus.</span><span class="sxs-lookup"><span data-stu-id="63b51-118">These attributes express the components dependencies on any COM+ services its implementation might rely on (for example, transactions, Queued Components, Security, Object Pooling, and Just-in-Time Activation).</span></span>
3.  <span data-ttu-id="63b51-119">Einrichten des Sicherheits Frameworks (Rollen und Zuweisung von Rollen für Klassen, Schnittstellen und Methoden).</span><span class="sxs-lookup"><span data-stu-id="63b51-119">Set up the security framework (roles and assignment of roles to classes, interfaces, and methods).</span></span>
4.  <span data-ttu-id="63b51-120">Konfigurieren Sie Umgebungs spezifische Attribute für Klassen und Anwendungen (z. b. die standardmäßige Objekt Pool Größe).</span><span class="sxs-lookup"><span data-stu-id="63b51-120">Configure environment-specific attributes on classes and applications (the default object pool size, for example).</span></span> <span data-ttu-id="63b51-121">Diese Umgebungs spezifischen Attribute können später vom Systemadministrator festgelegt (oder geändert) werden.</span><span class="sxs-lookup"><span data-stu-id="63b51-121">These environment-specific attributes can later be set (or modified) by the system administrator.</span></span>
5.  <span data-ttu-id="63b51-122">Exportieren Sie die Anwendung für die Verteilung und Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="63b51-122">Export the application for redistribution and deployment.</span></span>

<span data-ttu-id="63b51-123">Ausführlichere Informationen zu den Schritten beim Entwerfen verteilter Anwendungen finden Sie unter [Entwerfen von com+-Anwendungen](designing-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="63b51-123">For more detailed information on the steps in designing distributed applications, see [Designing COM+ Applications](designing-com--applications.md).</span></span>

## <a name="administering-com-applications"></a><span data-ttu-id="63b51-124">Verwalten von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="63b51-124">Administering COM+ Applications</span></span>

<span data-ttu-id="63b51-125">In der Regel stellt ein Entwickler dem Systemadministrator eine teilweise konfigurierte COM+-Anwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="63b51-125">Typically, a developer delivers a partially configured COM+ application to the system administrator.</span></span> <span data-ttu-id="63b51-126">Der Administrator kann die Anwendung dann für eine oder mehrere bestimmte Umgebungen anpassen (z. b. durch Hinzufügen von Benutzerkonten in Rollen und Servernamen in einem Anwendungs Cluster).</span><span class="sxs-lookup"><span data-stu-id="63b51-126">The administrator can then customize the application for one or more specific environments (for example, by adding user accounts in roles and server names in an application cluster).</span></span> <span data-ttu-id="63b51-127">Die Aufgaben des Administrators umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="63b51-127">The administrator's tasks include the following:</span></span>

-   <span data-ttu-id="63b51-128">Die teilweise konfigurierte COM+-Anwendung wird auf einem administrativen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="63b51-128">Installing the partially configured COM+ application on an administrative computer.</span></span>
-   <span data-ttu-id="63b51-129">Bereitstellen von Umgebungs spezifischen Attributen, z. b. Rollen Mitgliedern und Größe des Objekt Pools.</span><span class="sxs-lookup"><span data-stu-id="63b51-129">Providing environment-specific attributes, such as role members and object pool size.</span></span>
-   <span data-ttu-id="63b51-130">Erneutes Exportieren der vollständig konfigurierten COM+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="63b51-130">Re-exporting the fully configured COM+ application.</span></span>
-   <span data-ttu-id="63b51-131">Erstellen eines Anwendungs Proxys (wenn ein Remote Zugriff auf die Anwendung möglich ist).</span><span class="sxs-lookup"><span data-stu-id="63b51-131">Creating an application proxy (if the application is to be accessed remotely).</span></span>

<span data-ttu-id="63b51-132">Nachdem eine Anwendung vollständig für eine bestimmte Umgebung konfiguriert wurde, kann Sie vom Administrator auf Test-oder Produktions Computern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="63b51-132">After an application is fully configured for a specific environment, the administrator can then deploy it on test or production machines.</span></span> <span data-ttu-id="63b51-133">Dies umfasst die Installation der vollständig konfigurierten COM+-Anwendung auf einem oder mehreren Computern.</span><span class="sxs-lookup"><span data-stu-id="63b51-133">This involves installing the fully configured COM+ application on one or more computers.</span></span>

<span data-ttu-id="63b51-134">Ausführliche Informationen zu com+-Verwaltungsverfahren finden Sie im Verwaltungs Programmkomponenten Dienste.</span><span class="sxs-lookup"><span data-stu-id="63b51-134">For detailed information on COM+ administration procedures, see the Component Services administrative tool.</span></span>

 

 



