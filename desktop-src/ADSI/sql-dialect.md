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
# <a name="sql-dialect"></a>SQL-Dialekt

Der SQL-Dialekt, der aus der Structured Query Language abgeleitet ist, verwendet lesbare Ausdrücke zum Definieren von Abfrage Anweisungen. Verwenden Sie eine SQL-Abfrage Anweisung mit den folgenden ADSI-Such Schnittstellen:

-   Die ADO-Schnittstellen [(ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , bei denen es sich um Automatisierungs Schnittstellen handelt, die OLE DB verwenden.
-   [OLE DB](searching-with-ole-db.md), bei dem es sich um einen Satz von C/C++-Schnittstellen zum Abfragen von Datenbanken handelt.

SQL-Anweisungen erfordern folgende Syntax.


```sql
SELECT [ALL] * | select-list FROM 'ADsPath' [WHERE search-condition] [ORDER BY sort-list]
```



In der folgenden Tabelle sind die Schlüsselwörter der SQL-Abfrage Anweisung aufgeführt



| Schlüsselwort  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SELECT   | Gibt eine durch Trennzeichen getrennte Liste von Attributen an, die für jedes Objekt abgerufen werden sollen. Wenn Sie angeben \* , ruft die Abfrage nur den ADsPath der einzelnen Objekte ab.                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| FROM     | Gibt den ADsPath der Basis für die Suche an. Der ADsPath des Containers "Users" in einer Active Directory Domäne kann z. b. "LDAP://CN = Users, DC = fabrikam, DC = com" lauten. Beachten Sie, dass der Pfad in einfache Anführungszeichen (') eingeschlossen ist.                                                                                                                                                                                                                                                                                                                                                    |
| WHERE    | Ein optionales Schlüsselwort, das den Abfrage Filter angibt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ORDER BY | Ein optionales Schlüsselwort, das eine serverseitige Sortierung generiert, wenn der Server das LDAP-Sortier Steuerelement unterstützt. Active Directory unterstützt das Sortier Steuerelement, kann sich jedoch auf die Serverleistung auswirken, insbesondere dann, wenn das Resultset groß ist. Sort-List ist eine durch Trennzeichen getrennte Liste von Attributen, nach denen sortiert werden soll. Beachten Sie, dass Active Directory nur einen einzelnen Sortierschlüssel unterstützt. Mit den optionalen Schlüsselwörtern ASC und Debug können Sie eine aufsteigende oder absteigende Sortierreihenfolge angeben. der Standardwert ist aufsteigend. Das Order by-Schlüsselwort überschreibt jeden Sortierschlüssel, der mit der Eigenschaft "Sortieren nach" des ADO-Befehls Objekts angegeben wird. |



 

> [!Note]  
> In Fällen, in denen ein Multibyte-Zeichensatz verwendet wird, kann ein umgekehrter Schrägstrich nicht zum Escapezeichen verwendet werden, wenn die Suche von ADO mit dem SQL-Dialekt ausgeführt wird. Stattdessen müssen die in [Sonderzeichen](search-filter-syntax.md) aufgeführten Escapesequenzen verwendet werden. Beispielsweise können Sie für eine Anweisung, die die Syntax "SamAccountName = Test" verwendet, die den umgekehrten \( Schrägstrich "" verwendet, \\ um die öffnende Klammer mit Escapezeichen zu versehen ("("), stattdessen den umgekehrten Schrägstrich durch das Sonderzeichen " \\ 28" ersetzen: "SamAccountName = \\ 28test".

 

Die folgenden Abfrage Anweisungen sind Beispiele für den SQL-Dialekt in ADSI.

, Um nach allen Gruppen Objekten zu suchen.


```sql
SELECT ADsPath, cn FROM 'LDAP://DC=Fabrikam,DC=COM' WHERE objectCategory='group'
```



Um nach allen Benutzern zu suchen, deren Nachname mit dem Buchstaben H beginnt.


```sql
SELECT ADsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=COM' WHERE objectCategory='person' AND objectClass='user' AND sn = 'H*' ORDER BY sn
```



Die formale Grammatik für SQL-Abfragen wird im folgenden Codebeispiel definiert. Bei allen Schlüsselwörtern wird Groß-/Kleinschreibung nicht beachtet


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



Innere SQL-Joins werden vom Active Directory OLE DB-Anbieter nicht unterstützt. Sie können jedoch SQL verwenden, um SQL-und Active Directory-Daten zu verknüpfen. Weitere Informationen finden Sie unter [Erstellen eines heterogenen Joins zwischen SQL Server und Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Such Filter Syntax](search-filter-syntax.md)
</dt> <dt>

[LDAP-Dialekt](ldap-dialect.md)
</dt> <dt>

[Suchen mit der idirector ysearch-Schnittstelle](searching-with-idirectorysearch.md)
</dt> <dt>

[Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Suchen mit OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




