---
description: Anwendungen können PDH verwenden, um Leistungsindikatoren aus SQL Protokollen zu extrahieren, oder sie können formatierte oder unformatierte Leistungsindikatoren direkt aus der Datenbank über SQL Abfragen extrahieren.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL Protokolldateischema
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a95026c478094d8e71a44c2c57e65c2fa7044b00e982ea43187244838beed2ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143813"
---
# <a name="sql-log-file-schema"></a>SQL Protokolldateischema

> [!IMPORTANT]
> Die PDH-Unterstützung für ODBC SQL Datenbanken kann in Zukunft geändert oder nicht mehr verfügbar sein.

Anwendungen können PDH-APIs verwenden, um Leistungsindikatordaten in kompatiblen ODBC SQL-Datenbanken zu lesen und zu schreiben, und dann eine weitere Verarbeitung über SQL Abfragen durchführen. In diesem Abschnitt wird das SQL Schema beschrieben, das zum Speichern von Leistungsindikatoren verwendet wird. Sie können diese Informationen verwenden, um benutzerdefinierte Ansichten und Berichte zu erstellen. Das Schema besteht aus den folgenden drei Tabellen:

- [**Counterdata**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> Die PDH-Unterstützung für ODBC SQL-Datenbanken funktioniert nur mit ODBC SQL-Treibern, die [BCP-Erweiterungen (Bulk Copy)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions)unterstützen.
