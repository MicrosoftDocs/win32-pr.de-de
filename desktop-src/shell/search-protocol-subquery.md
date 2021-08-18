---
description: Erfahren Sie mehr über das SUBQUERY-Argument in The Windows Shell. Eine Unterabfrage ist eine gespeicherte Suchdatei, die Sie als Filter für eine neue Abfrage verwenden können.
title: SUBQUERY-Argument (die Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fc478c9aff21b20566ffcd8d10580abaf8affa8eb36c39adb8c3c75486ca999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452866"
---
# <a name="subquery-argument-the-windows-shell"></a>SUBQUERY-Argument (die Windows Shell)

Eine Unterabfrage ist eine gespeicherte Suchdatei ( .search-ms), die Sie als Filter für \* eine neue Abfrage verwenden können. Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet. Beispiel: Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage nach E-Mail-Verteilerliste einschränken: mydepartment.search-ms, teamproject.search-ms und corporatewide.search-ms. Mithilfe `subquery` des -Arguments können Sie E-Mail-Suchvorgänge auf eine oder alle dieser gespeicherten Suchvorgänge beschränken.

## <a name="example"></a>Beispiel


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



