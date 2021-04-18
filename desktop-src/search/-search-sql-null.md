---
description: Das NULL-Prädikat gibt an, ob das Dokument über einen Wert für die Spalte verfügt.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: NULL-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea02a04313ac2b86afe809633bee5ad2cbcf764e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341187"
---
# <a name="null-predicate"></a>NULL-Prädikat

Das **null** -Prädikat gibt an, ob das Dokument über einen Wert für die Spalte verfügt.

Das **null** -Prädikat weist die folgende Syntax auf:


```
...WHERE <column> IS [NOT] NULL
```



Das optionale not-Schlüsselwort negiert das Ergebnis. Die Spalte kann ein regulärer oder Begrenzungs [Bezeichner](-search-sql-identifiers.md)sein.

> [!IMPORTANT]
> Um zu testen, ob eine Spalte den **null** -Wert aufweist, müssen Sie das **null** -Prädikat verwenden. Die Verwendung des **null** -Werts in einem Vergleichs Prädikat ist ungültig. "Where column is **null**" ist richtig. "Where Column = **null**" ist ungültig.

 

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden Dokumente zurückgegeben, die keinen System. Video. Director-Wert aufweisen.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[LIKE-Prädikat](-search-sql-like.md)
</dt> <dt>

[Vergleich von literalen Werten](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Mehrwertige Vergleiche (Array)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



