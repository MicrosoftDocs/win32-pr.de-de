---
description: Com+ bietet ein Verwaltungs Objektmodell, das die gesamte Funktionalität des Verwaltungs Programms Komponenten Dienste verfügbar macht, selbst ein grafisches Front-End, das auf den administrativen Objekten verfasst ist.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatisieren der com+-Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ef3f56da64e442594a7685a77efb9a06e3fe08
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127164"
---
# <a name="automating-com-administration"></a><span data-ttu-id="19afb-103">Automatisieren der com+-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="19afb-103">Automating COM+ Administration</span></span>

<span data-ttu-id="19afb-104">Com+ bietet ein Verwaltungs Objektmodell, das die gesamte Funktionalität des Verwaltungs Programms Komponenten Dienste verfügbar macht, selbst ein grafisches Front-End, das auf den administrativen Objekten verfasst ist.</span><span class="sxs-lookup"><span data-stu-id="19afb-104">COM+ provides an administration object model that exposes all of the functionality of the Component Services administrative tool, itself a graphical front end written on top of the administrative objects.</span></span> <span data-ttu-id="19afb-105">Mithilfe dieser Objekte, die von der Bibliothek für die Verwaltung von Komponenten Diensten (COMAdmin) bereitgestellt werden, können Sie alle Aufgaben in der Verwaltung von com+-Anwendungen und-Diensten automatisieren.</span><span class="sxs-lookup"><span data-stu-id="19afb-105">You can use these objects, supplied by the Component Services Administration (COMAdmin) Library, to automate all tasks in the administration of COM+ applications and services.</span></span>

<span data-ttu-id="19afb-106">Mit den COMAdmin-Objekten können Sie Informationen lesen und schreiben, die im com+-Katalog gespeichert sind, dem zugrunde liegenden Datenspeicher, der alle com+-Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="19afb-106">The COMAdmin objects enable you to read and write information that is stored on the COM+ catalog, the underlying data store that holds all COM+ configuration data.</span></span>

<span data-ttu-id="19afb-107">Mit diesen Objekten können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="19afb-107">You can use these objects to do the following:</span></span>

-   <span data-ttu-id="19afb-108">Erstellen und konfigurieren Sie com+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="19afb-108">Create and configure COM+ applications.</span></span>
-   <span data-ttu-id="19afb-109">Installieren und exportieren Sie vorhandene COM+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="19afb-109">Install and export existing COM+ applications.</span></span>
-   <span data-ttu-id="19afb-110">Installierte COM+-Anwendungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="19afb-110">Manage installed COM+ applications.</span></span>
-   <span data-ttu-id="19afb-111">Verwalten und Konfigurieren von Diensten.</span><span class="sxs-lookup"><span data-stu-id="19afb-111">Manage and configure services.</span></span>
-   <span data-ttu-id="19afb-112">Remote Verwaltung von Komponenten Diensten auf einem anderen Computer.</span><span class="sxs-lookup"><span data-stu-id="19afb-112">Remotely administer Component Services on a different machine.</span></span>

<span data-ttu-id="19afb-113">Sie können die Skript fähigen COMAdmin-Objekte mit einer beliebigen Automatisierungs kompatiblen Sprache verwenden, wie z. b. Microsoft Visual Basic und Visual Basic Skripts.</span><span class="sxs-lookup"><span data-stu-id="19afb-113">You can use the scriptable COMAdmin objects with any Automation-compatible language, such as Microsoft Visual Basic and Visual Basic Script.</span></span> <span data-ttu-id="19afb-114">Sie können entweder Lightweight-Skripts oder allgemeine Verwaltungs Tools entwickeln.</span><span class="sxs-lookup"><span data-stu-id="19afb-114">You can develop either lightweight scripts or general-purpose administration tools.</span></span> <span data-ttu-id="19afb-115">So können Sie z. B. Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="19afb-115">For example, you can do the following:</span></span>

-   <span data-ttu-id="19afb-116">Schreiben Sie Skripts, um routinemäßige administrative Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="19afb-116">Write scripts to perform routine administrative tasks.</span></span>
-   <span data-ttu-id="19afb-117">Schreiben Sie Skripts, um Prozesse bei der Entwicklung von com+-Anwendungen zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="19afb-117">Write scripts to automate processes in the development of COM+ applications.</span></span>
-   <span data-ttu-id="19afb-118">Entwickeln Sie allgemeine Tools zum Verwalten und Überwachen von Komponenten Diensten.</span><span class="sxs-lookup"><span data-stu-id="19afb-118">Develop general-purpose tools for administering and monitoring Component Services.</span></span>
-   <span data-ttu-id="19afb-119">Entwickeln Sie ausführbare Setup Dateien zum Installieren und Bereitstellen der com+-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="19afb-119">Develop setup executables to install and deploy your COM+ application.</span></span>

<span data-ttu-id="19afb-120">Die COMAdmin-Bibliothek bietet Abwärtskompatibilität mit der MTS 2,0-Verwaltungs Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="19afb-120">The COMAdmin Library provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="19afb-121">Der größte vorhandene MTS 2,0-Verwaltungs Code funktioniert trotz einiger Ausnahmen weiterhin.</span><span class="sxs-lookup"><span data-stu-id="19afb-121">Most existing MTS 2.0 administration code will still work, although with some exceptions.</span></span> <span data-ttu-id="19afb-122">(Siehe die [MTS-Verwaltungs Bibliothek](mts-administration-library.md).)</span><span class="sxs-lookup"><span data-stu-id="19afb-122">(See [MTS Administration Library](mts-administration-library.md).)</span></span>

<span data-ttu-id="19afb-123">Um die Verwaltung effektiv zu automatisieren, sollten Sie mit den Verwaltungsaufgaben vertraut sein, die mit dem Verwaltungs Programmkomponenten Dienste ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="19afb-123">To automate administration effectively, you should be familiar with administration tasks as performed with the Component Services administrative tool.</span></span>

<span data-ttu-id="19afb-124">Vollständige Beschreibungen der COMAdmin-Objekte und der entsprechenden Schnittstellen finden Sie in der com+-Referenz Dokumentation für die folgenden Klassen und Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="19afb-124">For full descriptions of the COMAdmin objects and the corresponding interfaces, see the COM+ Reference documentation for the following classes and interfaces:</span></span>

-   [<span data-ttu-id="19afb-125">**Comadmincatalog**</span><span class="sxs-lookup"><span data-stu-id="19afb-125">**COMAdminCatalog**</span></span>](comadmincatalog.md)
-   [<span data-ttu-id="19afb-126">**Comadmincatalogcollection**</span><span class="sxs-lookup"><span data-stu-id="19afb-126">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
-   [<span data-ttu-id="19afb-127">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="19afb-127">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
-   [<span data-ttu-id="19afb-128">**Icomadmincatalog**</span><span class="sxs-lookup"><span data-stu-id="19afb-128">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [<span data-ttu-id="19afb-129">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="19afb-129">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [<span data-ttu-id="19afb-130">**Icatalogcollection**</span><span class="sxs-lookup"><span data-stu-id="19afb-130">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [<span data-ttu-id="19afb-131">**Icatalogobject**</span><span class="sxs-lookup"><span data-stu-id="19afb-131">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

<span data-ttu-id="19afb-132">Die folgenden Themen in diesem Abschnitt bieten eine Übersicht über die Automatisierung der Verwaltung mithilfe der COMAdmin-Objekte:</span><span class="sxs-lookup"><span data-stu-id="19afb-132">The following topics in this section provide an overview for automating administration using the COMAdmin objects:</span></span>

-   [<span data-ttu-id="19afb-133">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="19afb-133">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
-   [<span data-ttu-id="19afb-134">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="19afb-134">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
-   [<span data-ttu-id="19afb-135">Festlegen von Eigenschaften und Speichern von Änderungen am com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="19afb-135">Setting Properties and Saving Changes to the COM+ Catalog</span></span>](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [<span data-ttu-id="19afb-136">Behandeln von com+-Verwaltungsfehlern</span><span class="sxs-lookup"><span data-stu-id="19afb-136">Handling COM+ Administration Errors</span></span>](handling-com--administration-errors.md)
-   [<span data-ttu-id="19afb-137">Com+-Verwaltungsvorgänge in Transaktionen</span><span class="sxs-lookup"><span data-stu-id="19afb-137">COM+ Administration Operations Within Transactions</span></span>](com--administration-operations-within-transactions.md)
-   [<span data-ttu-id="19afb-138">Einführ Endes Beispiel mit dem com+-Verwaltungs Katalog</span><span class="sxs-lookup"><span data-stu-id="19afb-138">Introductory Example Using the COM+ Administration Catalog</span></span>](introductory-example-using-the-com--administration-catalog.md)

 

 



