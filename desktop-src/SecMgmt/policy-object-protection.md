---
description: Beschreibt, wie das Richtlinien Objekt standardmäßig geschützt wird.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Richtlinien Objektschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750889"
---
# <a name="policy-object-protection"></a><span data-ttu-id="e5982-103">Richtlinien Objektschutz</span><span class="sxs-lookup"><span data-stu-id="e5982-103">Policy Object Protection</span></span>

<span data-ttu-id="e5982-104">Das [**Richtlinien**](policy-object.md) Objekt ist standardmäßig mit den folgenden Einstellungen geschützt:</span><span class="sxs-lookup"><span data-stu-id="e5982-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="e5982-105">Die lokale Gruppenumgebung hat allgemeinen \_ Ausführungs Zugriff.</span><span class="sxs-lookup"><span data-stu-id="e5982-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="e5982-106">Das bekannte ID-System erhält Zugriff auf die Richtlinie \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e5982-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="e5982-107">Der lokale Administrator der lokalen Gruppe \_ verfügt über generische \_ Lese-, generischer \_ Schreib-und generischer \_ Ausführungs Zugriff.</span><span class="sxs-lookup"><span data-stu-id="e5982-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="e5982-108">Der lokale Administrator der Gruppe \_ wird als Besitzer und primäre Gruppe dieses Objekts zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e5982-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="e5982-109">Das [**Richtlinien**](policy-object.md) Objekt kann nicht erstellt oder zerstört werden.</span><span class="sxs-lookup"><span data-stu-id="e5982-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 



