---
description: 'VDS bietet zwei Hilfsobjekte: das-Enumerationsobjekt und das Async-Objekt. In diesem Thema werden die einzelnen Objekte beschrieben und Links zu Beispielen für die Funktionsweise von Aufrufern von Aufrufern bereitstellt.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Hilfsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218501"
---
# <a name="helper-objects"></a><span data-ttu-id="8c823-104">Hilfsobjekte</span><span class="sxs-lookup"><span data-stu-id="8c823-104">Helper Objects</span></span>

<span data-ttu-id="8c823-105">\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]</span><span class="sxs-lookup"><span data-stu-id="8c823-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="8c823-106">VDS bietet zwei Hilfsobjekte: das-Enumerationsobjekt und das Async-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8c823-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="8c823-107">In diesem Thema werden die einzelnen Objekte beschrieben und Links zu Beispielen für die Funktionsweise von Aufrufern von Aufrufern bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8c823-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="8c823-108">Enumerationsobjekt</span><span class="sxs-lookup"><span data-stu-id="8c823-108">Enumeration Object</span></span>

<span data-ttu-id="8c823-109">Ein Enumerationsobjekt listet einen Satz von VDS-Objekten eines bestimmten Typs auf.</span><span class="sxs-lookup"><span data-stu-id="8c823-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="8c823-110">Bei Objekten kann es sich um Anbieter, Subsysteme, Controller, LUNs, LUN-plexes, Laufwerke, Festplatten Pakete, Datenträger, Volumes oder Volumeplexes handeln.</span><span class="sxs-lookup"><span data-stu-id="8c823-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="8c823-111">Aufrufer können einen Zeiger auf ein bestimmtes Objekt erhalten, indem Sie das gewünschte Objekt aus der-Enumeration auswählen, das von der entsprechenden-Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8c823-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="8c823-112">Ein Codebeispiel finden Sie unter [Arbeiten mit enumerationsobjekten](working-with-enumeration-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8c823-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="8c823-113">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8c823-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="8c823-114">type</span><span class="sxs-lookup"><span data-stu-id="8c823-114">Type</span></span>                                              | <span data-ttu-id="8c823-115">Element</span><span class="sxs-lookup"><span data-stu-id="8c823-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="8c823-116">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="8c823-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="8c823-117">**Ienumvdsobject**</span><span class="sxs-lookup"><span data-stu-id="8c823-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="8c823-118">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8c823-118">Associated enumerations</span></span>                           | <span data-ttu-id="8c823-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c823-119">None.</span></span>                                    |
| <span data-ttu-id="8c823-120">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="8c823-120">Associated structures</span></span>                             | <span data-ttu-id="8c823-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c823-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="8c823-122">Async-Objekt</span><span class="sxs-lookup"><span data-stu-id="8c823-122">Async Object</span></span>

<span data-ttu-id="8c823-123">Asynchrone Vorgänge werden von einem Async-Objekt verwaltet.</span><span class="sxs-lookup"><span data-stu-id="8c823-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="8c823-124">Methoden, die asynchrone Vorgänge initiieren, geben einen Zeiger auf eine [**ivdsasync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) -Schnittstelle zurück, die es dem Aufrufer ermöglicht, den Status des asynchronen Vorgangs abzubrechen, zu warten und abzufragen.</span><span class="sxs-lookup"><span data-stu-id="8c823-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="8c823-125">VDS-Vorgänge mit langer Ausführungszeit werden in der Regel asynchron implementiert.</span><span class="sxs-lookup"><span data-stu-id="8c823-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="8c823-126">Die Softwareanbieter Programme Basic und Dynamic implementieren asynchrone Methoden konsistent für Volume-, Partitions-und Datenträger Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="8c823-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="8c823-127">Hardware Anbieter implementieren optional asynchrone Methoden, die asynchron in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="8c823-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="8c823-128">Unabhängig davon, wie der Anbieter die-Methode implementiert, muss der Vorgang einen Zeiger auf eine [**ivdsasync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) -Schnittstelle an den Aufrufer zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8c823-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="8c823-129">Ein Codebeispiel finden Sie unter [Verwalten von asynchronen Vorgängen](managing-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="8c823-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="8c823-130">Zu den asynchronen Vorgängen gehören:</span><span class="sxs-lookup"><span data-stu-id="8c823-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="8c823-131">Erstellen einer LUN, eines Volumes oder einer Partition.</span><span class="sxs-lookup"><span data-stu-id="8c823-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="8c823-132">Formatieren eines Volumes oder einer Partition.</span><span class="sxs-lookup"><span data-stu-id="8c823-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="8c823-133">Hinzufügen oder Entfernen einer LUN oder eines volumeplex.</span><span class="sxs-lookup"><span data-stu-id="8c823-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="8c823-134">Aufteilen eines volumeplex.</span><span class="sxs-lookup"><span data-stu-id="8c823-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="8c823-135">Erweitern oder Verkleinern einer LUN oder eines Volumes.</span><span class="sxs-lookup"><span data-stu-id="8c823-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="8c823-136">Wiederherstellen einer LUN oder eines Volumes.</span><span class="sxs-lookup"><span data-stu-id="8c823-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="8c823-137">Bereinigen eines Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="8c823-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="8c823-138">Ersetzen eines Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="8c823-138">Replacing a disk.</span></span>

<span data-ttu-id="8c823-139">In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8c823-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="8c823-140">type</span><span class="sxs-lookup"><span data-stu-id="8c823-140">Type</span></span>                                              | <span data-ttu-id="8c823-141">Element</span><span class="sxs-lookup"><span data-stu-id="8c823-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="8c823-142">Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden</span><span class="sxs-lookup"><span data-stu-id="8c823-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="8c823-143">**Ivdsasync**</span><span class="sxs-lookup"><span data-stu-id="8c823-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="8c823-144">Zugehörige Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8c823-144">Associated enumerations</span></span>                           | <span data-ttu-id="8c823-145">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c823-145">None.</span></span>                          |
| <span data-ttu-id="8c823-146">Zugeordnete Strukturen</span><span class="sxs-lookup"><span data-stu-id="8c823-146">Associated structures</span></span>                             | <span data-ttu-id="8c823-147">Keine.</span><span class="sxs-lookup"><span data-stu-id="8c823-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="8c823-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c823-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c823-149">VDS-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="8c823-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="8c823-150">**Ivdsasync**</span><span class="sxs-lookup"><span data-stu-id="8c823-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="8c823-151">Arbeiten mit enumerationsobjekten</span><span class="sxs-lookup"><span data-stu-id="8c823-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="8c823-152">Verwalten von asynchronen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="8c823-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 
