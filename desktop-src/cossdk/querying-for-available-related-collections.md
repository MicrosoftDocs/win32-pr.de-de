---
description: Abfragen von verfügbaren verwandten Sammlungen
ms.assetid: 9c7d2a01-5dc3-4d35-b938-f1d0525a8286
title: Abfragen von verfügbaren verwandten Sammlungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0203df5bb7b5bf89396d5687dc28b19e9b183d56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342319"
---
# <a name="querying-for-available-related-collections"></a><span data-ttu-id="64519-103">Abfragen von verfügbaren verwandten Sammlungen</span><span class="sxs-lookup"><span data-stu-id="64519-103">Querying for Available Related Collections</span></span>

<span data-ttu-id="64519-104">Wenn Sie ein allgemeines Verwaltungs Tool schreiben, ist es wahrscheinlich, dass Sie Routinen für die Navigation in der gesamten Sammlungs Hierarchie schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="64519-104">If you are writing a general-purpose administration tool, it is likely that you will need to write routines for navigating the entire collection hierarchy.</span></span> <span data-ttu-id="64519-105">Um dies zu unterstützen, verfügt com+ über eine Funktion, die es Ihnen ermöglicht, die verknüpften Auflistungen, die in einer bestimmten Sammlung verfügbar sind, dynamisch abzufragen</span><span class="sxs-lookup"><span data-stu-id="64519-105">To support this, COM+ has a facility that enables you to dynamically query for the related collections that are available from any given collection.</span></span>

<span data-ttu-id="64519-106">Die [**relatedcollectioninfo**](relatedcollectioninfo.md) -Auflistung ist in jeder Auflistung verfügbar, die Sie möglicherweise beibehalten, und enthält ein Element für jede verfügbare verknüpfte Auflistung.</span><span class="sxs-lookup"><span data-stu-id="64519-106">The [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection is available from any collection that you might be holding and contains an item for each available related collection.</span></span> <span data-ttu-id="64519-107">Sie können diese Elemente durchlaufen, um zu bestimmen, ob eine bestimmte Sammlung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="64519-107">You can enumerate through these items to determine whether a given collection is available.</span></span>

<span data-ttu-id="64519-108">Sie können die [**relatedcollectioninfo**](relatedcollectioninfo.md) -Auflistung aus einer beliebigen Auflistung mit der [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt erhalten, wobei der zweite Parameter leer bleibt, wo Sie normalerweise die Schlüsseleigenschaft eines übergeordneten Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="64519-108">You can get the [**RelatedCollectionInfo**](relatedcollectioninfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64519-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64519-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64519-110">Navigieren in der com+-Sammlungs Hierarchie</span><span class="sxs-lookup"><span data-stu-id="64519-110">Navigating the COM+ Collection Hierarchy</span></span>](navigating-the-com--collection-hierarchy.md)
</dt> <dt>

[<span data-ttu-id="64519-111">Com+-Sammlungen werden aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="64519-111">Populating COM+ Collections</span></span>](populating-com--collections.md)
</dt> <dt>

[<span data-ttu-id="64519-112">Abrufen von Auflistungen im com+-Katalog</span><span class="sxs-lookup"><span data-stu-id="64519-112">Retrieving Collections on the COM+ Catalog</span></span>](retrieving-collections-on-the-com--catalog.md)
</dt> </dl>

 

 



