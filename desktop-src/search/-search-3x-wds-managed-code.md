---
description: Das Windows Search SDK stellt eine Interoperabilität Assembly bereit, damit Sie mit Component Object Model (com)-Objekten arbeiten können, die von Windows Search und anderen Programmen für die Schnittstellen und Klassen mit verwaltetem Code verfügbar gemacht werden.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Verwenden von verwaltetem Code mit Shelldaten und Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128608"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a>Verwenden von verwaltetem Code mit Shelldaten und Windows Search

Das Windows Search SDK stellt eine Interoperabilität Assembly bereit, damit Sie mit Component Object Model (com)-Objekten arbeiten können, die von Windows Search und anderen Programmen für die Schnittstellen und Klassen mit verwaltetem Code verfügbar gemacht werden. Die Interoperabilität-Assembly wird von Microsoft digital signiert und kann mit den [Windows-Such Beispielen](-search-samples-ovw.md)gefunden werden.

Dieses Thema ist wie folgt organisiert:

-   [Verwenden der Windows-API-codepack](#using-the-windows-api-codepack)
    -   [Zugreifen auf Index Ergebnisse](#accessing-index-results)
    -   [Beispielanwendung mit der Windows-API-codepack](#sample-application-using-the-windows-api-codepack)
-   [Zugehörige Themen](#related-topics)

## <a name="using-the-windows-api-codepack"></a>Verwenden der Windows-API-codepack

Wenn Sie in der Microsoft .NET-Umgebung arbeiten, verwenden Sie das [Windows-API-Code Paket für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) , um Suchergebnisse zu erhalten, oder Durchsuchen Sie einfach den-Namespace. Das [Windows-API-Code Paket für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) stellt eine Sammlung von shellelementen bereit, die im Grunde Wrapper um die native [IShellItem-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)sind. Sie können diese Auflistung durchlaufen und die verschiedenen Eigenschaftswerte auf ähnliche Weise wie die Ergebnisse in einer Tabelle aus einer Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB) aufzählen.

Der folgende Code Ausschnitt veranschaulicht, wie Sie Such Elemente durchlaufen und die Eigenschaftswerte für jedes Element abrufen können.


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a>Zugreifen auf Index Ergebnisse

Sie können entweder über OLE DB oder das shelldatenmodell auf Index Ergebnisse zugreifen. Bei beiden Ansätzen gibt es vor-und Nachteile. Ein Vorteil besteht darin, dass OLE DB und Structured Query Language (SQL) den Daten Bank Programmierern vertraut sind. Andere Vorteile sind eine bessere Kontrolle über die Leistung, wenn nur der Indexer abgefragt wird, sowie der Zugriff auf zusätzliche Funktionen, wie z. b. die Möglichkeit, vorherige Ergebnisse schnell in einem neuen Rowset zu finden.

Der Vorteil des shelldatenmodells besteht darin, dass es sich über verschiedene Informationsquellen wie z. b. OpenSearch zusammenfasst und den Zugriff auf zusätzliche Funktionen ermöglicht, wie z. b. Miniaturansichten und Eigenschaften Handler. Außerdem erfordert das shellobjektmodell keine besondere Unterstützung für nicht-Dateinamen, wie z. b. e-Mail-Elemente und OneNote-Ergebnisse, sowie für Elemente, die sich im Index des Benutzers befinden. Beachten Sie, dass in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) der bekannte Ordner Bereich für lokale indizierte Inhalte ist. Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

OpenSearch-Datenquellen werden nicht über OLE DB für die Verbund Suche in Windows 7 und höher verfügbar gemacht. Aus diesem Grund empfiehlt es sich, einen LINQ-Anbieter für den Shellnamespace zu schreiben, anstatt OLE DB für den Zugriff auf die indexerergebnisse zu verwenden. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines iquerable LINQ-Anbieters](/previous-versions/bb546158(v=vs.140)).

### <a name="sample-application-using-the-windows-api-codepack"></a>Beispielanwendung mit der Windows-API-codepack

Der folgende Screenshot zeigt ein Mock einer Beispielanwendung, die mit dem [Windows-API-Code Pack für Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility)erstellt wurde.

![Screenshot der Media Player-Anwendung mit e-Mail-Nachrichten](images/folderid-searchhome.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Verbundsuche in Windows 10](-search-federated-search-overview.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Sprachübergreifende Interoperabilität](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))
</dt> </dl>

 

 
