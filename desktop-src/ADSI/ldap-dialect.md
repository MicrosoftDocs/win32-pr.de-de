---
title: LDAP-Dialekt
description: Der LDAP-Dialekt ist ein Format für Abfrageanweisungen, die die LDAP-Suchfiltersyntax verwenden.
ms.assetid: 29aca7e6-3ed5-4efd-8b03-6a2ee0571f1f
ms.tgt_platform: multiple
keywords:
- LDAP-Dialekt ADSI
- Dialekte ADSI , LDAP-Dialekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c231d3c4d619775cca2ed9542733bff51219d92ff31d922f6d38ea7b1bcd2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509980"
---
# <a name="ldap-dialect"></a>LDAP-Dialekt

Der LDAP-Dialekt ist ein Format für Abfrageanweisungen, die die [LDAP-Suchfiltersyntax](search-filter-syntax.md)verwenden. Verwenden Sie eine LDAP-Abfrage-Anweisung mit den folgenden ADSI-Suchschnittstellen:

-   Die [ADO-Schnittstellen (ActiveX Data Object),](searching-with-activex-data-objects-ado.md) bei denen es sich um Automation-Schnittstellen handelt, die OLE DB verwenden.
-   [OLE DB](searching-with-ole-db.md), bei dem es sich um eine Reihe von C/C++-Schnittstellen zum Abfragen von Datenbanken handelt.
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)ist die C/C++-Schnittstelle für Active Directory.

Eine LDAP-Dialektzeichenfolge besteht aus vier Teilen, die durch Semikolons (;).

-   Basisunterscheidungsname. Beispiel:

    ```VB
    <LDAP://DC=Fabrikam,DC=COM>
    ```

    

-   LDAP-Suchfilter. Weitere Informationen zu Suchfiltern finden Sie unter [Suchfiltersyntax.](search-filter-syntax.md)
-   Der LDAP-Anzeigename der abzurufende Attribute. Mehrere Attribute werden durch ein Komma getrennt.
-   Gibt den Bereich der Suche an. Gültige Werte sind "base", "onelevel" und "subtree". Der in einer LDAP-Abfragezeichenfolge angegebene Bereich überschreibt jeden Suchbereich, der mit der SearchScope-Eigenschaft des ADO Command-Objekts angegeben wird.

Im Folgenden ist ein Codebeispiel für den LDAP-Dialekt in ADSI aufgeführt, der alle Objekte in der Unterstruktur durchsucht.


```VB
"<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn;subTree"
```



Nicht alle Suchoptionen (z. B. die Größe der Suchseite) können im LDAP-Dialekt ausgedrückt werden. Daher müssen Sie die Optionen festlegen, bevor die eigentliche Abfrageausführung beginnt.

## <a name="example-code-for-performing-an-ldap-query"></a>Beispielcode zum Ausführen einer LDAP-Abfrage

Im folgenden Codebeispiel wird die Verwendung einer LDAP-Abfrage veranschaulicht.


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



Ausführliche Informationen zur Abfragesyntax finden Sie unter [Suchfiltersyntax.](search-filter-syntax.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchfiltersyntax](search-filter-syntax.md)
</dt> <dt>

[SQL Dialekt](sql-dialect.md)
</dt> <dt>

[Suchen mit der IDirectorySearch-Schnittstelle](searching-with-idirectorysearch.md)
</dt> <dt>

[Suchen mit ActiveX Datenobjekten](searching-with-activex-data-objects-ado.md)
</dt> <dt>

[Suchen mit OLE DB](searching-with-ole-db.md)
</dt> </dl>

 

 




