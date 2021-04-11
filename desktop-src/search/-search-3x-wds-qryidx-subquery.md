---
description: Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: Unterabfrage Argument (Windows-Suche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958785"
---
# <a name="subquery-argument-windows-search"></a>Unterabfrage Argument (Windows-Suche)

Eine Unterabfrage ist eine gespeicherte Suchdatei ( \* . Search-MS), die Sie als Filter für eine neue Abfrage verwenden können. Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet. Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage durch eine e-Mail-Verteilerliste einschränken: myDepartment. Search-MS, teamproject. Search-MS und corporatewide. Search-ms. Mit dem `subquery` -Argument können Sie e-Mail-Suchvorgänge auf beliebige oder alle dieser gespeicherten Suchvorgänge beschränken.

Dieses Thema ist wie folgt organisiert:

-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="example"></a>Beispiel


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Die ersten Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Locale-bezeichnerargumente](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[Crumb-Argument](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[Syntax Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[Stackedby-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



