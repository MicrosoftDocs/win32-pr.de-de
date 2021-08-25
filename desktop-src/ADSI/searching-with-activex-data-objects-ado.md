---
title: Suchen mit ActiveX Data Objects (ADO)
description: Das ActiveX ADO-Modell (Data Object) besteht aus objekten, die in der folgenden Tabelle aufgeführt sind.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI , Suchen mit ADO
- Suchen mit ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52eba3dd5bc9013500aa4def7a31104d1408d4818b78a35ff75f09f2454f4d21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770450"
---
# <a name="searching-with-activex-data-objects-ado"></a>Suchen mit ActiveX Data Objects (ADO)

Das ActiveX ADO-Modell (Data Object) besteht aus objekten, die in der folgenden Tabelle aufgeführt sind.



| Object         | BESCHREIBUNG                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Connection** | Eine offene Verbindung mit einer OLE DB Datenquelle wie ADSI.                                                                          |
| **Befehl**    | Definiert einen bestimmten Befehl, der für die Datenquelle ausgeführt werden soll.                                                                         |
| **Parameter**  | Eine optionale Auflistung für alle Parameter, die für das Befehlsobjekt angegeben werden.                                                        |
| **Recordset**  | Ein Satz von Datensätzen aus einer Tabelle, einem Befehlsobjekt oder einer SQL Syntax. Ein Recordset kann ohne zugrunde liegendes Verbindungsobjekt erstellt werden. |
| **Feld**      | Eine einzelne Datenspalte in einem Recordset.                                                                                            |
| **Eigenschaft**   | Eine Auflistung von Werten, die vom Anbieter für ADO bereitgestellt werden.                                                                           |
| **Fehler**      | Enthält Daten zu Datenzugriffsfehlern. Wird aktualisiert, wenn ein Fehler in einem einzelnen Vorgang auftritt.                                      |



 

Damit ADO mit ADSI kommunizieren kann, müssen mindestens zwei ADO-Objekte enthalten sein: **Connection** und **RecordSet**. Diese ADO-Objekte dienen zur Authentifizierung von Benutzern bzw. zum Aufzählen von Ergebnissen. In der Regel verwenden  Sie auch ein Command-Objekt, um eine aktive Verbindung zu verwalten, Abfrageparameter wie Seitengröße und Suchbereich anzugeben und eine Abfrage auszuführen. Weitere Informationen zur Suchfiltersyntax finden Sie unter [Suchfiltersyntax](search-filter-syntax.md).

Das **Connection-Objekt** lädt OLE DB Anbieter und überprüft Die Benutzeranmeldeinformationen. Rufen Visual Basic **CreateObject-Funktion** mit "ADODB" auf. Verbindung", um eine Instanz eines **Connection-Objekts** zu erstellen, und legen Sie dann die **Provider-Eigenschaft** des **Connection-Objekts** auf "ADsDSOObject" fest. "ADODB. Connection" ist die ProgID des **Connection-Objekts,** und "ADsDSOObject" ist der Name des OLE DB Anbieters in ADSI. Wenn keine Anmeldeinformationen angegeben werden, werden die Anmeldeinformationen des aktuell angemeldeten Benutzers verwendet.

Das folgende Codebeispiel zeigt, wie eine Instanz eines **Connection-Objekts erstellt** wird.


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



Das folgende Codebeispiel zeigt, wie eine Instanz eines **Connection-Objekts erstellt** wird.


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



Das folgende Codebeispiel zeigt, wie eine Instanz eines **Connection-Objekts erstellt** wird. Beachten Sie, dass Sie die ADO-Typbibliothek (msadoXX.dll) als einen der Verweise in das Projekt Visual Basic müssen.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Geben Sie Benutzerauthentifizierungsdaten an, indem Sie die Eigenschaften des **Connection-Objekts** festlegen. In der folgenden Tabelle sind adsI-unterstützte Benutzerauthentifizierungseigenschaften aufgeführt.



| Eigenschaft           | Beschreibung                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Benutzer-ID"          | Eine Zeichenfolge, die den Benutzer identifiziert, dessen Sicherheitskontext beim Ausführen der Suche verwendet wird. Weitere Informationen zum Format der Benutzernamenzeichenfolge finden Sie unter [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Wenn nicht angegeben, ist der Standardwert der angemeldete Benutzer oder der Benutzer, der durch den aufrufenden Prozess die Identität angenommen hat. |
| Password         | Eine Zeichenfolge, die das Kennwort des Benutzers angibt, der durch "Benutzer-ID" identifiziert wird.                                                                                                                                                                                                                                                                      |
| "Kennwort verschlüsseln" | Ein boolescher Wert, der angibt, ob das Kennwort verschlüsselt ist. Der Standardwert ist **FALSE**.                                                                                                                                                                                                                                                    |
| "ADSI-Flag"        | Ein Satz von Flags aus der [**ADS \_ AUTHENTICATION \_ ENUM-Enumeration,**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) die die Bindungsauthentifizierungsoptionen angeben. Der Standardwert ist 0.                                                                                                                                                                         |



 

Das folgende Codebeispiel zeigt, wie die Eigenschaften vor dem Erstellen des **Command-Objekts festgelegt** werden.


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



Das zweite ADO-Objekt ist das **Command-Objekt.** Die ProgID des **Command-Objekts** ist "ADODB.Command". Mit diesem Objekt können Sie Abfrage-Anweisungen und andere Befehle über die aktive Verbindung an ADSI senden. Das **Command-Objekt** verwendet seine **ActiveConnection-Eigenschaft,** um eine aktive Verbindung zu verwalten. Außerdem wird die **CommandText-Eigenschaft** verwaltet, um von einem Benutzer ausgegebene Abfrageaufforderungen zu enthalten. Die Abfrage-Anweisungen werden entweder im [SQL-Dialekt oder](sql-dialect.md) im [LDAP-Dialekt ausgedrückt.](ldap-dialect.md)

In den folgenden Codebeispielen wird das Erstellen eines **Command-Objekts** gezeigt.


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



Schließen Sie im folgenden Codebeispiel die ADO-Typbibliothek (msadoXX.dll) als einen der Verweise ein.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



Suchoptionen für das **Command-Objekt** werden durch Festlegen der **Properties-Eigenschaft** angegeben. In der folgenden Tabelle sind zulässige benannte Eigenschaften für Eigenschaften **aufgeführt.**



| Benannte Eigenschaft      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Asynchron"      | Ein boolescher Wert, der angibt, ob die Suche synchron oder asynchron ist. Der Standardwert ist False (synchron). Eine synchrone Suche wird blockiert, bis der Server das gesamte Ergebnis oder bei einer seitenseitigen Suche die gesamte Seite zurückgibt. Eine asynchrone Suche wird blockiert, bis eine Zeile der Suchergebnisse verfügbar ist oder bis die von der Eigenschaft "Timeout" angegebene Zeit verstrichen ist.                           |
| "Ergebnisse zwischenspeichern"     | Ein boolescher Wert, der angibt, ob das Ergebnis clientseitig zwischengespeichert werden soll. Der Standardwert ist **true.** ADSI speichert das Ergebnisset zwischen. Das Deaktivieren dieser Option kann bei großen ResultSets wünschenswert sein.                                                                                                                                                                                                    |
| "Empfehlungsempfehlungen"   | Ein Wert aus der [**ADS \_ ADS ADS \_ \_ REFERRALS-ENUM,**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) der angibt, wie die Suche Empfehlungen durchsucht. Der Standardwert ist **ADS \_ ADS \_ REFERRALS \_ NEVER**. Weitere Informationen zu dieser Eigenschaft finden Sie unter [Empfehlungen.](/windows/desktop/AD/referrals)<br/>                                                                                                                                           |
| "Nur Spaltennamen" | Ein boolescher Wert, der angibt, dass bei der Suche nur der Name der Attribute abgerufen werden soll, denen Werte zugewiesen wurden. Der Standardwert ist **FALSE**.                                                                                                                                                                                                                                                       |
| "Deref-Aliase"     | Ein boolescher Wert, der angibt, ob Aliase gefundener Objekte aufgelöst werden. Der Standardwert ist **FALSE**.                                                                                                                                                                                                                                                                                                        |
| "Seitengröße"         | Ein ganzzahliger Wert, der paging aktiviert und die maximale Anzahl von Objekten angibt, die in einem Resultset zurückgegeben werden. Der Standardwert ist keine Seitengröße. Weitere Informationen finden Sie unter [Abrufen großer Resultsets.](retrieving-large-results-sets.md)                                                                                                                                                                       |
| "SearchScope"       | Ein Wert aus der [**ADS \_ SCOPEENUM-Enumeration,**](/windows/win32/api/iads/ne-iads-ads_scopeenum) der den Suchbereich angibt. Der Standardwert ist **ADS \_ SCOPE \_ SUBTREE.**                                                                                                                                                                                                                                                                  |
| "Größenbeschränkung"        | Ein ganzzahliger Wert, der die Größenbeschränkung für die Suche angibt. Für Active Directory gibt das Größenlimit die maximale Anzahl zurückgegebener Objekte an. Der Server beendet die Suche, wenn das Größenlimit erreicht ist, und gibt die gesammelten Ergebnisse zurück. Der Standardwert ist "no limit".                                                                                                                                  |
| "Sortieren nach"           | Eine Zeichenfolge, die eine durch Komma getrennte Liste von Attributen angibt, die als Sortierschlüssel verwendet werden. Diese Eigenschaft funktioniert nur für Verzeichnisserver, die das LDAP-Steuerelement für die serverseitige Sortierung unterstützen. Active Directory unterstützt das Sortiersteuersystem, kann sich jedoch auf die Serverleistung auswirken, insbesondere wenn das Resultseset groß ist. Beachten Sie, dass Active Directory nur einen einzelnen Sortierschlüssel unterstützt. Der Standardwert ist keine Sortierung. |
| "Zeitlimit"        | Ein ganzzahliger Wert, der das Zeitlimit für die Suche in Sekunden angibt. Wenn das Zeitlimit erreicht ist, beendet der Server die Suche und gibt die gesammelten Ergebnisse zurück. Der Standardwert ist kein Zeitlimit.                                                                                                                                                                                                      |
| "Timeout"           | Ein ganzzahliger Wert, der den clientseitigen Timeoutwert in Sekunden angibt. Dieser Wert gibt an, wie lange der Client auf Ergebnisse vom Server wartet, bevor die Suche beendet wird. Der Standardwert ist kein Time out.                                                                                                                                                                                                  |



 

Das folgende Codebeispiel zeigt, wie Suchoptionen festgelegt werden.


```VB
Const ADS_SCOPE_ONELEVEL = 1
Const ADS_CHASE_REFERRALS_EXTERNAL = &H40

Dim Com As New Command
 
Com.Properties("Page Size") = 999
Com.Properties("Timeout") = 30     ' Seconds
Com.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Com.Properties("Chase referrals") = ADS_CHASE_REFERRALS_EXTERNAL
Com.Properties("Cache Results") = False     ' Do not cache the result set.
```



Das dritte ADO-Objekt ist **RecordSet.** Sie erhalten dieses Objekt, wenn Sie die **Execute-Methode** für ein **Command-Objekt** aufrufen. Die primäre Funktion des **RecordSet-Objekts** besteht darin, das Resultset aufzuzählen und die Daten abzurufen. Das Resultset kann Werte für Attribute enthalten, die sowohl einzelne als auch mehrere Werte aufweisen. Das Abrufen eines einwertigen Attributs ist einfach, ähnlich wie das Abrufen des Spaltenwerts in der relationalen Datenbank, z. B.:


```VB
Fields('name').Value
```



Das Abrufen eines Attributs mit mehreren Werten ist jedoch schwieriger. In diesem Fall ist **Field.Value** ein Array, und Sie müssen die untere und obere Grenze des Arrays überprüfen, wie im folgenden Codebeispiel gezeigt.


```VB
Set rs = Com.Execute
 
For i = 0 To rs.Fields.Count - 1
    Debug.Print rs.Fields(i).Name, rs.Fields(i).Type
Next i
 
'--------------------------
' Navigate the record set.
'--------------------------
rs.MoveFirst
lstResult.Clear      ' Clear the user interface.
While Not rs.EOF
For i = 0 To rs.Fields.Count - 1
    ' For Multi Value attribute
    If rs.Fields(i).Type = adVariant And Not (IsNull(rs.Fields(i).Value)) Then
        Debug.Print rs.Fields(i).Name, " = "
        For j = LBound(rs.Fields(i).Value) To UBound(rs.Fields(i).Value)
            Debug.Print rs.Fields(i).Value(j), " # "
            lstResult.AddItem rs.Fields(i).Value(j)
        Next j
    Else
        ' For Single Value attribute.
         Debug.Print rs.Fields(i).Name, " = ", rs.Fields(i).Value
         lstResult.AddItem rs.Fields(i).Value
    End If
Next i
rs.MoveNext
Wend
```



Im folgenden Codebeispiel werden die Benutzerkonten auf einem LDAP-Server deaktiviert.


```VB
Dim X as IADs
Dim con As New Connection, rs As New Recordset
Dim MyUser As IADsUser
 
con.Provider = "ADsDSOObject"
con.Open "Active Directory Provider", "CN=Test,CN=Users,DC=Fabrikam,DC=COM,O=INTERNET", "Password"
Set rs = con.Execute("<LDAP://MyMachine/DC=MyDomain,DC=Fabrikam,DC=com>;(objectClass=User);ADsPath;onelevel")
 
While Not rs.EOF
    ' Bind to the object to make changes 
    ' to it because ADO is currently read-only.
    MyUser = GetObject(rs.Fields(0).Value)
    MyUser.AccountDisabled = True
    MyUser.SetInfo
    rs.MoveNext
Wend
```



Weitere Informationen zum ADO-Objektmodell finden Sie unter [Microsoft ActiveX Data Objects](/sql/ado/microsoft-activex-data-objects-ado?view=sql-server-ver15).

 

