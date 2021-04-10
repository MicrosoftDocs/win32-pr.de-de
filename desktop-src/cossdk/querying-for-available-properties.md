---
description: Abfragen von verfügbaren Eigenschaften
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Abfragen von verfügbaren Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127401"
---
# <a name="querying-for-available-properties"></a><span data-ttu-id="27047-103">Abfragen von verfügbaren Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27047-103">Querying for Available Properties</span></span>

<span data-ttu-id="27047-104">Wenn Sie ein allgemeines Verwaltungs Tool schreiben, müssen Sie höchstwahrscheinlich Routinen zum Festlegen von Eigenschaften mit vollständiger Generalität schreiben.</span><span class="sxs-lookup"><span data-stu-id="27047-104">If you are writing a general-purpose administration tool, you most likely will need to write routines for setting properties in full generality.</span></span> <span data-ttu-id="27047-105">Um dies zu unterstützen, gibt es eine Funktion, die es Ihnen ermöglicht, die Eigenschaften, die für die Elemente in einer bestimmten Sammlung verfügbar sind, dynamisch abzufragen.</span><span class="sxs-lookup"><span data-stu-id="27047-105">To support this, there is a facility that enables you to dynamically query for the properties that are available for the items in any given collection.</span></span>

<span data-ttu-id="27047-106">Die [**PropertyInfo**](propertyinfo.md) -Auflistung ist in jeder Auflistung verfügbar, die Sie möglicherweise halten.</span><span class="sxs-lookup"><span data-stu-id="27047-106">The [**PropertyInfo**](propertyinfo.md) collection is available from any collection that you might be holding.</span></span> <span data-ttu-id="27047-107">Die **PropertyInfo** -Auflistung enthält ein Element für jede verfügbare Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="27047-107">The **PropertyInfo** collection contains an item for each available property.</span></span> <span data-ttu-id="27047-108">Sie können diese Elemente durchlaufen, um zu bestimmen, ob eine bestimmte Eigenschaft verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="27047-108">You can enumerate through these items to determine whether a given property is available.</span></span>

<span data-ttu-id="27047-109">Sie können die [**PropertyInfo**](propertyinfo.md) -Auflistung von einer beliebigen Auflistung mit der [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt erhalten, wobei der zweite Parameter leer bleibt, wo Sie normalerweise die Schlüsseleigenschaft eines übergeordneten Elements angeben.</span><span class="sxs-lookup"><span data-stu-id="27047-109">You can get the [**PropertyInfo**](propertyinfo.md) collection from any collection you are holding by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, leaving the second parameter blank where you would normally specify a parent item's Key property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27047-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27047-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27047-111">Eigenschaften werden erhalten und festgelegt</span><span class="sxs-lookup"><span data-stu-id="27047-111">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="27047-112">Abhängigkeiten zwischen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="27047-112">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="27047-113">Speichern oder Verwerfen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="27047-113">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



