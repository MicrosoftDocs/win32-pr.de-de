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
# <a name="using-sql-and-aqs-approaches-to-query-the-index"></a><span data-ttu-id="12e96-104">Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="12e96-104">Using SQL and AQS Approaches to Query the Index</span></span>

<span data-ttu-id="12e96-105">Es gibt mehrere Möglichkeiten, um den Index mit Windows Search abzufragen.</span><span class="sxs-lookup"><span data-stu-id="12e96-105">There are several ways to use Windows Search to query the index.</span></span> <span data-ttu-id="12e96-106">In diesem Thema werden die Ansätze für die Erweiterte Abfrage Syntax (AQS) und die Structured Query Language (SQL) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="12e96-106">This topic outlines Advanced Query Syntax (AQS) and Structured Query Language (SQL) based approaches.</span></span>

<span data-ttu-id="12e96-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="12e96-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="12e96-108">SQL-basierte Abfragen</span><span class="sxs-lookup"><span data-stu-id="12e96-108">SQL Based Queries</span></span>](#sql-based-queries)
  - [<span data-ttu-id="12e96-109">Verwenden von OLE DB</span><span class="sxs-lookup"><span data-stu-id="12e96-109">Using OLE DB</span></span>](#using-ole-db)
  - [<span data-ttu-id="12e96-110">Verwenden von ADO und ADO.net</span><span class="sxs-lookup"><span data-stu-id="12e96-110">Using ADO and ADO.NET</span></span>](#using-ado-and-adonet)
  - [<span data-ttu-id="12e96-111">Verwenden von SQL in lokalen und Remote Abfragen</span><span class="sxs-lookup"><span data-stu-id="12e96-111">Using SQL in Local and Remote Queries</span></span>](#using-sql-in-local-and-remote-queries)
- [<span data-ttu-id="12e96-112">Auf AQS basierende Abfragen</span><span class="sxs-lookup"><span data-stu-id="12e96-112">AQS Based Queries</span></span>](#aqs-based-queries)
  - [<span data-ttu-id="12e96-113">Verwenden von isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="12e96-113">Using ISearchQueryHelper</span></span>](#using-isearchqueryhelper)
  - [<span data-ttu-id="12e96-114">Verwenden des Search-MS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="12e96-114">Using the search-ms Protocol</span></span>](#using-the-search-ms-protocol)
- [<span data-ttu-id="12e96-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12e96-115">Related topics</span></span>](#related-topics)

## <a name="sql-based-queries"></a><span data-ttu-id="12e96-116">SQL-basierte Abfragen</span><span class="sxs-lookup"><span data-stu-id="12e96-116">SQL Based Queries</span></span>

<span data-ttu-id="12e96-117">SQL ist eine Text Sprache, mit der Abfragen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="12e96-117">SQL is a text language that defines queries.</span></span> <span data-ttu-id="12e96-118">SQL ist in vielen verschiedenen Datenbanktechnologien üblich.</span><span class="sxs-lookup"><span data-stu-id="12e96-118">SQL is common across many different database technologies.</span></span> <span data-ttu-id="12e96-119">Windows Search verwendet SQL, implementiert eine Teilmenge davon und erweitert Sie durch Hinzufügen von Elementen zur Sprache.</span><span class="sxs-lookup"><span data-stu-id="12e96-119">Windows Search uses SQL, implements a subset of it, and extends it by adding elements to the language.</span></span> <span data-ttu-id="12e96-120">Die von Windows Search verwendete Windows Search-SQL-Datenbank erweitert Teile der Standard Abfrage Syntax von SQL-92 und SQL-99, um den Nutzen von textbasierten Such Vorgängen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="12e96-120">The Windows Search SQL used by Windows Search extends portions of the standard SQL-92 and SQL-99 database query syntax to enhance its usefulness with text-based searches.</span></span> <span data-ttu-id="12e96-121">Alle Features von Windows Search SQL sind mit Windows Search unter Windows XP und Windows Server 2003 und höher kompatibel.</span><span class="sxs-lookup"><span data-stu-id="12e96-121">All features of Windows Search SQL are compatible with Windows Search on Windows XP and Windows Server 2003, and later.</span></span>

<span data-ttu-id="12e96-122">Weitere Informationen zum Verwenden der Windows Search-SQL-Syntax finden Sie unter [Abfragen des Indexes mit der SQL](-search-sql-windowssearch-entry.md) -Syntax von Windows Search und [Übersicht über die SQL-Syntax von Windows Search](-search-sql-ovwofsearchquery.md).</span><span class="sxs-lookup"><span data-stu-id="12e96-122">For more information about using Windows Search SQL syntax, see [Querying the Index with Windows Search SQL Syntax](-search-sql-windowssearch-entry.md) and [Overview of Windows Search SQL Syntax](-search-sql-ovwofsearchquery.md).</span></span>

<span data-ttu-id="12e96-123">Die folgenden Ansätze zum Abfragen des Indexes sind SQL-basiert.</span><span class="sxs-lookup"><span data-stu-id="12e96-123">The following approaches for querying the index are SQL based.</span></span>

### <a name="using-ole-db"></a><span data-ttu-id="12e96-124">Verwenden von OLE DB</span><span class="sxs-lookup"><span data-stu-id="12e96-124">Using OLE DB</span></span>

<span data-ttu-id="12e96-125">Bei der Objekt Verknüpfungs-und Einbettungs Datenbank (OLE DB) handelt es sich um eine Component Object Model (com)-API, mit der Sie gleichmäßig auf verschiedene Typen von Daten speichern zugreifen können, einschließlich nicht relationaler Datenbanken wie Tabellen.</span><span class="sxs-lookup"><span data-stu-id="12e96-125">The Object Linking and Embedding Database (OLE DB) is a Component Object Model (COM) API that enables you to access different types of data stores uniformly, including non-relational databases like spreadsheets.</span></span> <span data-ttu-id="12e96-126">OLE DB trennt den Datenspeicher von der Anwendung, die darauf zugreift, über einen Satz von Abstraktionen, die die shelldatenquelle, die Sitzung, den Befehl und die Rowsets einschließen.</span><span class="sxs-lookup"><span data-stu-id="12e96-126">OLE DB separates the data store from the application accessing it through a set of abstractions that include the Shell data source, session, command, and rowsets.</span></span> <span data-ttu-id="12e96-127">Ein OLE DB-Anbieter ist eine Softwarekomponente, die die OLE DB-Schnittstelle implementiert, um Daten für Anwendungen aus einem bestimmten Datenspeicher bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="12e96-127">An OLE DB provider is a software component that implements the OLE DB interface to provide data to applications from a particular data store.</span></span>

<span data-ttu-id="12e96-128">Sie können über die OleDbConnection-und oledbsession-Objekte in C \# und mithilfe der in Active Template Library (ATL) in C++ integrierten OLE DB Unterstützung (über atlclidb. h) Programm gesteuert auf den Windows Search-OLE DB Anbieter zugreifen.</span><span class="sxs-lookup"><span data-stu-id="12e96-128">You can access the Windows Search OLE DB provider programmatically by using the OleDbConnection and OleDbSession objects in C\# and by using the OLE DB support built into Active Template Library (ATL) in C++ (via atlclidb.h).</span></span> <span data-ttu-id="12e96-129">Die einzige Eigenschaft, die festgelegt werden muss, ist die Anbieter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="12e96-129">The only property that has to be set is the provider string.</span></span>

<span data-ttu-id="12e96-130">Sie können die folgende Zeichenfolge verwenden:</span><span class="sxs-lookup"><span data-stu-id="12e96-130">You can use the following string:</span></span>

`provider=Search.CollatorDSO;EXTENDED PROPERTIES="Application=Windows"`

<span data-ttu-id="12e96-131">Alternativ dazu können Sie die Verbindungs Zeichenfolge abrufen, indem Sie [**isearchqueryhelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="12e96-131">Alternatively, you can get the connection string by calling [**ISearchQueryHelper::get\_ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span> <span data-ttu-id="12e96-132">Ein Beispiel finden Sie unter Verwenden von [isearchqueryhelper](#using-isearchqueryhelper) .</span><span class="sxs-lookup"><span data-stu-id="12e96-132">See Using [ISearchQueryHelper](#using-isearchqueryhelper) for an example.</span></span>

> [!Note]  
> <span data-ttu-id="12e96-133">Der Windows Search-OLE DB-Anbieter ist schreibgeschützt und unterstützt SELECT-und Group on-Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="12e96-133">The Windows Search OLE DB provider is read-only, and support SELECT and GROUP ON statements.</span></span> <span data-ttu-id="12e96-134">INSERT-und DELETE-Anweisungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12e96-134">INSERT and DELETE statements are not supported.</span></span>

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

<span data-ttu-id="12e96-135">Weitere Informationen zu OLE DB finden Sie unter [Übersicht über die OLE DB Programmierung](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="12e96-135">For more information on OLE DB, see [OLE DB Programming Overview](https://msdn.microsoft.com/library/5d8sd9we(VS.71).aspx).</span></span> <span data-ttu-id="12e96-136">Informationen zu den .NET Framework Datenanbieter für OLE DB finden Sie in der Dokumentation zum [System. Data. OleDb-Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) .</span><span class="sxs-lookup"><span data-stu-id="12e96-136">For information on the .NET Framework Data Provider for OLE DB, see the [System.Data.OleDb Namespace](/dotnet/api/system.data.oledb?view=dotnet-plat-ext-3.1) documentation.</span></span>

### <a name="using-ado-and-adonet"></a><span data-ttu-id="12e96-137">Verwenden von ADO und ADO.net</span><span class="sxs-lookup"><span data-stu-id="12e96-137">Using ADO and ADO.NET</span></span>

<span data-ttu-id="12e96-138">Microsoft ActiveX Data Objects (ADO) und ADO.net ermöglichen das Schreiben von Client Anwendungen, um auf Daten in einem Datenbankserver über einen Anbieter zuzugreifen und diese zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="12e96-138">Microsoft ActiveX Data Objects (ADO) and ADO.NET enable you to write client applications to access and manipulate data in a database server through a provider.</span></span> <span data-ttu-id="12e96-139">Windows Search ist eine schreibgeschützte Technologie: Sie können Daten mithilfe der Desktop Suche abrufen, aber Sie können die Daten nicht mithilfe von Windows Search ändern.</span><span class="sxs-lookup"><span data-stu-id="12e96-139">Windows Search is a read-only technology: you can retrieve data using Desktop Search but you can't change data using Windows Search.</span></span> <span data-ttu-id="12e96-140">Sie können jedoch die Ergebnisse einer Suche an eine Technologie übergeben, die Daten ändern kann.</span><span class="sxs-lookup"><span data-stu-id="12e96-140">You can, however, pass the results of a search over to a technology that can change data.</span></span>

<span data-ttu-id="12e96-141">Die folgenden Codebeispiele veranschaulichen, wie Sie eine Verbindung mit der Datenquelle öffnen, ein Recordset mit einer [Windows Search-SQL](-search-sql-ovwofsearchquery.md) -SELECT-Anweisung erstellen und öffnen und die URLs der fünf größten Dateien aus dem Index erhalten.</span><span class="sxs-lookup"><span data-stu-id="12e96-141">The following code examples demonstrate how to open a connection to the data source, create and open a RecordSet with a [Windows Search SQL](-search-sql-ovwofsearchquery.md) SELECT statement, and get the URLs of the five largest files from the index.</span></span>

> [!Note]  
> <span data-ttu-id="12e96-142">Weitere Informationen zum Abrufen der Verbindungs Zeichenfolge finden Sie unter [Abfragen des Indexes mit isearchqueryhelper](-search-3x-wds-qryidx-searchqueryhelper.md)und [isearchqueryhelper:: get- \_ Verbindungs Zeichenfolge](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span><span class="sxs-lookup"><span data-stu-id="12e96-142">For information on how to obtain the connection string, see [Querying the Index with ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md), and [ISearchQueryHelper::get\_Connection String](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring).</span></span>

#### <a name="ado-and-vbscript"></a><span data-ttu-id="12e96-143">ADO und VBScript</span><span class="sxs-lookup"><span data-stu-id="12e96-143">ADO and VBScript</span></span>

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

#### <a name="ado-and-c"></a><span data-ttu-id="12e96-144">ADO und C++</span><span class="sxs-lookup"><span data-stu-id="12e96-144">ADO and C++</span></span>

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

#### <a name="ado-and-visualbasic"></a><span data-ttu-id="12e96-145">ADO und VisualBasic</span><span class="sxs-lookup"><span data-stu-id="12e96-145">ADO and VisualBasic</span></span>

<span data-ttu-id="12e96-146">Fügen Sie zunächst einen Verweis auf adodb in Ihrem Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="12e96-146">First add a reference to ADODB in your project</span></span>

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

#### <a name="adonet-and-c"></a><span data-ttu-id="12e96-147">ADO.net und C\#</span><span class="sxs-lookup"><span data-stu-id="12e96-147">ADO.NET and C\#</span></span>

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

### <a name="using-sql-in-local-and-remote-queries"></a><span data-ttu-id="12e96-148">Verwenden von SQL in lokalen und Remote Abfragen</span><span class="sxs-lookup"><span data-stu-id="12e96-148">Using SQL in Local and Remote Queries</span></span>

<span data-ttu-id="12e96-149">Sie können Ihre Abfragen entweder lokal oder Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="12e96-149">You can execute your queries either locally or remotely.</span></span> <span data-ttu-id="12e96-150">Eine lokale Abfrage mit der [from-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="12e96-150">A local query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="12e96-151">Eine lokale Abfrage fragt nur den lokalen SystemIndex-Katalog ab.</span><span class="sxs-lookup"><span data-stu-id="12e96-151">A local query queries the local SystemIndex catalog only.</span></span>

```sql
FROM SystemIndex
```

<span data-ttu-id="12e96-152">Eine Remote Abfrage mit der [from-Klausel](-search-sql-from.md) wird im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="12e96-152">A remote query using the [FROM clause](-search-sql-from.md) is shown in the following example.</span></span> <span data-ttu-id="12e96-153">Durch das Hinzufügen von Computername wird das vorherige Beispiel in eine Remote Abfrage transformiert.</span><span class="sxs-lookup"><span data-stu-id="12e96-153">Adding ComputerName transforms the previous example into a remote query.</span></span>

```sql
FROM [<ComputerName>.]SystemIndex
```

<span data-ttu-id="12e96-154">In Windows XP und Windows Server 2003 ist Windows Search standardmäßig nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="12e96-154">By default, Windows XP and Windows Server 2003 do not have Windows Search installed.</span></span> <span data-ttu-id="12e96-155">Nur Windows Search 4 (WS4) bietet Unterstützung für Remote Abfragen.</span><span class="sxs-lookup"><span data-stu-id="12e96-155">Only Windows Search 4 (WS4) provides remote query support.</span></span> <span data-ttu-id="12e96-156">Frühere Versionen von Windows Desktop Search (WDS), wie z. b. 3,01 und früher, unterstützen keine Remote Abfragen.</span><span class="sxs-lookup"><span data-stu-id="12e96-156">Previous versions of Windows Desktop Search (WDS), such as 3.01 and earlier, do not support remote querying.</span></span> <span data-ttu-id="12e96-157">Mit Windows Explorer können Sie den lokalen Index eines Remote Computers für Dateisystem Elemente (Elemente, die vom Protokoll "file:" behandelt werden) Abfragen.</span><span class="sxs-lookup"><span data-stu-id="12e96-157">With Windows Explorer you can query the local index of a remote computer for file system items (items handled by the "file:" protocol).</span></span>

<span data-ttu-id="12e96-158">Zum Abrufen eines Elements nach Remote Abfrage muss das Element die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="12e96-158">To retrieve an item by remote query, the item must meet the following requirements:</span></span>

- <span data-ttu-id="12e96-159">Kann über Universal Naming Convention (UNC)-Pfad aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="12e96-159">Be accessible via Universal Naming Convention (UNC) path.</span></span>
- <span data-ttu-id="12e96-160">Vorhanden auf dem Remote Computer, auf den der Client Zugriff hat.</span><span class="sxs-lookup"><span data-stu-id="12e96-160">Exist on the remote computer to which the client has access.</span></span>
- <span data-ttu-id="12e96-161">Die Sicherheit muss festgelegt sein, damit der Client über Lesezugriff verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="12e96-161">Have its security set to allow the client to have Read access.</span></span>

<span data-ttu-id="12e96-162">Windows-Explorer verfügt über Features zum Freigeben von Elementen, einschließlich einer öffentlichen Freigabe ( \\ \\ \\ Public \\ ...) im **Netzwerk-und Freigabe Center** und einer "Benutzer Freigabe" ( \\ \\ Computer \\ Benutzer \\ ...) für Elemente, die über den Freigabe-Assistenten freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="12e96-162">Windows Explorer has features for sharing items including a "Public" share (\\\\Machine\\Public\\...) in the **Network and Sharing Center**, and a "Users" share (\\\\Machine\\Users\\...) for items shared through the Sharing Wizard.</span></span> <span data-ttu-id="12e96-163">Nachdem Sie die Ordner freigegeben haben, können Sie den lokalen Index Abfragen, indem Sie den Computernamen des Remote Computers in der from-Klausel und einen UNC-Pfad auf dem Remote Computer in der Scope-Klausel angeben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="12e96-163">After you share the folder(s), you can query the local index by specifying the remote computer's machine name in the FROM clause, and a UNC path on the remote machine in the SCOPE clause, as shown in the following example:</span></span>

```sql
SELECT System.ItemName FROM MachineName.SystemIndex WHERE SCOPE='file://MachineName/<path>'
```

## <a name="aqs-based-queries"></a><span data-ttu-id="12e96-164">Auf AQS basierende Abfragen</span><span class="sxs-lookup"><span data-stu-id="12e96-164">AQS Based Queries</span></span>

<span data-ttu-id="12e96-165">AQS ist die Standard Abfrage Syntax, die von Windows Search verwendet wird, um den Index abzufragen und Suchparameter zu verfeinern und einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="12e96-165">AQS is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="12e96-166">Obwohl AQS hauptsächlich für Benutzer steht, kann es von Entwicklern verwendet werden, um Abfragen Programm gesteuert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="12e96-166">While AQS is primarily user facing, it can be used by developers to build queries programmatically.</span></span> <span data-ttu-id="12e96-167">In Windows 7 wurde die kanonische AQS eingeführt und muss in Windows 7 und höher verwendet werden, um AQS-Abfragen Programm gesteuert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="12e96-167">In Windows 7 canonical AQS was introduced, and must be used in Windows 7 and later, to programmatically generate AQS queries.</span></span> <span data-ttu-id="12e96-168">Ausführliche Informationen zu AQS finden Sie unter [Programm gesteuertes verwenden der erweiterten Abfrage Syntax](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="12e96-168">For detailed information on AQS, see [Using Advanced Query Syntax Programmatically](-search-3x-advancedquerysyntax.md).</span></span>

<span data-ttu-id="12e96-169">Die folgenden Ansätze zum Abfragen des Indexes sind AQS-basiert.</span><span class="sxs-lookup"><span data-stu-id="12e96-169">The following approaches for querying the index are AQS based.</span></span>

### <a name="using-isearchqueryhelper"></a><span data-ttu-id="12e96-170">Verwenden von isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="12e96-170">Using ISearchQueryHelper</span></span>

<span data-ttu-id="12e96-171">Sie können eine Komponente oder Hilfsklasse entwickeln, um den Index mithilfe der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle abzufragen. Dadurch können Sie einige Features des Systems nutzen und die Verwendung von Windows Search vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="12e96-171">You can develop a component or helper class to query the index by using the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, which enables you to take advantage of some features of the system and simplify your use of Windows Search.</span></span> <span data-ttu-id="12e96-172">Diese Schnittstelle unterstützt Sie dabei:</span><span class="sxs-lookup"><span data-stu-id="12e96-172">This interface helps you:</span></span>

- <span data-ttu-id="12e96-173">Rufen Sie eine OLE DB Verbindungs Zeichenfolge für die Verbindung mit der Windows Search-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="12e96-173">Obtain an OLE DB connection string to connect to the Windows Search database.</span></span>
- <span data-ttu-id="12e96-174">Konvertieren von Benutzer Abfragen von AQS in Windows Search SQL.</span><span class="sxs-lookup"><span data-stu-id="12e96-174">Convert user queries from AQS to Windows Search SQL.</span></span>

<span data-ttu-id="12e96-175">Diese Schnittstelle ist als Hilfsklasse für [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) implementiert und wird durch Aufrufen von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)abgerufen, wie im folgenden C++-Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="12e96-175">This interface is implemented as a helper class to [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) and is obtained by calling [**ISearchCatalogManager::GetQueryHelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper), as shown in the following C++ example.</span></span>

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

<span data-ttu-id="12e96-176">Informationen zum Implementieren der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle finden [Sie unter Verwenden der isearchqueryhelper-Schnittstelle](-search-3x-wds-qryidx-searchqueryhelper.md) und des [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Referenz Themas.</span><span class="sxs-lookup"><span data-stu-id="12e96-176">To implement the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) interface, see [Using the ISearchQueryHelper Interface](-search-3x-wds-qryidx-searchqueryhelper.md) and the [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) reference topic.</span></span>

> [!Note]  
> <span data-ttu-id="12e96-177">Ältere Microsoft Windows-Desktop Suche (WDS) 2 x Kompatibilität: auf Computern, auf denen Windows XP und Windows Server 2003 und höher ausgeführt wird, ist [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) veraltet.</span><span class="sxs-lookup"><span data-stu-id="12e96-177">Legacy Microsoft Windows Desktop Search (WDS) 2x compatibility: On computers running Windows XP and Windows Server 2003 and later, [**ISearchDesktop**](/previous-versions//aa965729(v=vs.85)) is deprecated.</span></span> <span data-ttu-id="12e96-178">Stattdessen sollten Entwickler [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) verwenden, um eine Verbindungs Zeichenfolge zu erhalten, die Abfrage des Benutzers in SQL zu analysieren und dann OLE DB abzufragen.</span><span class="sxs-lookup"><span data-stu-id="12e96-178">Instead, developers should use [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) to get a connection string, parse the user's query into SQL, and then query through OLE DB.</span></span>

### <a name="using-the-search-ms-protocol"></a><span data-ttu-id="12e96-179">Verwenden des Search-MS-Protokolls</span><span class="sxs-lookup"><span data-stu-id="12e96-179">Using the search-ms Protocol</span></span>

<span data-ttu-id="12e96-180">Das **Search-MS-** [Anwendungsprotokoll](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) ist eine Konvention zum Starten einer Anwendung wie Windows-Explorer, um den Windows-Suchindex abzufragen.</span><span class="sxs-lookup"><span data-stu-id="12e96-180">The **search-ms** [application protocol](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85)) is a convention for starting an application, like Windows Explorer, to query the Windows Search index.</span></span> <span data-ttu-id="12e96-181">Sie ermöglicht das Erstellen von Abfragen mit Parameter-Wert-Argumenten, einschließlich Eigenschafts Argumenten, zuvor gespeicherter Suchvorgänge, erweiterter Abfrage Syntax (AQS), natürlicher Abfrage Syntax (NQS) und Sprachcode Bezeichner (LCIDs) für den Indexer und die Abfrage selbst.</span><span class="sxs-lookup"><span data-stu-id="12e96-181">It enables queries to be built with parameter-value arguments, including property arguments, previously saved searches, Advanced Query Syntax (AQS), Natural Query Syntax (NQS), and language code identifiers (LCIDs) for both the indexer and the query itself.</span></span>

<span data-ttu-id="12e96-182">Ausführliche Informationen zur Search-MS-Protokoll Syntax finden Sie unter [Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md).</span><span class="sxs-lookup"><span data-stu-id="12e96-182">For detailed information on the search-ms protocol syntax, see [Querying the Index with the search-ms Protocol](-search-3x-wds-qryidx-searchms.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="12e96-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12e96-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12e96-184">Programm gesteuertes Abfragen des Indexes</span><span class="sxs-lookup"><span data-stu-id="12e96-184">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="12e96-185">Abfragen des Indexes mit isearchqueryhelper</span><span class="sxs-lookup"><span data-stu-id="12e96-185">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="12e96-186">Abfragen des Indexes mit dem Search-MS-Protokoll</span><span class="sxs-lookup"><span data-stu-id="12e96-186">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="12e96-187">Abfragen des Indexes mit der SQL-Syntax von Windows Search</span><span class="sxs-lookup"><span data-stu-id="12e96-187">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> <dt>

[<span data-ttu-id="12e96-188">Programm gesteuertes verwenden der erweiterten Abfrage Syntax</span><span class="sxs-lookup"><span data-stu-id="12e96-188">Using Advanced Query Syntax Programmatically</span></span>](-search-3x-advancedquerysyntax.md)
</dt> </dl>
