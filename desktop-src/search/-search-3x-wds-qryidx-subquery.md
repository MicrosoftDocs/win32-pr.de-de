---
description: Erfahren Sie mehr über das SUBQUERY-Argument in Windows Search. Eine Unterabfrage ist eine gespeicherte Suchdatei, die Sie als Filter für eine neue Abfrage verwenden können.
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: SUBQUERY-Argument (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b23028d0bddcc674714f51f8b31883052431bd
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011033"
---
# <a name="subquery-argument-windows-search"></a>SUBQUERY-Argument (Windows Search)

Eine Unterabfrage ist eine gespeicherte Suchdatei ( .search-ms), die Sie als Filter für \* eine neue Abfrage verwenden können. Die Ergebnisse der Unterabfrage werden als Quelle für die neue Abfrage verwendet. Angenommen, Sie verfügen über mehrere gespeicherte Suchdateien, die eine Abfrage nach E-Mail-Verteilerliste einschränken: mydepartment.search-ms, teamproject.search-ms und corporatewide.search-ms. Mithilfe `subquery` des -Arguments können Sie E-Mail-Suchvorgänge auf eine oder alle dieser gespeicherten Suchvorgänge beschränken.

Dieses Thema ist wie folgt organisiert:

-   [Beispiel](#example)
-   [Verwandte Themen](#related-topics)

## <a name="example"></a>Beispiel


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit Parameter-Value Argumenten](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[Locale Identifier Arguments](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[CRUMB-Argument](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[SYNTAX-Argument](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY-Argument](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 



