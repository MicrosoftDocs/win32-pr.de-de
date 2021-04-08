---
title: LDAP-Dialekt
description: Der LDAP-Dialekt ist ein Format für Abfrage Anweisungen, die die LDAP-Suchfilter Syntax verwenden.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- LDAP-Dialekt-ADSI
- Dialekte ADSI, LDAP-Dialekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f7d1f65a41655596d0a14cf6e2a3595916c2cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855288"
---
# <a name="ldap-dialect"></a><span data-ttu-id="cd0ef-105">LDAP-Dialekt</span><span class="sxs-lookup"><span data-stu-id="cd0ef-105">LDAP Dialect</span></span>

<span data-ttu-id="cd0ef-106">Der LDAP-Dialekt ist ein Format für Abfrage Anweisungen, die die [LDAP-Suchfilter Syntax](search-filter-syntax.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-106">The LDAP dialect is a format for query statements that use the [LDAP search filter syntax](search-filter-syntax.md).</span></span> <span data-ttu-id="cd0ef-107">Verwenden Sie eine LDAP-Abfrage Anweisung mit den folgenden ADSI-Such Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="cd0ef-107">Use an LDAP query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="cd0ef-108">Die ADO-Schnittstellen [(ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , bei denen es sich um Automatisierungs Schnittstellen handelt, die OLE DB verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="cd0ef-109">[OLE DB](searching-with-ole-db.md), bei dem es sich um einen Satz von C/C++-Schnittstellen zum Abfragen von Datenbanken handelt.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>
-   <span data-ttu-id="cd0ef-110">[**Idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), bei der es sich um die C/C++-Schnittstelle für Active Directory handelt.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-110">[**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), which is the C/C++ interface for Active Directory.</span></span>

<span data-ttu-id="cd0ef-111">Eine LDAP-Dialekt Zeichenfolge besteht aus vier Teilen, die durch Semikolons (;) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-111">An LDAP dialect string consists of four parts separated by semicolons (;).</span></span>

-   <span data-ttu-id="cd0ef-112">Basis definierter Name.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-112">Base distinguished name.</span></span> <span data-ttu-id="cd0ef-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cd0ef-113">For example:</span></span>

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   <span data-ttu-id="cd0ef-114">LDAP-Suchfilter.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-114">LDAP search filters.</span></span> <span data-ttu-id="cd0ef-115">Weitere Informationen zu Suchfiltern finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cd0ef-115">For more information about search filters, see [Search Filter Syntax](search-filter-syntax.md).</span></span>
-   <span data-ttu-id="cd0ef-116">Der LDAP-Anzeige Name der abzurufenden Attribute.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-116">The LDAP display name of the attributes to retrieve.</span></span> <span data-ttu-id="cd0ef-117">Mehrere Attribute werden durch ein Komma getrennt.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-117">Multiple attributes are separated by a comma.</span></span>
-   <span data-ttu-id="cd0ef-118">Gibt den Suchbereich an.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-118">Specifies the scope of the search.</span></span> <span data-ttu-id="cd0ef-119">Gültige Werte sind "Base", "onelevel" und "subtree".</span><span class="sxs-lookup"><span data-stu-id="cd0ef-119">Valid values are "base", "onelevel", and "subtree".</span></span> <span data-ttu-id="cd0ef-120">Der in einer LDAP-Abfrage Zeichenfolge angegebene Bereich überschreibt jeden Suchbereich, der mit der Eigenschaft "SearchScope" des ADO-Befehls Objekts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-120">The scope specified in an LDAP query string overrides any search scope specified with the "SearchScope" property of the ADO Command object.</span></span>

<span data-ttu-id="cd0ef-121">Im folgenden finden Sie ein Codebeispiel für den LDAP-Dialekt in ADSI, der alle Objekte in der Teilstruktur durchsucht.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-121">The following is a code example of the LDAP dialect in ADSI that searches all the objects in the subtree.</span></span>


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



<span data-ttu-id="cd0ef-122">Nicht alle Suchoptionen (z. b. Suchseiten Größe) können im LDAP-Dialekt ausgedrückt werden. Daher müssen Sie die Optionen festlegen, bevor die tatsächliche Ausführung der Abfrage gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-122">Not all search options (search page size, for example) can be expressed in the LDAP dialect, so you must set the options before the actual query execution starts.</span></span>

## <a name="example-code-for-performing-an-ldap-query"></a><span data-ttu-id="cd0ef-123">Beispiel Code für das Ausführen einer LDAP-Abfrage</span><span class="sxs-lookup"><span data-stu-id="cd0ef-123">Example Code for Performing an LDAP Query</span></span>

<span data-ttu-id="cd0ef-124">Im folgenden Codebeispiel wird gezeigt, wie eine LDAP-Abfrage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd0ef-124">The following code example shows how to use an LDAP query</span></span>


```VB
Dim con As New Connection, rs As New Recordset
Dim adVariant
Dim i 'Used for counter
Dim j 'Used for counter
Dim Com As New Command
Dim strDomain As String
Dim strPassword As String
 
' Open a Connection object.
con.Provider = "ADsDSOObject"
con.Properties("ADSI Flag") = 1
con.Properties("User ID") = strDomain + "\" + strUserID
con.Properties("Password") = strPassword

con.Open "Active Directory Provider"
 
' Create a command object on this connection.
Set Com.ActiveConnection = con
 
' Set the query string.
Com.CommandText = "<LDAP://MyServer/DC=MyDomain,DC=Fabrikam,DC=com>;
     (objectClass=*);ADsPath, objectclass;base"
 
' Set search preferences.
Com.Properties("Page Size") = 1000
Com.Properties("Timeout") = 30 'seconds
 
' Execute the query.
Set rs = Com.Execute
 
' Navigate the record set.
rs.MoveFirst
While Not rs.EOF
    For i = 0 To rs.Fields.Count - 1
        If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
            Debug.Print rs.Fields(i).Name, " = "
            For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
                Debug.Print rs.Fields(i).Value(j), " # "
            Next j
        Else
            Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
        End If
    Next i
    rs.MoveNext
Wend
 
rs.MoveLast
Debug.Print "No. of rows = ", rs.RecordCount
```



<span data-ttu-id="cd0ef-125">Ausführliche Informationen zur Abfrage Syntax finden Sie unter [Syntax für Such Filter](search-filter-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="cd0ef-125">For details about the query syntax, see [Search Filter Syntax](search-filter-syntax.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd0ef-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd0ef-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd0ef-127">Such Filter Syntax</span><span class="sxs-lookup"><span data-stu-id="cd0ef-127">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="cd0ef-128">SQL-Dialekt</span><span class="sxs-lookup"><span data-stu-id="cd0ef-128">SQL dialect</span></span>](sql-dialect.md)
</dt> <dt>

[<span data-ttu-id="cd0ef-129">Suchen mit der idirector ysearch-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cd0ef-129">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="cd0ef-130">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="cd0ef-130">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="cd0ef-131">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="cd0ef-131">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




