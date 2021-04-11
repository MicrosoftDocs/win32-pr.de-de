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
# <a name="set-statement"></a>Set-Anweisung

Die Set-Anweisung gibt PropertyName-und RankMethod-Optionen für die Abfrage an.

## <a name="propertyname"></a>PropertyName

Sie können eine Eigenschaft mit einem benutzerfreundlichen Alias für die Abfrage verknüpfen, indem Sie die folgende Syntax verwenden:


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>RankMethod

Mit der folgenden Syntax können Sie die Rang-Methode für Abfragen mit dem Begriff "ISABOUT" angeben:


```
SET RANKMETHOD <rankmethod>      
```



Die RankMethod-Methoden, die mithilfe der Set-Anweisung angegeben werden können, sind Jaccard-Koeffizient, Würfel Koeffizienten und Inneres Produkt.

 

 



