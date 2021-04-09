---
description: Speichern oder Verwerfen von Änderungen
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Speichern oder Verwerfen von Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860848"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="69bd7-103">Speichern oder Verwerfen von Änderungen</span><span class="sxs-lookup"><span data-stu-id="69bd7-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="69bd7-104">Wenn Sie Eigenschaften für ein Element festlegen, werden keine Änderungen tatsächlich im com+-Katalog aufgezeichnet, bis Sie die Änderungen explizit speichern.</span><span class="sxs-lookup"><span data-stu-id="69bd7-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="69bd7-105">Verwenden Sie hierzu die [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt für die Auflistung, die das Element enthält.</span><span class="sxs-lookup"><span data-stu-id="69bd7-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="69bd7-106">Wenn Sie Änderungen verwerfen möchten, für die noch kein Commit ausgeführt wurde, können Sie die [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) -Methode für das [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekt aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="69bd7-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="69bd7-107">Dadurch werden alle persistenten Daten aus dem com+-Katalog für alle Elemente in der Auflistung gelesen, wodurch alle ausstehenden Änderungen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="69bd7-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="69bd7-108">Wenn Sie [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)verwenden, führen alle Inkonsistenzen in den von Ihnen ausgewählten Eigenschafts Einstellungen zu einem Fehler, und **SaveChanges** kann das Objekt, das den Fehler zurückgegeben hat, nicht schreiben.</span><span class="sxs-lookup"><span data-stu-id="69bd7-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="69bd7-109">Alle Eigenschaften für ein bestimmtes Element werden entweder geschrieben oder können nicht als Ganzes geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="69bd7-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="69bd7-110">Wenn jedoch Schreibfehler auftreten, sind Sie möglicherweise nicht auf inkompatible Einstellungen zurückzuführen. Möglicherweise ist ein anderer Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="69bd7-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="69bd7-111">Sie müssen die Details des Fehlers überprüfen, um sicher zu sein.</span><span class="sxs-lookup"><span data-stu-id="69bd7-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="69bd7-112">Weitere Informationen finden Sie unter [Behandeln von com+-Verwaltungsfehlern](handling-com--administration-errors.md) und [Abhängigkeiten zwischen Eigenschaften](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="69bd7-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="69bd7-113">Als allgemeine Regel gilt: je mehr Änderungen Sie versuchen, gleichzeitig zu speichern, insbesondere Änderungen an mehreren Objekten, desto wahrscheinlicher ist es, dass Sie eine Fehlermeldung erhalten, und desto schwieriger ist es, eine Nachverfolgung durchführen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="69bd7-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="69bd7-114">Außerdem verfügen Sie zwischen Aufrufen [**von "auffüllen" und "**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)" nicht über eine Sperre für die Elemente in der Sammlung. Konflikte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="69bd7-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="69bd7-115">Weitere Informationen finden Sie unter " [erhalten und Festlegen von Eigenschaften](getting-and-setting-properties.md)".</span><span class="sxs-lookup"><span data-stu-id="69bd7-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="69bd7-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="69bd7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69bd7-117">Eigenschaften werden erhalten und festgelegt</span><span class="sxs-lookup"><span data-stu-id="69bd7-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="69bd7-118">Abhängigkeiten zwischen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69bd7-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="69bd7-119">Abfragen von verfügbaren Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="69bd7-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



