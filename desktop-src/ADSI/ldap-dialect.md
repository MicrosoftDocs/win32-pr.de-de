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
# <a name="ldap-dialect"></a>LDAP-Dialekt

Der LDAP-Dialekt ist ein Format für Abfrage Anweisungen, die die [LDAP-Suchfilter Syntax](search-filter-syntax.md)verwenden. Verwenden Sie eine LDAP-Abfrage Anweisung mit den folgenden ADSI-Such Schnittstellen:

-   Die ADO-Schnittstellen [(ActiveX Data Object)](searching-with-activex-data-objects-ado.md) , bei denen es sich um Automatisierungs Schnittstellen handelt, die OLE DB verwenden.
-   [OLE DB](searching-with-ole-db.md), bei dem es sich um einen Satz von C/C++-Schnittstellen zum Abfragen von Datenbanken handelt.
-   [**Idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), bei der es sich um die C/C++-Schnittstelle für Active Directory handelt.

Eine LDAP-Dialekt Zeichenfolge besteht aus vier Teilen, die durch Semikolons (;) getrennt sind.

-   Basis definierter Name. Beispiel:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   LDAP-Suchfilter. Weitere Informationen zu Suchfiltern finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).
-   Der LDAP-Anzeige Name der abzurufenden Attribute. Mehrere Attribute werden durch ein Komma getrennt.
-   Gibt den Suchbereich an. Gültige Werte sind "Base", "onelevel" und "subtree". Der in einer LDAP-Abfrage Zeichenfolge angegebene Bereich überschreibt jeden Suchbereich, der mit der Eigenschaft "SearchScope" des ADO-Befehls Objekts angegeben wird.

Im folgenden finden Sie ein Codebeispiel für den LDAP-Dialekt in ADSI, der alle Objekte in der Teilstruktur durchsucht.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Nicht alle Suchoptionen (z. b. Suchseiten Größe) können im LDAP-Dialekt ausgedrückt werden. Daher müssen Sie die Optionen festlegen, bevor die tatsächliche Ausführung der Abfrage gestartet wird.

## <a name="example-code-for-performing-an-ldap-query"></a>Beispiel Code für das Ausführen einer LDAP-Abfrage

Im folgenden Codebeispiel wird gezeigt, wie eine LDAP-Abfrage verwendet wird.


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



Ausführliche Informationen zur Abfrage Syntax finden Sie unter [Syntax für Such Filter](search-filter-syntax.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Such Filter Syntax](search-filter-syntax.md)
</dt> <dt>

[SQL-Dialekt](sql-dialect.md)
</dt> <dt>

[Suchen mit der idirector ysearch-Schnittstelle](searching-with-idirectorysearch.md)
</dt> <dt>

[Suchen mit ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Suchen mit OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




