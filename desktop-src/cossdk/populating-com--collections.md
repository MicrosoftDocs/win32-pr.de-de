---
description: Com+-Sammlungen werden aufgefüllt.
ms.assetid: df86cbab-dcb8-46ac-aebf-8516276b6e81
title: Com+-Sammlungen werden aufgefüllt.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d85521eb7e3750d06920a570ddeaf4d7e9b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342249"
---
# <a name="populating-com-collections"></a><span data-ttu-id="4aed3-103">Com+-Sammlungen werden aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="4aed3-103">Populating COM+ Collections</span></span>

<span data-ttu-id="4aed3-104">Nachdem Sie eine Sammlung abgerufen haben und bevor Sie direkt mit den darin enthaltenen Elementen arbeiten können, müssen Sie die Auflistung mit der Auffüllen [**-Methode auffüllen**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) .</span><span class="sxs-lookup"><span data-stu-id="4aed3-104">After you have retrieved a collection and before you can work directly with the items it contains, you must populate the collection by using the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method.</span></span> <span data-ttu-id="4aed3-105">Dadurch werden Daten für den Inhalt der Sammlung aus dem com+-Katalog abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4aed3-105">This fetches data for the collection's contents from the COM+ catalog.</span></span>

<span data-ttu-id="4aed3-106">Es ist wichtig zu verstehen, dass Sie immer, wenn Sie die COMAdmin-Objekte zum Bearbeiten von Elementen oder Daten in Auflistungen verwenden, tatsächlich an transitiv zwischengespeicherten Daten arbeiten. Sie arbeiten nicht direkt mit dem beibehaltenen Katalog.</span><span class="sxs-lookup"><span data-stu-id="4aed3-106">It is important to understand that whenever you use the COMAdmin objects to manipulate items or data in collections, you are really working on transiently cached data; you are not working directly with the persisted catalog.</span></span> <span data-ttu-id="4aed3-107">Nichts, was Sie mit einer Auflistung oder einem ihrer Elemente tun, wird im Katalog widergespiegelt, bis Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) für die Auflistung aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="4aed3-107">Nothing that you do with a collection or any of its items is reflected on the catalog until you call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the collection.</span></span> <span data-ttu-id="4aed3-108">Weitere Details finden Sie unter [Speichern oder Verwerfen von Änderungen](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="4aed3-108">For more detail, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="4aed3-109">Alle nachfolgenden Aufrufe [**zum Auffüllen**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate)vor dem Aufruf von [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)haben den Effekt, ausstehende Änderungen an allen Elementen in der Auflistung zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="4aed3-109">Any subsequent calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate), prior to calling [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), has the effect of discarding pending changes to all items in the collection.</span></span> <span data-ttu-id="4aed3-110">Auffüllen **füllt immer den** Cache, in dem Sie arbeiten, mit den Daten, die im zugrunde liegenden Katalogdaten Speicher beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="4aed3-110">**Populate** always populates the cache you're working in with whatever data is persisted on the underlying catalog data store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aed3-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4aed3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aed3-112">Navigieren in der com+-Sammlungs Hierarchie</span><span class="sxs-lookup"><span data-stu-id="4aed3-112">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="4aed3-113">Abfragen von verfügbaren verwandten Sammlungen</span><span class="sxs-lookup"><span data-stu-id="4aed3-113">Querying for Available Related Collections</span></span>](querying-for-available-related-collections.md)
</dt> <dt>

[<span data-ttu-id="4aed3-114">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="4aed3-114">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



