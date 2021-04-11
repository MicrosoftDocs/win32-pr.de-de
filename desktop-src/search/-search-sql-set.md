---
description: Die Set-Anweisung gibt PropertyName-und RankMethod-Optionen für die Abfrage an.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Set-Anweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128529"
---
# <a name="set-statement"></a><span data-ttu-id="c5f60-103">Set-Anweisung</span><span class="sxs-lookup"><span data-stu-id="c5f60-103">SET Statement</span></span>

<span data-ttu-id="c5f60-104">Die Set-Anweisung gibt PropertyName-und RankMethod-Optionen für die Abfrage an.</span><span class="sxs-lookup"><span data-stu-id="c5f60-104">The SET statement specifies PROPERTYNAME and RANKMETHOD options for the query.</span></span>

## <a name="propertyname"></a><span data-ttu-id="c5f60-105">PropertyName</span><span class="sxs-lookup"><span data-stu-id="c5f60-105">PROPERTYNAME</span></span>

<span data-ttu-id="c5f60-106">Sie können eine Eigenschaft mit einem benutzerfreundlichen Alias für die Abfrage verknüpfen, indem Sie die folgende Syntax verwenden:</span><span class="sxs-lookup"><span data-stu-id="c5f60-106">You can associate a property with a friendly alias for the query by using the following syntax:</span></span>


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a><span data-ttu-id="c5f60-107">RankMethod</span><span class="sxs-lookup"><span data-stu-id="c5f60-107">RANKMETHOD</span></span>

<span data-ttu-id="c5f60-108">Mit der folgenden Syntax können Sie die Rang-Methode für Abfragen mit dem Begriff "ISABOUT" angeben:</span><span class="sxs-lookup"><span data-stu-id="c5f60-108">You can specify the rank method for queries with the ISABOUT term by using the following syntax:</span></span>


```
SET RANKMETHOD <rankmethod>      
```



<span data-ttu-id="c5f60-109">Die RankMethod-Methoden, die mithilfe der Set-Anweisung angegeben werden können, sind Jaccard-Koeffizient, Würfel Koeffizienten und Inneres Produkt.</span><span class="sxs-lookup"><span data-stu-id="c5f60-109">The RANKMETHOD methods that can be specified by using the SET statement are JACCARD COEFFICIENT, DICE COEFFICIENT, and INNER PRODUCT.</span></span>

 

 



