---
title: Aktualisieren des Schema Caches
description: Alle Informationen, die auf einen Active Directory Server geschrieben werden, werden anhand des Schemas überprüft.
ms.assetid: 948f8ec5-7207-4566-bd79-60cdd54231bf
ms.tgt_platform: multiple
keywords:
- Aktualisieren des Schema Cache-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bf915d00b463b81a331ffe39b342f620a50417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707517"
---
# <a name="updating-the-schema-cache"></a><span data-ttu-id="1f3bf-104">Aktualisieren des Schema Caches</span><span class="sxs-lookup"><span data-stu-id="1f3bf-104">Updating the Schema Cache</span></span>

<span data-ttu-id="1f3bf-105">Alle Informationen, die auf einen Active Directory Server geschrieben werden, werden anhand des Schemas überprüft.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-105">All information that is written to an Active Directory server is validated against the schema.</span></span> <span data-ttu-id="1f3bf-106">Das Schema wird aus Leistungsgründen im Arbeitsspeicher auf Verzeichnisservern (Domänen Controllern) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-106">The schema is held in memory on directory servers (domain controllers) for performance reasons.</span></span> <span data-ttu-id="1f3bf-107">Die in-Memory-Version wird automatisch aktualisiert, nachdem die auf dem Datenträger aktualisierte Version aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-107">The in-memory version is updated automatically after the on-disk version has been updated.</span></span> <span data-ttu-id="1f3bf-108">Das automatische Update erfolgt fünf Minuten nach dem Anwenden der letzten Änderung. Wenn Sie im 5-Minuten-Fenster eine weitere Änderung am Schema anwenden, wird der Timer für weitere fünf Minuten zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-108">The automatic update occurs five minutes after the last change was applied; applying another change to the schema in the 5-minute window resets the timer for another 5 minutes.</span></span> <span data-ttu-id="1f3bf-109">Dieses Verhalten sorgt für einen konsistenten Cache, kann jedoch verwirrend sein, da Änderungen nicht im Schema angezeigt werden, bis der Cache aktualisiert wird, auch wenn Sie auf den Datenträger angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-109">This behavior keeps the cache consistent, but can be confusing, because changes do not appear in the schema until the cache is updated, even though they were applied on disk.</span></span>

<span data-ttu-id="1f3bf-110">Um den Active Directory Schema Cache nach einer Schema Aktualisierung zu aktualisieren, oder wenn Sie die Schema Aktualisierung für nicht-Schema-Vorgänge sofort verwenden möchten, fügen Sie das Attribut **schemaUpdateNow** (es ist ein Betriebs Attribut) dem Stamm-DSE (leeres DN) mit dem Wert 1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-110">To update the Active Directory schema cache after a schema update, or if you want to use the schema update for non-schema operations immediately, add the **schemaUpdateNow** attribute (it is an operational attribute) to the root DSE (blank DN) with value 1.</span></span> <span data-ttu-id="1f3bf-111">Ein Schema Cache Update wird sofort gestartet.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-111">A schema cache update will start immediately.</span></span> <span data-ttu-id="1f3bf-112">Der-Befehl blockiert.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-112">The call is blocking.</span></span> <span data-ttu-id="1f3bf-113">Wenn der-Rückruf ohne Fehler zurückgegeben wird, wird der Cache aktualisiert, und alle Schema Aktualisierungen sind zur Verwendung bereit.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-113">If the call returns with no error, the cache is updated and all schema updates are ready to be used.</span></span> <span data-ttu-id="1f3bf-114">Ein Fehler gibt an, dass das Cache Update nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-114">An error return indicates the cache update was unsuccessful.</span></span> <span data-ttu-id="1f3bf-115">Anwendungen, die dieses Feature verwenden müssen, sollten für den blockierenden Schreibvorgang konzipiert werden, insbesondere bei der Bereitstellung des Benutzer Feedbacks, wenn das Programm oder Skript interaktiv ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-115">Applications that must use this feature should be designed to accommodate the blocking write, particularly in giving the user feedback, if the program or script executes interactively.</span></span>

<span data-ttu-id="1f3bf-116">Das folgende Codebeispiel zeigt ein LDIFDE-Beispielskript, das zeigt, wie ein erneutes Laden des Caches auslöst.</span><span class="sxs-lookup"><span data-stu-id="1f3bf-116">The following code example is a sample LDIFDE script that shows how to trigger a cache reload.</span></span>

``` syntax
dn:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

<span data-ttu-id="1f3bf-117">Weitere Informationen zum programmgesteuerten Aktualisieren des Schema Caches finden Sie unter [Beispiel Code zum Aktualisieren des Schema Caches](example-code-for-updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="1f3bf-117">For more information about how to update the schema cache programmatically, see [Example Code for Updating the Schema Cache](example-code-for-updating-the-schema-cache.md).</span></span>

 

 




