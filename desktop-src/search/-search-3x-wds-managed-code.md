---
description: Das Windows Search SDK bietet eine Inopierbarkeitsassembly für die Arbeit mit com-Objekten (Component Object Model), die von Windows Search und anderen Programmen für die Schnittstellen und Klassen mit verwaltetem Code verfügbar gemacht werden.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Verwenden von verwaltetem Code mit Shelldaten und Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26276236c2dee056f603d359a89560e9b1ce9e06b0b3f1cfed2c68f77b0b0eae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118052242"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Verwenden von verwaltetem Code mit Shelldaten und Windows Search

Das Windows Search SDK bietet eine Inopierbarkeitsassembly für die Arbeit mit com-Objekten (Component Object Model), die von Windows Search und anderen Programmen für die Schnittstellen und Klassen mit verwaltetem Code verfügbar gemacht werden. Die Interopability-Assembly wird digital von Microsoft signiert und befindet sich in den [Windows Search-Beispielen.](-search-samples-ovw.md)

Dieses Thema ist wie folgt organisiert:

-   [Verwenden des codePack der Windows-API](#using-the-windows-api-codepack)
    -   [Zugreifen auf Indexergebnisse](#accessing-index-results)
    -   [Beispielanwendung mit dem Windows-API-Codepack](#sample-application-using-the-windows-api-codepack)
-   [Zugehörige Themen](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Verwenden des codePack der Windows-API

Wenn Sie in der Microsoft .NET-Umgebung arbeiten, verwenden Sie das [Windows API Code Pack für Microsoft .NET Framework,](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) um Suchergebnisse abzurufen, oder durchsuchen Sie einfach den Namespace. Das [Windows API Code Pack für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) bietet Ihnen eine Sammlung von Shellelementen, die im Wesentlichen Wrapper um die native [IShellItem-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)sind. Sie können diese Auflistung iterieren und die verschiedenen Eigenschaftswerte auf ähnliche Weise abrufen, wie Sie die Ergebnisse in einer Tabelle aus einer Object Linking and Embedding-Datenbank -Abfrage (OLE DB) aufzählen würden.

Der folgende Codeausschnitt veranschaulicht das Iterieren von Suchelementen und das Abrufen der jeweiligen Eigenschaftswerte.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Zugreifen auf Indexergebnisse

Sie können entweder über OLE DB oder das Shell-Datenmodell auf Indexergebnisse zugreifen. Bei beiden Ansätzen gibt es Vor- und Nachteile. Ein Vorteil besteht darin, dass datenbankprogrammierern OLE DB und strukturierte Abfragesprache (SQL) vertraut sind. Weitere Vorteile sind eine bessere Kontrolle über die Leistung, wenn nur der Indexer abgefragt wird, und der Zugriff auf zusätzliche Funktionen, z. B. die Möglichkeit, vorherige Ergebnisse schnell in einem neuen Rowset zu finden.

Der Vorteil des Shell-Datenmodells besteht darin, dass es verschiedene Informationsquellen wie OpenSearch abstrahiert und Zugriff auf zusätzliche Funktionen wie Miniaturansichten und Eigenschaftenhandler bietet. Das Shell-Objektmodell erfordert auch keine Sonderfallunterstützung für Nicht-Dateinamenergebnisse wie E-Mail-Elemente und OneNote Ergebnisse, noch für Elemente, die sich im Index des Benutzers befinden. Beachten Sie, dass in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) der bekannte Ordnerbereich für lokalen indizierten Inhalt ist. Weitere Informationen zum Erstellen einer Shell-Datenquelle finden Sie unter [Implementieren der grundlegenden Ordnerobjektschnittstellen.](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))

OpenSearch Datenquellen werden in Windows 7 und höher nicht über OLE DB für die Verbundsuche verfügbar gemacht. Aus diesem Grund wird empfohlen, einen LINQ-Anbieter für den Shellnamespace zu schreiben, anstatt OLE DB zu verwenden, um auf die Indexerergebnisse zuzugreifen. Weitere Informationen finden Sie unter [Exemplarische Vorgehensweise: Erstellen eines IQueryable LINQ-Anbieters.](/previous-versions/bb546158(v=vs.140))

### <a name="sample-application-using-the-windows-api-codepack"></a>Beispielanwendung mit dem Windows-API-Codepack

Der folgende Screenshot zeigt ein Modell einer Beispielanwendung, die mit dem [Windows API Code Pack für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)erstellt wurde.

![Screenshot der Media Player-Anwendung mit E-Mail-Nachrichten](images/folderid-searchhome.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Konzeptionellen**
</dt> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Sprachübergreifende Interoperabilität](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
