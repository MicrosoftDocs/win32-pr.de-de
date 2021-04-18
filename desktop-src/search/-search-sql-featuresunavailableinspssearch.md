---
description: Die Microsoft Windows Search-Abfragesprache basiert auf Structured Query Language (SQL). Es wird jedoch nicht in einer relationalen Datenbank mit benutzerdefinierten Tabellen oder Indizes durchsucht.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL-Funktionen sind in Microsoft Windows Search nicht verfügbar.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341188"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL-Funktionen sind in Microsoft Windows Search nicht verfügbar.

Die Microsoft Windows Search-Abfragesprache basiert auf Structured Query Language (SQL). Es wird jedoch nicht in einer relationalen Datenbank mit benutzerdefinierten Tabellen oder Indizes durchsucht. Aus diesem Grund sind viele Standard-SQL-Anweisungen und Syntax Funktionen nicht anwendbar. Im folgenden finden Sie eine Liste der signifikanteren SQL-Features, die in Windows Search nicht unterstützt werden.


-   Batch-Anweisungen
-   COALESCE- \_ Tabellen Funktion
-   Convert-Funktion (verwenden Sie stattdessen die Cast Funktionen)
-   CREATE VIEW-Anweisung
-   Datendefinitionssprache
-   DataSource-Anweisung
-   Datums-und Uhrzeit Formate außer ISO-Datums-und Zeitstempel
-   DELETE-Anweisung
-   GRANT-Anweisung
-   Informations Schema
-   INSERT-Anweisung
-   Datentypen OLE DB
-   Reguläre SQL-Standard Ausdrücke (verwenden Sie stattdessen "enthält" oder ähnliches)
-   Parameter für SQL-Abfragen
-   Vergleich von relationalen Spalten
-   Revision-ID-Header
-   REVOKE-Anweisung
-   Bereichs Aliase oder Revisionsnummern
-   Alles auswählen (entfernt Duplikate automatisch)
-   Gespeicherte Prozeduren
-   Strukturierte Dokument Erweiterung
-   UNION ALL
-   Unbekanntes Schlüsselwort
-   UPDATE-Anweisung

Windows Search unterstützt keine Thesaurus-und Füll Wörter.

 

 



