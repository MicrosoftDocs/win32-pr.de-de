---
description: Das NULL-Prädikat gibt an, ob das Dokument über einen Wert für die angegebene Spalte verfügt.
ms.assetid: 078ffd99-2020-4da2-8968-301dba8cc436
title: NULL-Prädikat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd80ea6cba2009b398c8cdd0a2926240e3ce78309ca3f8511fb6ba286f44a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058120"
---
# <a name="null-predicate"></a>NULL-Prädikat

Das **NULL-Prädikat** gibt an, ob das Dokument über einen Wert für die angegebene Spalte verfügt.

Das **NULL-Prädikat** weist die folgende Syntax auf:


```
...WHERE <column> IS [NOT] NULL
```



Das optionale NOT-Schlüsselwort negiert das Ergebnis. Die Spalte kann ein regulärer oder durch Trennzeichen getrennter [Bezeichner](-search-sql-identifiers.md)sein.

> [!IMPORTANT]
> Um zu testen, ob eine Spalte über den **NULL-Wert** verfügt, müssen Sie das **NULL-Prädikat** verwenden. Es ist nicht gültig, den **NULL-Wert** in einem Vergleichsprädikat zu verwenden. "WHERE column IS **NULL"** ist richtig. "WHERE column = **NULL**" ist ungültig.

 

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden Dokumente zurückgegeben, die keinen System.Video.Director-Wert aufweisen.


```
...WHERE System.Video.Director IS NULL
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[LIKE-Prädikat](-search-sql-like.md)
</dt> <dt>

[Literalwertvergleich](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Mehrwertige Vergleiche (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltextprädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



