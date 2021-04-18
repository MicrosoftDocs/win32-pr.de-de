---
description: Microsoft Windows Search verbessert auf der Grundlage der SQL-92-und SQL-99-Standards die voll Textdokument basierte Suche in Dokumenten-oder Wissens Verwaltungs Anwendungen.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL-Erweiterungen in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525490"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQL-Erweiterungen in Microsoft Windows Search

Microsoft Windows Search verbessert auf der Grundlage der SQL-92-und SQL-99-Standards die voll Textdokument basierte Suche in Dokumenten-oder Wissens Verwaltungs Anwendungen. Die Verbesserungen der Windows-Suche umfassen Folgendes:

## <a name="128-character-identifier-names"></a>128-Zeichen Bezeichnernamen

Während SQL-92 und SQL-99 Spalten-und andere Bezeichner auf 18 Zeichen beschränken, unterstützt Windows Search 128 Zeichen-Spaltennamen. Weitere Informationen finden Sie unter [Bezeichner](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Gruppieren von Ergebnissen nach Spalten

Abfragen können angeben, wie Ergebnisse gruppiert werden sollen. Sie können die Bereiche angeben, nach denen gruppiert werden soll, und Sie können mehr als eine Spalte für die Gruppierung angeben. Beispielsweise können Sie Ergebnisse für einen Bereich von Dateigrößen gruppieren (Größe < 100, 100 <= size < 1000; 1000 <= size), und Sie können Gruppierungen Schachteln. Weitere Informationen finden Sie unter [Group on... Über... -Anweisung](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Diacritic-Insensitive Suche

Neben der Suche, bei der die Groß-/Kleinschreibung nicht beachtet wird, unterstützt Windows Search die Suche, die nicht von diakritischen Zeichen (Akzentzeichen) abhängig ist. Weitere Informationen finden Sie unter [diakritische Sensitivität bei Such](-search-sql-accentinsensitivitysearches.md)Vorgängen.

## <a name="column-weighting"></a>Spalten Gewichtung

Abfragen, die mehr als eine Spalte durchsuchen, können die Wichtigkeit der einzelnen Spalten angeben. Die Prädikate " [enthält](-search-sql-contains.md) " und " [fretext](-search-sql-freetext.md) " unterstützen die Spalten Gewichtung.

## <a name="null-predicate"></a>NULL-Prädikat

Obwohl die voll Text Inhalts Indizierung keinen definierten Satz von Spalten aufweist, können Abfragen erfordern, dass die Elemente des Resultsets über angegebene Spalten verfügen oder nicht. Es ist nicht möglich, zwischen einem Dokument eine angegebene Eigenschaft mit dem Wert **null** und einem Dokument, das nicht die-Eigenschaft aufweist, zu unterscheiden.

## <a name="rank-modification"></a>Änderung von Rang

Sie können die Rangfolge der Suchergebnisse mithilfe von [Gewichtungen](-search-sql-understandingrelevancevalues.md) in Eigenschaften und in Alias Gruppen Gruppen bearbeiten. Rang Koersion unterstützt die direkte Bearbeitung der Relevanzrangfolge basierend auf den von Ihnen angegebenen Kriterien.

 

 



