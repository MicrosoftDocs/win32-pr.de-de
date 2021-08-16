---
description: Es gibt mehrere Möglichkeiten, den Index mithilfe Windows Search abfragt.
ms.assetid: 2c161b7f-4e28-4e8a-add6-3c1cda00a622
title: Programm gesteuertes Abfragen des Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76f98d12e4a0615bf19dfb165766a67b8c9e58700ad2d0c897782e2a16ba9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094941"
---
# <a name="querying-the-index-programmatically"></a>Programm gesteuertes Abfragen des Indexes

Es gibt mehrere Möglichkeiten, den Index mithilfe Windows Search abfragt.

Dieser Abschnitt enthält das konzeptionelle Framework zum programmgesteuerten Abfragen des Indexes:

-   [Verwenden SQL und AQS-Ansätzen zum Abfragen des Indexes](using-sql-and-aqs-to-query-the-index.md)
-   [Abfragen des Index mit ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
-   [Abfragen des Indexes mit dem search-ms-Protokoll](-search-3x-wds-qryidx-searchms.md)
-   [Abfragen des Indexes mit Windows Search SQL Syntax](-search-sql-windowssearch-entry.md)
-   [Programmgesteuertes Verwenden der erweiterten Abfragesyntax](-search-3x-advancedquerysyntax.md)

> [!Note]  
> 2-fache Kompatibilität von Microsoft Windows Desktop Search (WDS): Auf Computern mit Windows XP und höher ist [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) veraltet. Stattdessen sollten Entwickler [**ISearchQueryHelper**](/windows/win32/api/Searchapi/nn-searchapi-isearchqueryhelper) verwenden, um eine Verbindungszeichenfolge zu erhalten und die Abfrage des Benutzers in strukturierte Abfragesprache (SQL) zu analysieren und dann über Object Linking and Embedding-Datenbank (OLE DB) abfragen.

 

## <a name="additional-resources"></a>Weitere Ressourcen

-   Weitere Informationen zu OLE DB finden Sie unter OLE DB Programming Overview ( Übersicht [über die Programmierung).](https://msdn.microsoft.com/library/Cc522830(v=VS.71).aspx) Informationen zum .NET Framework Datenanbieter für OLE DB finden Sie im [System.Data.OleDb-Namespace.](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1)
-   Weitere Hintergrundinformationen zur Verwendung von Eigenschaften bei Abfragen finden Sie in den folgenden Themen:
    -   [Eigenschaftensystem](../properties/building-property-handlers.md)
    -   [Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
-   Informationen zum Erstellen und Ändern von Suchordnern finden Sie unter [**ISearchFolderItemFactory-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory).
-   Von der Community unterstützte Frage- und Diskussionsnachrichtenboards zu Suchtechnologien finden Sie im [MSDN-Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
-   So laden Sie die Codebeispiele für das Search SDK herunter:
    -   Weitere Windows 7: [Windows Unter "Suchbeispiele" GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch)
    -   Beispiele Windows Vista: [Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
-   So laden Sie das Windows SDK herunter:
    -   Weitere Windows 7: [Windows SDK für Windows 7 und .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
    -   Für Windows Vista: [Windows SDK für Windows Vista und .NET Framework](https://www.microsoft.com/download/details.aspx?id=31950)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Search Development Guide](-search-developers-guide-entry-page.md)
</dt> <dt>

[Verwalten des Indexes](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[Erweitern des Windows Search Index](-search-3x-wds-extidx-overview.md)
</dt> <dt>

[Erweitern von Sprachressourcen](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
