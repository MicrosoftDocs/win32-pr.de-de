---
description: Es gibt mehrere Möglichkeiten, um den Index mit Windows Search abzufragen. In diesem Thema werden die Ansätze für die Erweiterte Abfrage Syntax (AQS) und die Structured Query Language (SQL) beschrieben.
ms.assetid: 544f03b3-cdf8-4550-a6da-e4a3bfc44744
title: Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641bea0e6109182b5896aa1f0f981695fd91b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343260"
---
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a>Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes

Es gibt mehrere Möglichkeiten, um den Index mit Windows Search abzufragen. In diesem Thema werden die Ansätze für die Erweiterte Abfrage Syntax (AQS) und die Structured Query Language (SQL) beschrieben.

Dieses Thema ist wie folgt organisiert:

- [SQL-basierte Abfragen](#sql-based-queries)
  - [Verwenden von OLE DB](#using-ole-db)
  - [Verwenden von ADO und ADO.net](#using-ado-and-adonet)
  - [Verwenden von SQL in lokalen und Remote Abfragen](#using-sql-in-local-and-remote-queries)
- [Auf AQS basierende Abfragen](#aqs-based-queries)
  - [Verwenden von isearchqueryhelper](#using-isearchqueryhelper)
  - [Verwenden des Search-MS-Protokolls](#using-the-search-ms-protocol)
- [Zugehörige Themen](#related-topics)

## <a name="sql-based-queries"></a>SQL-basierte Abfragen

SQL ist eine Text Sprache, mit der Abfragen definiert werden. SQL ist in vielen verschiedenen Datenbanktechnologien üblich. Windows Search verwendet SQL, implementiert eine Teilmenge davon und erweitert Sie durch Hinzufügen von Elementen zur Sprache. Die von Windows Search verwendete Windows Search-SQL-Datenbank erweitert Teile der Standard Abfrage Syntax von SQL-92 und SQL-99, um den Nutzen von textbasierten Such Vorgängen zu verbessern. Alle Features von Windows Search SQL sind mit Windows Search unter Windows XP und Windows Server 2003 und höher kompatibel.

Weitere Informationen zum Verwenden der Windows Search-SQL-Syntax finden Sie unter [Abfragen des Indexes mit der SQL](-search-sql-windowssearch-entry.md) -Syntax von Windows Search und [Übersicht über die SQL-Syntax von Windows Search](-search-sql-ovwofsearchquery.md).

Die folgenden Ansätze zum Abfragen des Indexes sind SQL-basiert.

### <a name="using-ole-db"></a>Verwenden von OLE DB

Bei der Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB) handelt es sich um eine Component Object Model (com)-API, mit der Sie gleichmäßig auf verschiedene Typen von Daten speichern zugreifen können, einschließlich nicht relationaler Datenbanken wie Tabellen. OLE DB trennt den Datenspeicher von der Anwendung, die darauf zugreift, über einen Satz von Abstraktionen, die die shelldatenquelle, die Sitzung, den Befehl und die Rowsets einschließen. Ein OLE DB-Anbieter ist eine Softwarekomponente, die die OLE DB-Schnittstelle implementiert, um Daten für Anwendungen aus einem bestimmten Datenspeicher bereitzustellen.

Sie können über die OleDbConnection-und oledbsession-Objekte in C \# und mithilfe der in Active Template Library (ATL) in C++ integrierten OLE DB Unterstützung (über atlclidb. h) Programm gesteuert auf den Windows Search-OLE DB Anbieter zugreifen. Die einzige Eigenschaft, die festgelegt werden muss, ist die Anbieter Zeichenfolge.

Sie können die folgende Zeichenfolge verwenden:

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

Alternativ dazu können Sie die Verbindungs Zeichenfolge abrufen, indem Sie [**isearchqueryhelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)aufrufen. Ein Beispiel finden Sie unter Verwenden von [isearchqueryhelper](#using-isearchqueryhelper) .

> [!Note]  
> Der Windows Search-OLE DB-Anbieter ist schreibgeschützt und unterstützt SELECT-und Group on-Anweisungen. INSERT-und DELETE-Anweisungen werden nicht unterstützt.

```cpp
#include <atldbcli.h>
CDataSource cDataSource;
hr = cDataSource.OpenFromInitializationString(L"provider=Search.CollatorDSO.1;EXTENDED PROPERTIES=\"Application=Windows\"");

if (SUCCEEDED(hr))
{
    CSession cSession;
    hr = cSession.Open(cDataSource);

    if (SUCCEEDED(hr))
    {
        CCommand<CDynamicAccessor, CRowset> cCommand;
        hr = cCommand.Open(cSession, pszSQL);

        if (SUCCEEDED(hr))
        {
            for (hr = cCommand.MoveFirst(); S_OK == hr; hr = cCommand.MoveNext())
            {
                for (DBORDINAL i = 1; i <= cCommand.GetColumnCount(); i++)
                {
                    PCWSTR pszName = cCommand.GetColumnName(i);
                    // do something with the column here
                }
            }
            cCommand.Close();
        }
    }
}
```

Weitere Informationen zu OLE DB finden Sie unter [Übersicht über die OLE DB Programmierung](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx). Informationen zu den .NET Framework Datenanbieter für OLE DB finden Sie in der Dokumentation zum [System. Data. OleDb-Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .

### <a name="using-ado-and-adonet"></a>Verwenden von ADO und ADO.net

Microsoft ActiveX Data Objects (ADO) und ADO.net ermöglichen das Schreiben von Client Anwendungen, um auf Daten in einem Datenbankserver über einen Anbieter zuzugreifen und diese zu bearbeiten. Windows Search ist eine schreibgeschützte Technologie: Sie können Daten mithilfe der Desktop Suche abrufen, aber Sie können die Daten nicht mithilfe von Windows Search ändern. Sie können jedoch die Ergebnisse einer Suche an eine Technologie übergeben, die Daten ändern kann.

Die folgenden Codebeispiele veranschaulichen, wie Sie eine Verbindung mit der Datenquelle öffnen, ein Recordset mit einer [Windows Search-SQL](-search-sql-ovwofsearchquery.md) -SELECT-Anweisung erstellen und öffnen und die URLs der fünf größten Dateien aus dem Index erhalten.

> [!Note]  
> Weitere Informationen zum Abrufen der Verbindungs Zeichenfolge finden Sie unter [Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md)und [isearchqueryhelper:: get- \_ Verbindungs Zeichenfolge](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).

#### <a name="ado-and-vbscript"></a>ADO und VBScript

```VB
'To run this snippet, save it to a file and run it using cscript.exe from a command line.
'Running the .vbs file with Windows Script Host may cause dialog boxes to open for each item returned from the index.

On Error Resume Next

Set objConnection = CreateObject("ADODB.Connection")
Set objRecordSet = CreateObject("ADODB.Recordset")

objConnection.Open "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"

objRecordSet.Open "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC", objConnection

objRecordSet.MoveFirst
Do Until objRecordset.EOF
    Wscript.Echo objRecordset.Fields.Item("System.ItemPathDisplay")
    objRecordset.MoveNext
Loop
```

#### <a name="ado-and-c"></a>ADO und C++

```cpp
#import "msado15.dll" rename_namespace("ADO") rename("EOF", "EndOfFile") implementation_only

ADO::_ConnectionPtr connection = NULL;
HRESULT hr = connection.CreateInstance(__uuidof(ADO::Connection));
if (SUCCEEDED(hr))
{
    ADO::_RecordsetPtr recordset = NULL;
    hr = recordset.CreateInstance(__uuidof(ADO::Recordset));
    if (SUCCEEDED(hr))
    {
        connection->CursorLocation = ADO::adUseClient;
        hr = connection->Open(L"Provider=Search.CollatorDSO;Extended Properties='Application=Windows';",
            L"", L"", ADO::adConnectUnspecified);
        if (SUCCEEDED(hr))
        {
            hr = recordset->Open("SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX WHERE scope='file:' ORDER BY System.Size DESC",
            connection.GetInterfacePtr(), ADO::adOpenForwardOnly, ADO::adLockReadOnly, ADO::adCmdText);
            if (SUCCEEDED(hr))
            {
                while (!recordset->EndOfFile)
                {
                    _variant_t var;
                    var = recordset->Fields->GetItem(L"System.ItemPathDisplay")->GetValue();
                    std::cout << static_cast<char *>(_bstr_t(var.bstrVal)) << std::endl;
                    recordset->MoveNext();
                };
                recordset->Close();
            }
            connection->Close();
        }
    }
}

```

#### <a name="ado-and-visualbasic"></a>ADO und VisualBasic

Fügen Sie zunächst einen Verweis auf adodb in Ihrem Projekt hinzu.

```VB
Dim con As ADODB.Connection
Dim rst As ADODB.Recordset

con = New ADODB.Connection
rst = New ADODB.Recordset

Dim sConString As String
Dim sSQLString As String

sConString = "Provider=Search.CollatorDSO;Extended Properties='Application=Windows';"
con.Open(sConString)

sSQLString = "SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC"

rst = con.Execute(sSQLString)

Do Until (rst.EOF)
    Print(1, rst("System.ItemPathDisplay").Value)
    rst.MoveNext
Loop

rst.Close
rst = Nothing

con.Close
con = Nothing
```

#### <a name="adonet-and-c"></a>ADO.net und C\#

```csharp
string query = @"SELECT Top 5 System.ItemPathDisplay FROM SYSTEMINDEX
                WHERE scope='file:'
                ORDER BY System.Size DESC";

using (OleDbConnection objConnection =
    new OleDbConnection
    ("Provider=Search.CollatorDSO.1;Extended?Properties='Application=Windows';"))
{
    objConnection.Open();
    OleDbCommand cmd = new OleDbCommand(query, objConnection);
    using (OleDbDataReader rdr = cmd.ExecuteReader())
    {
        for (int i = 0; i < rdr.FieldCount; i++)
        {
            Console.Write(rdr.GetName(i));
            Console.Write('\t');
        }
        while (rdr.Read())
        {
            Console.WriteLine();
            for (int i = 0; i < rdr.FieldCount; i++)
            {
                Console.Write(rdr[i]);
                Console.Write('\t');
            }
        }
        Console.ReadKey();
    }
}
```

### <a name="using-sql-in-local-and-remote-queries"></a>Verwenden von SQL in lokalen und Remote Abfragen

Sie können Ihre Abfragen entweder lokal oder Remote ausführen. Eine lokale Abfrage mit der [from-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt. Eine lokale Abfrage fragt nur den lokalen SystemIndex-Katalog ab.

```sql
FROM SystemIndex
```

Eine Remote Abfrage mit der [from-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt. Durch das Hinzufügen von Computername wird das vorherige Beispiel in eine Remote Abfrage transformiert.

```sql
FROM [<ComputerName>.]SystemIndex
```

In Windows XP und Windows Server 2003 ist Windows Search standardmäßig nicht installiert. Nur Windows Search 4 (WS4) bietet Unterstützung für Remote Abfragen. Frühere Versionen von Windows Desktop Search (WDS), wie z. b. 3,01 und früher, unterstützen keine Remote Abfragen. Mit Windows Explorer können Sie den lokalen Index eines Remote Computers für Dateisystem Elemente (Elemente, die vom Protokoll "file:" behandelt werden) Abfragen.

Zum Abrufen eines Elements nach Remote Abfrage muss das Element die folgenden Anforderungen erfüllen:

- Kann über Universal Naming Convention (UNC)-Pfad aufgerufen werden.
- Vorhanden auf dem Remote Computer, auf den der Client Zugriff hat.
- Die Sicherheit muss festgelegt sein, damit der Client über Lesezugriff verfügen kann.

Windows-Explorer verfügt über Features zum Freigeben von Elementen, einschließlich einer öffentlichen Freigabe ( \\ \\ \\ Public \\ ...) im **Netzwerk-und Freigabe Center** und einer "Benutzer Freigabe" ( \\ \\ Computer \\ Benutzer \\ ...) für Elemente, die über den Freigabe-Assistenten freigegeben werden. Nachdem Sie die Ordner freigegeben haben, können Sie den lokalen Index Abfragen, indem Sie den Computernamen des Remote Computers in der from-Klausel und einen UNC-Pfad auf dem Remote Computer in der Scope-Klausel angeben, wie im folgenden Beispiel gezeigt:

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a>Auf AQS basierende Abfragen

AQS ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken. Obwohl AQS hauptsächlich für Benutzer steht, kann es von Entwicklern verwendet werden, um Abfragen Programm gesteuert zu erstellen. In Windows 7 wurde die kanonische AQS eingeführt und muss in Windows 7 und höher verwendet werden, um AQS-Abfragen Programm gesteuert zu generieren. Ausführliche Informationen zu AQS finden Sie unter [Programm gesteuertes verwenden der erweiterten Abfrage Syntax](-search-3x-advancedquerysyntax.md).

Die folgenden Ansätze zum Abfragen des Indexes sind AQS-basiert.

### <a name="using-isearchqueryhelper"></a>Verwenden von isearchqueryhelper

Sie können eine Komponente oder Hilfsklasse entwickeln, um den Index mithilfe der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle abzufragen. Dadurch können Sie einige Features des Systems nutzen und die Verwendung von Windows Search vereinfachen. Diese Schnittstelle unterstützt Sie dabei:

- Rufen Sie eine OLE DB Verbindungs Zeichenfolge für die Verbindung mit der Windows Search-Datenbank ab.
- Konvertieren von Benutzer Abfragen von AQS in Windows Search SQL.

Diese Schnittstelle ist als Hilfsklasse für [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) implementiert und wird durch Aufrufen von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)abgerufen, wie im folgenden C++-Beispiel gezeigt.

```cpp
HRESULT GetQueryHelper(ISearchQueryHelper **ppQueryHelper)
{
    *ppQueryHelper = NULL;

    // Create an instance of the search manager

    ISearchManager *pSearchManager;
    HRESULT hr = CoCreateInstance(__uuidof(CSearchManager), NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));
    if (SUCCEEDED(hr))
    {
        // Get the catalog manager from the search manager
        ISearchCatalogManager *pSearchCatalogManager;
        hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
        if (SUCCEEDED(hr))
        {
            // Get the query helper from the catalog manager
            hr = pSearchCatalogManager->GetQueryHelper(ppQueryHelper);
            pSearchCatalogManager->Release();
        }
        pSearchManager->Release();
    }

    return hr;
}
```

Informationen zum Implementieren der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle finden [Sie unter Verwenden der isearchqueryhelper-Schnittstelle](-search-3x-wds-qryidx-searchqueryhelper.md) und des [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Referenz Themas.

> [!Note]  
> Ältere Microsoft Windows-Desktop Suche (WDS) 2 x Kompatibilität: auf Computern, auf denen Windows XP und Windows Server 2003 und höher ausgeführt wird, ist [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) veraltet. Stattdessen sollten Entwickler [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) verwenden, um eine Verbindungs Zeichenfolge zu erhalten, die Abfrage des Benutzers in SQL zu analysieren und dann OLE DB abzufragen.

### <a name="using-the-search-ms-protocol"></a>Verwenden des Search-MS-Protokolls

Das **Search-MS-** [Anwendungsprotokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) ist eine Konvention zum Starten einer Anwendung wie Windows-Explorer, um den Windows-Suchindex abzufragen. Sie ermöglicht das Erstellen von Abfragen mit Parameter-Wert-Argumenten, einschließlich Eigenschafts Argumenten, zuvor gespeicherter Suchvorgänge, erweiterter Abfrage Syntax (AQS), natürlicher Abfrage Syntax (NQS) und Sprachcode Bezeichner (LCIDs) für den Indexer und die Abfrage selbst.

Ausführliche Informationen zur Search-MS-Protokoll Syntax finden Sie unter [Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Abfragen des Indexes mit der SQL-Syntax von Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Programm gesteuertes verwenden der erweiterten Abfrage Syntax](-search-3x-advancedquerysyntax.md)
</dt> </dl>
