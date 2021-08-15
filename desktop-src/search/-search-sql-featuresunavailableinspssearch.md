---
description: Die Abfragesprache Windows Microsoft-Suche basiert auf strukturierte Abfragesprache (SQL); Es wird jedoch nicht in einer relationalen Datenbank mit benutzerdefinierten Tabellen oder Indizes gesucht.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL Features in Microsoft Windows Search nicht verfügbar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66adb175aa7fae799e0ad9b69916415f12c94ee984d276b5a2238ebb19ec2f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716120"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL Features in Microsoft Windows Search nicht verfügbar

Die Abfragesprache Windows Microsoft-Suche basiert auf strukturierte Abfragesprache (SQL); Es wird jedoch nicht in einer relationalen Datenbank mit benutzerdefinierten Tabellen oder Indizes gesucht. Aus diesem Grund gelten viele standard SQL-Anweisungen und Syntaxfeatures nicht. Im Folgenden finden Sie eine Liste der wichtigsten SQL, die in der Suchfunktion nicht Windows werden.


-   BATCH-Anweisungen
-   COALESCE \_ TABLE-Funktion
-   CONVERT-Funktion (verwenden Sie stattdessen die CAST-Funktionen)
-   CREATE VIEW-Anweisung
-   Datendefinitionssprache
-   DATASOURCE-Anweisung
-   Andere Datums- und Uhrzeitformate als ISO-Datums- und Zeitstempel
-   DELETE-Anweisung
-   GRANT-Anweisung
-   Informationsschema
-   INSERT-Anweisung
-   OLE DB Datentypen
-   SQL regulären Ausdrücken (verwenden Sie stattdessen CONTAINS oder LIKE)
-   Parameter zum SQL Abfragen
-   Vergleich relationaler Spalten
-   Revisions-ID-Header
-   REVOKE-Anweisung
-   SCOPE-Aliase oder Revisionsnummern
-   SELECT ALL (Duplikate werden automatisch entfernt)
-   Gespeicherte Prozeduren
-   Erweiterung strukturierter Dokumente
-   UNION ALL
-   UNKNOWN-Schlüsselwort
-   UPDATE-Anweisung

Windows Die Suche unterstützt Thesaurus und Rauschwörter nicht.

 

 



