---
description: Die removeodbc-Aktion entfernt die Datenquellen, Konvertierer und Treiber, die während der Installation zum Entfernen aufgeführt sind.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Removeodbc-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349866"
---
# <a name="removeodbc-action"></a>Removeodbc-Aktion

Die removeodbc-Aktion entfernt die Datenquellen, Konvertierer und Treiber, die während der Installation zum Entfernen aufgeführt sind. Mit dieser Aktion werden die [ODBCDatasource-Tabelle](odbcdatasource-table.md), die [odbctranslator-Tabelle](odbctranslator-table.md)und die [odbcdriver-Tabelle](odbcdriver-table.md) für jede Datenquelle, jeden Konvertierer oder Treiber, der zum Entfernen geplant ist, abgefragt.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Für jeden installierten Treiber.



| Feld | Beschreibung der Aktions Daten               |
|-------|------------------------------------------|
| \[1\] | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers. |
| \[2\] | ComponentID                              |



 

Für jeden installierten Konvertierer.



| Feld | Beschreibung der Aktions Daten               |
|-------|------------------------------------------|
| \[1\] | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers. |
| \[2\] | ComponentID                              |



 

Für jede installierte Datenquelle.



| Feld | Beschreibung der Aktions Daten                              |
|-------|---------------------------------------------------------|
| \[1\] | Treiber Beschreibung. Der Schlüssel des ODBC-Treibers.                |
| \[2\] | ComponentID                                             |
| \[3\] | Registrierung: SQL \_ Remove \_ DSN oder SQL \_ Remove \_ sys \_ DSN |



 

## <a name="remarks"></a>Bemerkungen

Wenn sowohl die ODBC-Verwendungs Anzahl als auch die Datei Verwendungs Anzahl 0 (null) betragen, wird die Datei entfernt. Die Registrierung ist abhängig von der Verwendung von ODBC-Verwendungs Anzahlen, und das Entfernen von Dateien basiert auf freigegebenen DLLs-Schlüssel Verweis

 

 



