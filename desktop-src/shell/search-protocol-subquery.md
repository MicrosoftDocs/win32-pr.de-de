---
description: Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können.
title: Unterabfrage Argument (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 43e4a5b904d5e769eb43acad05aa5d8ce37ebde2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995038"
---
# <a name="subquery-argument-the-windows-shell"></a>Unterabfrage Argument (die Windows-Shell)

Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können. Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet. Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage durch eine e-Mail-Verteilerliste einschränken: myDepartment. Search-MS, teamproject. Search-MS und corporatewide. Search-ms. Mit dem `subquery` -Argument können Sie e-Mail-Suchvorgänge auf beliebige oder alle dieser gespeicherten Suchvorgänge beschränken.

## <a name="example"></a>Beispiel


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Argument Informationen



|                          |                                         |
|--------------------------|-----------------------------------------|
| Mindestens Betriebs System | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



