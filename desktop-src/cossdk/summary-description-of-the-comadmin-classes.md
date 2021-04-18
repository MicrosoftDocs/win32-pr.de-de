---
description: Es gibt drei Klassen, die von der COMAdmin Library (comadmin.dll) bereitgestellt werden, von denen jede eine com-Dual Schnittstelle implementiert.
ms.assetid: 5a20199f-9d46-4dbe-8e30-2c7ddbde8795
title: Zusammenfassungs Beschreibung der COMAdmin-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d4a2f54f21f89e9bca644006d50f4eec544565c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343596"
---
# <a name="summary-description-of-the-comadmin-classes"></a><span data-ttu-id="0011e-103">Zusammenfassungs Beschreibung der COMAdmin-Klassen</span><span class="sxs-lookup"><span data-stu-id="0011e-103">Summary Description of the COMAdmin Classes</span></span>

<span data-ttu-id="0011e-104">Es gibt drei Klassen, die von der COMAdmin Library (comadmin.dll) bereitgestellt werden, von denen jede eine com-Dual Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="0011e-104">There are three classes provided by the COMAdmin library (comadmin.dll), each of which implements a COM dual interface.</span></span> <span data-ttu-id="0011e-105">Mithilfe von Objekten, die aus diesen Klassen erstellt werden, erhalten Sie Zugriff auf den Katalog, um Auflistungen im Katalog darzustellen und die in Auflistungen enthaltenen Elemente darzustellen.</span><span class="sxs-lookup"><span data-stu-id="0011e-105">You use objects created from these classes to gain access to the catalog, to represent collections in the catalog, and to represent the items contained within collections.</span></span>

## <a name="comadmincatalog"></a><span data-ttu-id="0011e-106">Comadmincatalog</span><span class="sxs-lookup"><span data-stu-id="0011e-106">COMAdminCatalog</span></span>

<span data-ttu-id="0011e-107">Die [**comadmincatalog**](comadmincatalog.md) -Klasse stellt den Katalog selbst dar.</span><span class="sxs-lookup"><span data-stu-id="0011e-107">The [**COMAdminCatalog**](comadmincatalog.md) class represents the catalog itself.</span></span> <span data-ttu-id="0011e-108">Ein aus **comadmincatalog** erstelltes Objekt ist das grundlegende Objekt, das Sie in der programmgesteuerten Verwaltung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0011e-108">An object created from **COMAdminCatalog** is the fundamental object that you use in programmatic administration.</span></span> <span data-ttu-id="0011e-109">Neben dem Einrichten der grundlegenden Verbindung mit dem Katalogserver, wenn Sie ihn instanziieren, stellt **comadmincatalog** Methoden bereit, mit denen Sie die folgenden Aufgaben ausführen können:</span><span class="sxs-lookup"><span data-stu-id="0011e-109">Besides establishing the basic connection with the catalog server when you instantiate it, **COMAdminCatalog** provides methods that enable you to do the following:</span></span>

-   <span data-ttu-id="0011e-110">Sammlungen im Katalog erhalten.</span><span class="sxs-lookup"><span data-stu-id="0011e-110">Get collections on the catalog.</span></span>
-   <span data-ttu-id="0011e-111">Stellen Sie eine Verbindung mit dem Katalogserver auf einem Remote Computer her.</span><span class="sxs-lookup"><span data-stu-id="0011e-111">Connect to the catalog server on a remote machine.</span></span>
-   <span data-ttu-id="0011e-112">Installieren, exportieren, starten, Herunterfahren und Abrufen von Informationen zu com+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="0011e-112">Install, export, start, shut down, and obtain information regarding COM+ applications.</span></span>
-   <span data-ttu-id="0011e-113">Installieren von Komponenten in com+-Anwendungen und Abrufen von Informationen zu Komponenten.</span><span class="sxs-lookup"><span data-stu-id="0011e-113">Install components into COM+ applications and obtain information regarding components.</span></span>
-   <span data-ttu-id="0011e-114">Starten, Abbrechen oder Aktualisieren von Diensten, die auf dem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0011e-114">Start, stop, or refresh services running on the machine.</span></span>
-   <span data-ttu-id="0011e-115">Aktualisieren, wiederherstellen oder Sichern von Katalog Informationen.</span><span class="sxs-lookup"><span data-stu-id="0011e-115">Refresh, restore, or back up catalog information.</span></span>

<span data-ttu-id="0011e-116">In com+ 1,0 implementiert die [**comadmincatalog**](comadmincatalog.md) -Klasse die [**icomadmincatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0011e-116">In COM+ 1.0, the [**COMAdminCatalog**](comadmincatalog.md) class implements the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span> <span data-ttu-id="0011e-117">In com+ 1,5 implementiert die **comadmincatalog** -Klasse [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) als Standardschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0011e-117">In COM+ 1.5, the **COMAdminCatalog** class implements [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) as its default interface.</span></span>

## <a name="comadmincatalogcollection"></a><span data-ttu-id="0011e-118">Comadmincatalogcollection</span><span class="sxs-lookup"><span data-stu-id="0011e-118">COMAdminCatalogCollection</span></span>

<span data-ttu-id="0011e-119">Die [**comadmincatalogcollection**](comadmincatalogcollection.md) -Klasse stellt eine beliebige Auflistung im Katalog dar, indem eine Zeichenfolge bereitgestellt wird, die die jeweilige Auflistung bei der Objekt Instanziierung benennt.</span><span class="sxs-lookup"><span data-stu-id="0011e-119">The [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class represents any collection in the catalog, by supplying a string naming the particular collection at object instantiation time.</span></span> <span data-ttu-id="0011e-120">(Verfügbare Katalog Sammlungen werden in der Tabelle unter [com+-Verwaltungs Sammlungen](com--administration-collections.md)benannt.) Objekte werden aus dieser Klasse erstellt, wenn eine Auflistung der obersten Ebene abgerufen wird, indem die [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode des [**comadmincatalog**](comadmincatalog.md) -Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0011e-120">(Available catalog collections are named in the table at [COM+ Administration Collections](com--administration-collections.md).) Objects are created from this class when retrieving a top-level collection by calling the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method of the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="0011e-121">Diese Objekte werden auch erstellt, wenn eine untergeordnete Auflistung abgerufen wird, indem die **GetCollection** -Methode des übergeordneten Auflistungs Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0011e-121">These objects are also created when retrieving a child collection by calling the **GetCollection** method of its parent collection object.</span></span> <span data-ttu-id="0011e-122">Mit **comadmincatalogcollection** -Objekten können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="0011e-122">**COMAdminCatalogCollection** objects enable you to do the following:</span></span>

-   <span data-ttu-id="0011e-123">Listet die Elemente auf, die in der Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0011e-123">Enumerate through the items contained within the collection.</span></span>
-   <span data-ttu-id="0011e-124">Ruft ein Element aus der Auflistung ab.</span><span class="sxs-lookup"><span data-stu-id="0011e-124">Retrieve an item from the collection.</span></span>
-   <span data-ttu-id="0011e-125">Hinzufügen oder Entfernen von Elementen zu oder aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="0011e-125">Add or remove items to or from the collection.</span></span>
-   <span data-ttu-id="0011e-126">Speichern oder verwerfen Sie alle ausstehenden Änderungen an der Sammlung oder an den darin enthaltenen Elementen.</span><span class="sxs-lookup"><span data-stu-id="0011e-126">Save or discard any pending changes made to the collection or to the items it contains.</span></span>
-   <span data-ttu-id="0011e-127">Sie erhalten eine andere Sammlung im Katalog.</span><span class="sxs-lookup"><span data-stu-id="0011e-127">Get a different collection in the catalog.</span></span>

<span data-ttu-id="0011e-128">Die [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse implementiert die [**icatalogcollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0011e-128">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface.</span></span>

## <a name="comadmincatalogobject"></a><span data-ttu-id="0011e-129">COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="0011e-129">COMAdminCatalogObject</span></span>

<span data-ttu-id="0011e-130">Die [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse stellt ein beliebiges Element dar, das in einer Auflistung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0011e-130">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class represents any item that is contained within a collection.</span></span> <span data-ttu-id="0011e-131">Objekte werden aus dieser Klasse erstellt, wenn ein Element durch die [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) -Eigenschaft eines Katalog Sammlungs Objekts erhalten wird.</span><span class="sxs-lookup"><span data-stu-id="0011e-131">Objects are created from this class when getting an item through the [**Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) property of a catalog collection object.</span></span> <span data-ttu-id="0011e-132">Mithilfe von Objekten, die aus der **COMAdminCatalogObject** -Klasse erstellt wurden, können Sie folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="0011e-132">Objects created from the **COMAdminCatalogObject** class enable you to do the following:</span></span>

-   <span data-ttu-id="0011e-133">Dient zum Festlegen oder Festlegen von Eigenschaften, die von dem Element unterstützt werden, mit dem das Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0011e-133">Get or set properties supported by the item that the object is being used to represent.</span></span>
-   <span data-ttu-id="0011e-134">Abrufen von Informationen über das Element und seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0011e-134">Obtain information about the item and its properties.</span></span>

<span data-ttu-id="0011e-135">Die [**COMAdminCatalogObject**](comadmincatalogobject.md) -Klasse implementiert die [**icatalogobject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0011e-135">The [**COMAdminCatalogObject**](comadmincatalogobject.md) class implements the [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0011e-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0011e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0011e-137">Zugreifen auf den com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="0011e-137">Accessing the COM+ Catalog</span></span>](accessing-the-com--catalog.md)
</dt> <dt>

[<span data-ttu-id="0011e-138">Übersicht über die COMAdmin-Objekte</span><span class="sxs-lookup"><span data-stu-id="0011e-138">Overview of the COMAdmin Objects</span></span>](overview-of-the-comadmin-objects.md)
</dt> </dl>

 

 



