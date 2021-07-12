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
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581598"
---
# <a name="subquery-argument-the-windows-shell"></a>SUBQUERY-Argument (die Windows Shell)

Eine Unterabfrage ist eine gespeicherte Suchdatei \* (.search-ms), die Sie als Filter für eine neue Abfrage verwenden können. Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet. Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage nach E-Mail-Verteilerliste einschränken: mydepartment.search-ms, teamproject.search-ms und corporatewide.search-ms. Mithilfe des `subquery` -Arguments können Sie E-Mail-Suchvorgänge auf eine oder alle dieser gespeicherten Suchvorgänge beschränken.

## <a name="example"></a>Beispiel


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



