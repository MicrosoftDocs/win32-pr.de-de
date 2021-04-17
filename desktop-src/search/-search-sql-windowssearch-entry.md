---
description: Windows Search stellt Content-crawlen und Suchfunktionen bereit, die die Volltextsuche unterstützen. Die von Windows Search verwendete Abfragesprache erweitert die standardmäßige SQL-92-und SQL-99-Datenbankabfrage Syntax, um die Nützlichkeit durch textbasierte Suchvorgänge zu verbessern.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Abfragen des Indexes mit der SQL-Syntax von Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484411"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Abfragen des Indexes mit der SQL-Syntax von Windows Search

Windows Search stellt Content-crawlen und Suchfunktionen bereit, die die Volltextsuche unterstützen. Die von Windows Search verwendete Abfragesprache erweitert die standardmäßige SQL-92-und SQL-99-Datenbankabfrage Syntax, um die Nützlichkeit durch textbasierte Suchvorgänge zu verbessern.

Alle Features von Windows Search Structured Query Language (SQL) sind mit Windows Search unter Windows Vista und höher kompatibel, einschließlich aller Versionen von Windows 10.

Dieser Abschnitt enthält eine Übersicht über die SQL-Syntax in Windows Search und enthält die folgenden Themen:

- [Übersicht über die SQL-Syntax von Windows Search](-search-sql-ovwofsearchquery.md)
- [Allgemeine Informationen zur Abfragesprache](-search-sql-generalqueryinfo.md)
- [Gruppieren nach... Über... An](-search-sql-group-on-over.md)
- [SELECT-Anweisung](-search-sql-select.md)
- [FROM-Klausel](-search-sql-from.md)
- [WHERE-Klausel](-search-sql-where.md)
- [Order By-Klausel](-search-sql-orderby.md)
- [Rank by-Klausel](-search-sql-rankby.md)
- [Set-Anweisung](-search-sql-set.md)
- [Rowset-Eigenschaften](-search-sql-rowset-properties.md)

In dieser Dokumentation wird davon ausgegangen, dass Sie mit dem Objekt Verknüpfungs-und Einbetten von Datenbanken (OLE DB)

## <a name="code-samples"></a>Codebeispiele

Das wssql-Codebeispiel veranschaulicht die Kommunikation zwischen Microsoft OLE DB und Windows Search über SQL. Das wsoledb-Codebeispiel veranschaulicht Active Template Library (ATL)-OLE DB Zugriff auf Windows Search-Anwendungen und zwei zusätzliche Methoden zum Abrufen von Ergebnissen aus Windows Search. Beide Beispiele sind in den [Windows-Such Beispielen](-search-samples-ovw.md) und im [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk) verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

[Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)

[Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)

[Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md)

[Abfragen des Indexes mit der SQL-Syntax von Windows Search](-search-sql-windowssearch-entry.md)

[Programm gesteuertes verwenden der erweiterten Abfrage Syntax](-search-3x-advancedquerysyntax.md)
