---
title: Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle unterstützen
description: Es ist ungewöhnlich, dass zwei Erweiterungen die gleiche Schnittstelle für ADSI verfügbar machen.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle ADSI unterstützen
- Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle ADSI unterstützen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342237"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a><span data-ttu-id="5ce39-105">Auflösung mehrerer Aggregations Komponenten, die dieselbe Schnittstelle unterstützen</span><span class="sxs-lookup"><span data-stu-id="5ce39-105">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>

<span data-ttu-id="5ce39-106">Es ist ungewöhnlich, dass zwei Erweiterungen die gleiche Schnittstelle für ADSI verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="5ce39-106">It is uncommon that two extensions expose the same interface to ADSI.</span></span> <span data-ttu-id="5ce39-107">In diesem Fall gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="5ce39-107">If this happens, the following rules apply:</span></span>

-   <span data-ttu-id="5ce39-108">Wenn eine Schnittstelle, z. b. **IMyInterface**, sowohl vom Aggregator (ADSI) als auch von Erweiterungs Objekten unterstützt wird, gibt **QueryInterface** immer die **IMyInterface** für ADSI zurück.</span><span class="sxs-lookup"><span data-stu-id="5ce39-108">If an interface, such as **IMyInterface**, is supported by both the aggregator (ADSI) and any extension objects, **QueryInterface** always returns the **IMyInterface** for ADSI.</span></span>
-   <span data-ttu-id="5ce39-109">Wenn eine Schnittstelle, z. b. **IMyInterface**, nicht vom Aggregator (ADSI) unterstützt wird, sondern von mehr als einem Erweiterungs Objekt unterstützt wird, gibt **QueryInterface** die **IMyInterface** des ersten Erweiterungs Objekts zurück, das in der Registrierung aufgeführt ist, die die-Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ce39-109">If an interface, such as **IMyInterface**, is not supported by the aggregator (ADSI), but is supported by more than one extension object, **QueryInterface** returns the **IMyInterface** of the first extension object listed in the registry that supports the interface.</span></span>

<span data-ttu-id="5ce39-110">Beachten Sie, dass die Reihenfolge der Komponenten in der Registrierung auch die Auflösung von Namenskonflikten bei der Automatisierung beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="5ce39-110">Be aware that the order of components in the registry also affects the resolution of name conflicts in Automation.</span></span> <span data-ttu-id="5ce39-111">Weitere Informationen finden Sie unter Auflösen [von Funktions-/Eigenschaftenname-Konflikten in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5ce39-111">For more information, see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>

 

 




