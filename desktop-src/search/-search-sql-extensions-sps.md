---
description: Microsoft Windows Search, basierend auf den Standards SQL-92 und SQL-99, verbessert die dokumentbasierte Volltextsuche in Dokumentenverwaltungs- oder Wissensverwaltungsanwendungen.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: SQL Erweiterungen in Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c300b0960e97cba14237bd355e33ae7e42788b1925525e60462d15a5d014e6f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462458"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a>SQL Erweiterungen in Microsoft Windows Search

Microsoft Windows Search, basierend auf den Standards SQL-92 und SQL-99, verbessert die dokumentbasierte Volltextsuche in Dokumentenverwaltungs- oder Wissensverwaltungsanwendungen. Windows Die Suchverbesserungen umfassen Folgendes:

## <a name="128-character-identifier-names"></a>Bezeichnernamen mit 128 Zeichen

Während SQL-92 und SQL-99 Spalten- und andere Bezeichner auf 18 Zeichen beschränken, unterstützt Windows Search Spaltennamen mit 128 Zeichen. Weitere Informationen finden Sie unter [Bezeichner](-search-sql-identifiers.md).

## <a name="grouping-results-by-columns"></a>Gruppieren von Ergebnissen nach Spalten

Abfragen können angeben, wie Ergebnisse gruppiert werden sollen. Sie können die Bereiche angeben, nach denen gruppiert werden soll, und Sie können mehrere Spalten für die Gruppierung angeben. Beispielsweise können Sie Ergebnisse über einen Bereich von Dateigrößen gruppieren (Größe < 100, 100 <= Größe < 1000; 1000 <= Größe), und Sie können Gruppierungen schachteln. Weitere Informationen finden Sie unter [GROUP ON ... Über... Anweisung](-search-sql-group-on-over.md).

## <a name="diacritic-insensitive-searching"></a>Diacritic-Insensitive Suchen

Zusätzlich zur Suche, bei der die Groß-/Kleinschreibung nicht beachtet wird, unterstützt Windows Search die Suche, die nicht auf diakritische Zeichen (Akzente) reagiert. Weitere Informationen finden Sie unter [Diakritische Empfindlichkeit in Suchvorgänge.](-search-sql-accentinsensitivitysearches.md)

## <a name="column-weighting"></a>Spaltengewichtung

Abfragen, die mehr als eine Spalte durchsuchen, können die Wichtigkeit jeder Spalte angeben. Die [CONTAINS-](-search-sql-contains.md) und [FREETEXT-Prädikate](-search-sql-freetext.md) unterstützen beide die Spaltengewichtung.

## <a name="null-predicate"></a>NULL-Prädikat

Obwohl die Volltextinhaltsindizierung keinen definierten Satz von Spalten aufweist, können Abfragen erfordern, dass Member des Resultset bestimmte Spalten aufweisen oder nicht. Es ist nicht möglich, zwischen einem Dokument zu unterscheiden, das über eine angegebene Eigenschaft verfügt, wobei der Wert auf **NULL** festgelegt ist, und einem Dokument, das überhaupt nicht über die -Eigenschaft verfügt.

## <a name="rank-modification"></a>Rangfolgeänderung

Sie können die Rangfolge der Suchergebnisse bearbeiten, indem Sie [Gewichtungen](-search-sql-understandingrelevancevalues.md) für Eigenschaften und für Eigenschaftengruppen mit Alias verwenden. Die Rangfolgekoersion unterstützt die direkte Bearbeitung der Relevanzrangfolge basierend auf den von Ihnen angegebenen Kriterien.

 

 



