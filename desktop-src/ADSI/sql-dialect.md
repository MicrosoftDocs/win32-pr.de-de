---
title: SQL-Dialekt
description: Der SQL-Dialekt, der aus der Structured Query Language abgeleitet ist, verwendet lesbare Ausdrücke zum Definieren von Abfrage Anweisungen.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL-Dialekt-ADSI
- Dialekt ADSI, SQL-Dialekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0936a54bc7bd0028717967ce779fe2f2048a33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338561"
---
# <a name="sql-dialect"></a><span data-ttu-id="87bff-105">SQL-Dialekt</span><span class="sxs-lookup"><span data-stu-id="87bff-105">SQL Dialect</span></span>

<span data-ttu-id="87bff-106">Der SQL-Dialekt, der aus der Structured Query Language abgeleitet ist, verwendet lesbare Ausdrücke zum Definieren von Abfrage Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="87bff-106">The SQL dialect, derived from the Structured Query Language, uses human-readable expressions to define query statements.</span></span> <span data-ttu-id="87bff-107">Verwenden Sie eine SQL-Abfrage Anweisung mit den folgenden ADSI-Such Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="87bff-107">Use a SQL query statement with the following ADSI search interfaces:</span></span>

-   <span data-ttu-id="87bff-108">Die ADO-Schnittstellen [(ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , bei denen es sich um Automatisierungs Schnittstellen handelt, die OLE DB verwenden.</span><span class="sxs-lookup"><span data-stu-id="87bff-108">The [ActiveX Data Object (ADO)](searching-with-activex-data-objects-ado.md) interfaces, which are Automation interfaces that use OLE DB.</span></span>
-   <span data-ttu-id="87bff-109">[OLE DB](searching-with-ole-db.md), bei dem es sich um einen Satz von C/C++-Schnittstellen zum Abfragen von Datenbanken handelt.</span><span class="sxs-lookup"><span data-stu-id="87bff-109">[OLE DB](searching-with-ole-db.md), which is a set of C/C++ interfaces for querying databases.</span></span>

<span data-ttu-id="87bff-110">SQL-Anweisungen erfordern folgende Syntax.</span><span class="sxs-lookup"><span data-stu-id="87bff-110">SQL statements require the following syntax.</span></span>


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



<span data-ttu-id="87bff-111">In der folgenden Tabelle sind die Schlüsselwörter der SQL-Abfrage Anweisung aufgeführt</span><span class="sxs-lookup"><span data-stu-id="87bff-111">The following table lists SQL query statement keywords.</span></span>



| <span data-ttu-id="87bff-112">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="87bff-112">Keyword</span></span>  | <span data-ttu-id="87bff-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87bff-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87bff-114">SELECT</span><span class="sxs-lookup"><span data-stu-id="87bff-114">SELECT</span></span>   | <span data-ttu-id="87bff-115">Gibt eine durch Trennzeichen getrennte Liste von Attributen an, die für jedes Objekt abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="87bff-115">Specifies a comma-separated list of attributes to retrieve for each object.</span></span> <span data-ttu-id="87bff-116">Wenn Sie angeben \* , ruft die Abfrage nur den ADsPath der einzelnen Objekte ab.</span><span class="sxs-lookup"><span data-stu-id="87bff-116">If you specify \*, the query retrieves only the ADsPath of each object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="87bff-117">FROM</span><span class="sxs-lookup"><span data-stu-id="87bff-117">FROM</span></span>     | <span data-ttu-id="87bff-118">Gibt den ADsPath der Basis für die Suche an.</span><span class="sxs-lookup"><span data-stu-id="87bff-118">Specifies the ADsPath of the base of the search.</span></span> <span data-ttu-id="87bff-119">Der ADsPath des Containers "Users" in einer Active Directory Domäne kann z. b. "LDAP://CN = Users, DC = fabrikam, DC = com" lauten.</span><span class="sxs-lookup"><span data-stu-id="87bff-119">For example, the ADsPath of the Users container in an Active Directory domain might be 'LDAP://CN=Users,DC=Fabrikam,DC=COM'.</span></span> <span data-ttu-id="87bff-120">Beachten Sie, dass der Pfad in einfache Anführungszeichen (') eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="87bff-120">Be aware that the path is enclosed in a pair of single quotation marks (').</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="87bff-121">WHERE</span><span class="sxs-lookup"><span data-stu-id="87bff-121">WHERE</span></span>    | <span data-ttu-id="87bff-122">Ein optionales Schlüsselwort, das den Abfrage Filter angibt.</span><span class="sxs-lookup"><span data-stu-id="87bff-122">An optional keyword that specifies the query filter.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="87bff-123">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="87bff-123">ORDER BY</span></span> | <span data-ttu-id="87bff-124">Ein optionales Schlüsselwort, das eine serverseitige Sortierung generiert, wenn der Server das LDAP-Sortier Steuerelement unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87bff-124">An optional keyword that generates a server-side sort if the server supports the LDAP sort control.</span></span> <span data-ttu-id="87bff-125">Active Directory unterstützt das Sortier Steuerelement, kann sich jedoch auf die Serverleistung auswirken, insbesondere dann, wenn das Resultset groß ist.</span><span class="sxs-lookup"><span data-stu-id="87bff-125">Active Directory supports the sort control, but it can impact server performance, particularly if the results set is large.</span></span> <span data-ttu-id="87bff-126">Sort-List ist eine durch Trennzeichen getrennte Liste von Attributen, nach denen sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="87bff-126">The sort-list is a comma-separated list of attributes on which to sort.</span></span> <span data-ttu-id="87bff-127">Beachten Sie, dass Active Directory nur einen einzelnen Sortierschlüssel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87bff-127">Be aware that Active Directory supports only a single sort key.</span></span> <span data-ttu-id="87bff-128">Mit den optionalen Schlüsselwörtern ASC und Debug können Sie eine aufsteigende oder absteigende Sortierreihenfolge angeben. der Standardwert ist aufsteigend.</span><span class="sxs-lookup"><span data-stu-id="87bff-128">You can use the optional ASC and DESC keywords to specify ascending or descending sort order; the default is ascending.</span></span> <span data-ttu-id="87bff-129">Das Order by-Schlüsselwort überschreibt jeden Sortierschlüssel, der mit der Eigenschaft "Sortieren nach" des ADO-Befehls Objekts angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="87bff-129">The ORDER BY keyword overrides any sort key specified with the "Sort on" property of the ADO Command object.</span></span> |



 

> [!Note]  
> <span data-ttu-id="87bff-130">In Fällen, in denen ein Multibyte-Zeichensatz verwendet wird, kann ein umgekehrter Schrägstrich nicht zum Escapezeichen verwendet werden, wenn die Suche von ADO mit dem SQL-Dialekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87bff-130">In cases where a MultiByte Character Set is being used, if the search is performed by ADO with the SQL dialect, then a backslash cannot be used to escape characters.</span></span> <span data-ttu-id="87bff-131">Stattdessen müssen die in [Sonderzeichen](search-filter-syntax.md) aufgeführten Escapesequenzen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87bff-131">Instead, the escape sequences listed in [Special Characters](search-filter-syntax.md) must be used.</span></span> <span data-ttu-id="87bff-132">Beispielsweise können Sie für eine Anweisung, die die Syntax "SamAccountName = Test" verwendet, die den umgekehrten \( Schrägstrich "" verwendet, \\ um die öffnende Klammer mit Escapezeichen zu versehen ("("), stattdessen den umgekehrten Schrägstrich durch das Sonderzeichen " \\ 28" ersetzen: "SamAccountName = \\ 28test".</span><span class="sxs-lookup"><span data-stu-id="87bff-132">For example, for a statement that used the syntax "samAccountName=\(Test", which uses the backslash, "\\", to escape the open parenthesis, "(", instead, you would replace the backslash with the special character "\\28", as follows: "samAccountName=\\28Test".</span></span>

 

<span data-ttu-id="87bff-133">Die folgenden Abfrage Anweisungen sind Beispiele für den SQL-Dialekt in ADSI.</span><span class="sxs-lookup"><span data-stu-id="87bff-133">The following query statements are examples of SQL dialect in ADSI.</span></span>

<span data-ttu-id="87bff-134">, Um nach allen Gruppen Objekten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="87bff-134">To search for all the group objects.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



<span data-ttu-id="87bff-135">Um nach allen Benutzern zu suchen, deren Nachname mit dem Buchstaben H beginnt.</span><span class="sxs-lookup"><span data-stu-id="87bff-135">To search for all the users whose Last Name starts with letter H.</span></span>


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



<span data-ttu-id="87bff-136">Die formale Grammatik für SQL-Abfragen wird im folgenden Codebeispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="87bff-136">The formal grammar for SQL queries is defined in the following code example.</span></span> <span data-ttu-id="87bff-137">Bei allen Schlüsselwörtern wird Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="87bff-137">All keywords are case-insensitive.</span></span>


```sql
statement ::= select-statement
select-statement ::= SELECT [ALL] select-list FROM table-identifier [WHERE search-condition] [ORDER BY sort-list]
select-list ::= * | select-sublist [, select-sublist]... 
select-sublist ::= column-identifier
column-identifier ::= user-defined-name 
table-identifier ::= string-literal
search-condition ::= boolean-term [OR search-condition]
sort-list ::= column-identifier [ASC | DESC] [,column-identifier [ASC | DESC]]... 
boolean-term ::= boolean-factor [AND boolean-term]
boolean-factor ::= [NOT] boolean-primary
boolean-primary ::= comparison-predicate | (search-condition)
comparison-predicate ::= column-identifier comparison-operator literal
comparison-operator ::= < | > | <= | >= | = | <>
user-defined-name ::= letter [letter | digit]...
literal ::= string-literal | numeric-literal | boolean-literal 
string-literal ::= '{character}...' (Any sequence of characters delimited by quotes)
numeric-literal ::= digits [fraction] [exponent]
digits ::= digit [digit]...
fraction ::= . digits 
exponent ::= E digits
boolean-literal ::= TRUE | FALSE | YES | NO | ON | OFF
```



<span data-ttu-id="87bff-138">Innere SQL-Joins werden vom Active Directory OLE DB-Anbieter nicht unterstützt. Sie können jedoch SQL verwenden, um SQL-und Active Directory-Daten zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="87bff-138">SQL inner joins are not supported by the Active Directory OLE DB provider, but you can use SQL to join SQL and Active Directory data.</span></span> <span data-ttu-id="87bff-139">Weitere Informationen finden Sie unter [Erstellen eines heterogenen Joins zwischen SQL Server und Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="87bff-139">For more information, see [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="87bff-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="87bff-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87bff-141">Such Filter Syntax</span><span class="sxs-lookup"><span data-stu-id="87bff-141">Search Filter Syntax</span></span>](search-filter-syntax.md)
</dt> <dt>

[<span data-ttu-id="87bff-142">LDAP-Dialekt</span><span class="sxs-lookup"><span data-stu-id="87bff-142">LDAP dialect</span></span>](ldap-dialect.md)
</dt> <dt>

[<span data-ttu-id="87bff-143">Suchen mit der idirector ysearch-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="87bff-143">Searching with the IDirectorySearch Interface</span></span>](searching-with-idirectorysearch.md)
</dt> <dt>

[<span data-ttu-id="87bff-144">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="87bff-144">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[<span data-ttu-id="87bff-145">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="87bff-145">Searching with OLE DB</span></span>](searching-with-ole-db.md)
</dt> </dl>

 

 




