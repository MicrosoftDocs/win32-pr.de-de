---
description: Anwendungen können PDH zum Extrahieren von Leistungsindikatoren aus SQL-Protokollen verwenden, oder Sie können formatierte oder unformatierte Leistungsindikatoren direkt aus der Datenbank mithilfe von SQL-Abfragen extrahieren.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL-Protokolldatei Schema
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357752"
---
# <a name="sql-log-file-schema"></a>SQL-Protokolldatei Schema

> [!IMPORTANT]
> PDH-Unterstützung für ODBC-SQL-Datenbanken kann in Zukunft geändert oder nicht mehr verfügbar sein.

Anwendungen können PDH-APIs für Lese-und Schreibvorgänge von Leistungsdaten in kompatiblen ODBC-SQL-Datenbanken verwenden und dann mithilfe von SQL-Abfragen weitere Verarbeitung ausführen. In diesem Abschnitt wird das SQL-Schema zum Speichern von Leistungsindikatoren beschrieben. Sie können diese Informationen zum Erstellen von benutzerdefinierten Ansichten und Berichten verwenden. Das Schema besteht aus den folgenden drei Tabellen:

- [**Gegen Daten**](counterdata.md)
- [**Counter Details**](counterdetails.md)
- [**Display toid**](displaytoid.md)

> [!NOTE]
> PDH-Unterstützung für ODBC-SQL-Datenbanken funktioniert nur mit ODBC-SQL-Treibern, die [Massen Kopier Erweiterungen (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)unterstützen.
