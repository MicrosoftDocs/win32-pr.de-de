---
title: Was die Installation tun muss
description: Auf neue Attribute, auf die in Schritt 3 verwiesen wird, muss von ihrer OID verwiesen werden, da der neue Attribut Name an dieser Stelle nicht im Schema Cache vorhanden ist.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Was die Installation tun muss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947371"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="191b9-104">Was die Installation tun muss</span><span class="sxs-lookup"><span data-stu-id="191b9-104">What the Installation Must Do</span></span>

<span data-ttu-id="191b9-105">Anwendungen, die das Schema erweitern, müssen Updates anwenden, wie im folgenden Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="191b9-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="191b9-106">**So wenden Sie beim Erweitern des Schemas Updates an**</span><span class="sxs-lookup"><span data-stu-id="191b9-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="191b9-107">Fügen Sie die neuen Attribute hinzu.</span><span class="sxs-lookup"><span data-stu-id="191b9-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="191b9-108">Fügen Sie die neuen Klassen hinzu.</span><span class="sxs-lookup"><span data-stu-id="191b9-108">Add the new classes.</span></span>
3.  <span data-ttu-id="191b9-109">Fügen Sie die neuen Attribute zu Klassen hinzu.</span><span class="sxs-lookup"><span data-stu-id="191b9-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="191b9-110">Löst einen Cache erneuten Ladevorgang aus.</span><span class="sxs-lookup"><span data-stu-id="191b9-110">Trigger a cache reload.</span></span>

<span data-ttu-id="191b9-111">Auf neue Attribute, auf die in Schritt 3 verwiesen wird, muss von ihrer OID verwiesen werden, da der neue Attribut Name an dieser Stelle nicht im Schema Cache vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="191b9-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="191b9-112">Schritt 4 ist nicht erforderlich, wenn die Erweiterungen nicht sofort verwendet werden. die Erweiterungen werden je nach System Auslastung in ungefähr 5 Minuten im Schema Cache angezeigt.</span><span class="sxs-lookup"><span data-stu-id="191b9-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="191b9-113">Weitere Informationen zum Schema Cache und zum erneuten Laden des Caches finden Sie unter [Aktualisieren des Schema Caches](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="191b9-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 




