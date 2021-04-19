---
description: Es gibt mehrere Möglichkeiten, um den Index mit Windows Search abzufragen.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Programm gesteuertes Abfragen des Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6390b31f4a1cc01ca723978a5107d5d9a502c4ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348354"
---
# <a name="querying-the-index-programmatically"></a>Programm gesteuertes Abfragen des Indexes

Es gibt mehrere Möglichkeiten, um den Index mit Windows Search abzufragen.

Dieser Abschnitt enthält das konzeptionelle Framework zum programmgesteuerten Abfragen des Indexes:

-   [Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes](using-sql-and-aqs-to-query-the-index.md)
-   [Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md)
-   [Abfragen des Indexes mit der SQL-Syntax von Windows Search](-search-sql-windowssearch-entry.md)
-   [Programm gesteuertes verwenden der erweiterten Abfrage Syntax](-search-3x-advancedquerysyntax.md)

> [!Note]  
> Ältere Microsoft Windows-Desktop Suche (WDS) 2 x Kompatibilität: auf Computern, auf denen Windows XP und höher ausgeführt wird, ist [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) veraltet. Stattdessen sollten Entwickler [**isearchqueryhelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) verwenden, um eine Verbindungs Zeichenfolge zu erhalten und die Abfrage des Benutzers in Structured Query Language (SQL) zu analysieren und dann eine Abfrage über die Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB) durchführen.

 

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zu OLE DB finden Sie unter Übersicht über die [OLE DB Programmierung](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx). Informationen zu den .NET Framework Datenanbieter für OLE DB finden Sie unter [System. Data. OleDb-Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1).
-   Weitere Hintergrundinformationen zur Verwendung von Eigenschaften beim Abfragen finden Sie in den folgenden Themen:
    -   [Eigenschaften System](../properties/building-property-handlers.md)
    -   [System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Weitere Informationen zum Erstellen und Ändern von Suchordnern finden Sie unter [**isearchfolderitemfactory-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   Informationen zu den von der Community unterstützten Frage-und Diskussions Nachrichten für Suchtechnologien finden Sie im [MSDN-Forum: Entwicklung von Windows-Desktop-suchen](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   So laden Sie die Code Beispiele für das Search SDK herunter:
    -   Für Windows 7: [Beispiele für Windows-Suche auf GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Für Windows Vista: [Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   So laden Sie die Windows SDK herunter:
    -   Für Windows 7: [Windows SDK für Windows 7 und .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Für Windows Vista: [Windows SDK für Windows Vista und .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwicklungs Leit Faden für Windows-Suche](-search-developers-guide-entry-page.md)
</dt> <dt>

[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Erweitern des Windows-Suchindexes](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
