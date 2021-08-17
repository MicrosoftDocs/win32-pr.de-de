---
title: SQL Dialekt
description: Der SQL, abgeleitet vom strukturierte Abfragesprache, verwendet lesbare Ausdrücke, um Abfrageausdrücke zu definieren.
ms.assetid: c1032268-e0f5-4d74-ab72-864cdd36851d
ms.tgt_platform: multiple
keywords:
- SQL Dialekt ADSI
- Dialekt ADSI , SQL Dialekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7483a5e3785f410e6c2fd875122ba24618a82b70d1ed6dc9a85105ae4e8dcfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262050"
---
# <a name="sql-dialect"></a>SQL Dialekt

Der SQL, abgeleitet vom strukturierte Abfragesprache, verwendet lesbare Ausdrücke, um Abfrageausdrücke zu definieren. Verwenden Sie SQL Abfrageauszug mit den folgenden ADSI-Suchschnittstellen:

-   Die [ActiveX ADO-Schnittstellen (Data Object),](searching-with-activex-data-objects-ado.md) bei denen es sich um Automatisierungsschnittstellen handelt, die OLE DB.
-   [OLE DB](searching-with-ole-db.md), einem Satz von C/C++-Schnittstellen zum Abfragen von Datenbanken.

SQL-Anweisungen erfordern die folgende Syntax.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



In der folgenden Tabelle werden SQL Abfrageauszugsschlüsselwörter aufgeführt.



| Stichwort  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Gibt eine durch Komma getrennte Liste von Attributen an, die für jedes Objekt abgerufen werden. Wenn Sie \* angeben, ruft die Abfrage nur den ADsPath jedes Objekts ab.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Gibt den ADsPath der Basis der Suche an. Beispielsweise kann der ADsPath des Containers Users in einer Active Directory-Domäne "LDAP://CN=Users,DC=Fabrikam,DC=COM" sein. Beachten Sie, dass der Pfad in ein Paar aus einfachen Anführungszeichen (') eingeschlossen ist.                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Ein optionales Schlüsselwort, das den Abfragefilter angibt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Ein optionales Schlüsselwort, das eine serverseitige Sortierung generiert, wenn der Server das LDAP-Sortiersteuerwort unterstützt. Active Directory unterstützt das Sortiersteuersystem, kann sich jedoch auf die Serverleistung auswirken, insbesondere wenn das Resultseset groß ist. Die Sortierliste ist eine durch Komma getrennte Liste von Attributen, nach denen sortiert werden soll. Beachten Sie, dass Active Directory nur einen einzelnen Sortierschlüssel unterstützt. Sie können die optionalen ASC- und DESC-Schlüsselwörter verwenden, um eine aufsteigende oder absteigende Sortierreihenfolge anzugeben. Der Standardwert ist aufsteigend. Das ORDER BY-Schlüsselwort überschreibt alle Sortierschlüssel, die mit der Eigenschaft "Sort on" des ADO-Befehlsobjekts angegeben sind. |



 

> [!Note]  
> In Fällen, in denen ein MultiByte-Zeichensatz verwendet wird und die Suche von ADO mit dem SQL-Dialekt ausgeführt wird, kann kein schräger Schrägstrich als Escapezeichen verwendet werden. Stattdessen müssen die in Sonderzeichen aufgeführten [Escapesequenzen](search-filter-syntax.md) verwendet werden. Beispiel: Für eine -Anweisung, die die Syntax "samAccountName= Test" verwendet, die den zurücken Schrägstrich " " verwendet, um die geöffnete Klammer "("" zu escapen, ersetzen Sie stattdessen den zurücken Schrägstrich durch das Sonderzeichen \( \\ " \\ 28", wie folgt: "samAccountName= \\ 28Test".

 

Die folgenden Abfrage-Anweisungen sind Beispiele für SQL Dialekt in ADSI.

So suchen Sie nach allen Gruppenobjekten.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



So suchen Sie nach allen Benutzern, deren Nachname mit dem Buchstaben H beginnt.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



Die formale Grammatik SQL Abfragen wird im folgenden Codebeispiel definiert. Bei allen Schlüsselwörtern wird die Groß-/Kleinschreibung nicht beachtet.


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



SQL inneren Joins werden vom Active Directory OLE DB-Anbieter nicht unterstützt, aber Sie können SQL verwenden, um daten- SQL Active Directory-Daten zu verbinden. Weitere Informationen finden Sie unter [Creating a Heterogeneous Join between SQL Server and Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchfiltersyntax](search-filter-syntax.md)
</dt> <dt>

[LDAP-Dialekt](ldap-dialect.md)
</dt> <dt>

[Suchen mit der IDirectorySearch-Schnittstelle](searching-with-idirectorysearch.md)
</dt> <dt>

[Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Suchen mit OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




