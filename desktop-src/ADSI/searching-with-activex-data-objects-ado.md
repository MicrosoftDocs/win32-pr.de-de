---
title: Suchen mit ActiveX Data Objects (ADO)
description: Das ADO-Modell (ActiveX Data Object) besteht aus den in der folgenden Tabelle aufgeführten Objekten.
ms.assetid: 27298f53-a652-49f2-a6e6-d92c7c6022af
ms.tgt_platform: multiple
keywords:
- ActiveX Data Objects ADSI, suchen mit ADO
- Suchen mit ActiveX Data Objects ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e73f630892169c7086daf9bb1e7b6c13bfdf0a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341553"
---
# <a name="searching-with-activex-data-objects-ado"></a>Suchen mit ActiveX Data Objects (ADO)

Das ADO-Modell (ActiveX Data Object) besteht aus den in der folgenden Tabelle aufgeführten Objekten.



| Object         | BESCHREIBUNG                                                                                                                        |
|----------------|------------------------------------------------------------------------------------------------------------------------------------|
| **Connection** | Eine offene Verbindung mit einer OLE DB Datenquelle, z. b. ADSI.                                                                          |
| **Befehl**    | Definiert einen bestimmten Befehl, der für die Datenquelle ausgeführt werden soll.                                                                         |
| **Parameter**  | Eine optionale-Auflistung für alle Parameter, die für das Command-Objekt bereitgestellt werden sollen.                                                        |
| **Recordset**  | Ein Satz von Datensätzen aus einer Tabelle, einem Befehls Objekt oder einer SQL-Syntax. Ein Recordset kann ohne ein zugrunde liegendes Verbindungs Objekt erstellt werden. |
| **Feld**      | Eine einzelne Datenspalte in einem Recordset.                                                                                            |
| **Eigenschaft**   | Eine Auflistung von Werten, die vom Anbieter für ADO bereitgestellt werden.                                                                           |
| **Fehler**      | Enthält Daten zu Datenzugriffs Fehlern. Wird aktualisiert, wenn ein Fehler in einem einzelnen Vorgang auftritt.                                      |



 

Damit ADO mit ADSI kommunizieren kann, müssen mindestens zwei ADO-Objekte vorhanden sein: **Connection** und **Recordset**. Diese ADO-Objekte dienen zum Authentifizieren von Benutzern und zum Auflisten der Ergebnisse. In der Regel verwenden Sie ein **Command** -Objekt, um eine aktive Verbindung beizubehalten, Abfrage Parameter anzugeben, z. b. die Seitengröße und den Suchbereich, und eine Abfrage auszuführen. Weitere Informationen zur Suchfilter Syntax finden Sie unter [Syntax für Suchfilter](search-filter-syntax.md).

Das **Verbindungs** Objekt lädt den OLE DB Anbieter und überprüft die Anmelde Informationen des Benutzers. Aufrufen Sie in **Visual Basic die Funktion** "Funktion" mit "ADODB". Verbindung "zum Erstellen einer Instanz eines **Verbindungs** Objekts, und legen Sie dann die **Provider** -Eigenschaft des **Verbindungs** Objekts auf" ADSDSOObject "fest. ADODB. Connection "ist die ProgID des **Verbindungs** Objekts, und" ADSDSOObject "ist der Name des OLE DB Anbieters in ADSI. Wenn keine Anmelde Informationen angegeben sind, werden die Anmelde Informationen des aktuell angemeldeten Benutzers verwendet.

Im folgenden Codebeispiel wird gezeigt, wie eine Instanz eines **Verbindungs** Objekts erstellt wird.


```VB
Set con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
```



Im folgenden Codebeispiel wird gezeigt, wie eine Instanz eines **Verbindungs** Objekts erstellt wird.


```VB
<%
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
%>
```



Im folgenden Codebeispiel wird gezeigt, wie eine Instanz eines **Verbindungs** Objekts erstellt wird. Beachten Sie, dass Sie die ADO-Typbibliothek (msadoXX.dll) als einen der Verweise im Visual Basic Projekt einschließen müssen.


```VB
Dim Con As New Connection
con.Provider = "ADsDSOObject"
```



Geben Sie die Benutzer Authentifizierungsdaten an, indem Sie die Eigenschaften des **Verbindungs** Objekts festlegen. In der folgenden Tabelle sind die von ADSI unterstützten Eigenschaften für Benutzerauthentifizierung aufgeführt.



| Eigenschaft           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Benutzer-ID"          | Eine Zeichenfolge, die den Benutzer angibt, dessen Sicherheitskontext beim Ausführen der Suche verwendet wird. Weitere Informationen zum Format der Benutzernamen Zeichenfolge finden Sie unter [**iadsopendsobject:: opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject). Wenn nicht angegeben, ist der Standardwert der angemeldete Benutzer, oder der Benutzer hat den Aufruf durch den aufrufenden Prozess angenommen. |
| Password         | Eine Zeichenfolge, die das Kennwort des Benutzers angibt, der durch die Benutzer-ID identifiziert wird.                                                                                                                                                                                                                                                                      |
| "Kennwort verschlüsseln" | Ein boolescher Wert, der angibt, ob das Kennwort verschlüsselt ist. Der Standardwert ist **FALSE**.                                                                                                                                                                                                                                                    |
| "ADSI-Flag"        | Ein Satz von Flags aus der Enumeration der [**ADS- \_ \_ authentifizierungsenumeration**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) , die die Bindungs Authentifizierungs Optionen angeben. Der Standardwert ist 0.                                                                                                                                                                         |



 

Im folgenden Codebeispiel wird gezeigt, wie die-Eigenschaften festgelegt werden, bevor das **Command** -Objekt erstellt wird.


```VB
Set oConnect = CreateObject("ADODB.Connection")
oConnect.Provider = "ADsDSOObject"
oConnect.Properties("User ID") = stUser
oConnect.Properties("Password") = stPass
oConnect.Properties("Encrypt Password") = True
oConnect.Open "DS Query", stUser, stPass
```



Das zweite ADO-Objekt ist das **Command** -Objekt. Die ProgID des **Command** -Objekts ist "ADODB. Command". Mit diesem Objekt können Sie mithilfe der aktiven Verbindung Abfrage Anweisungen und andere Befehle an ADSI ausgeben. Das **Command** -Objekt verwendet seine **ActiveConnection** -Eigenschaft, um eine aktive Verbindung beizubehalten. Außerdem wird die **CommandText** -Eigenschaft zum Speichern von Abfrage Anweisungen verwaltet, die von einem Benutzer ausgegeben werden. Die Abfrage Anweisungen werden entweder im SQL- [Dialekt](sql-dialect.md) oder im [LDAP-Dialekt](ldap-dialect.md)ausgedrückt.

In den folgenden Codebeispielen wird gezeigt, wie ein **Befehls** Objekt erstellt wird.


```VB
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = oConnect
command.CommandText = 
"SELECT AdsPath, cn FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectClass = '*'"
```



Fügen Sie im folgenden Codebeispiel die ADO-Typbibliothek (msadoXX.dll) als einen der Verweise ein.


```VB
Dim command As New Command
Set command.ActiveConnection = oConnect
command.CommandText = "<LDAP://DC=Fabrikam,DC=com>;(objectClass=*);AdsPath, cn; subTree"
```



Suchoptionen für das **Command** -Objekt werden durch Festlegen der **Properties** -Eigenschaft angegeben. In der folgenden Tabelle sind die zulässigen benannten Eigenschaften für **Eigenschaften** aufgeführt.



| Benannte Eigenschaft      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Asynchronen      | Ein boolescher Wert, der angibt, ob die Suche synchron oder asynchron ist. Der Standardwert ist false (synchron). Ein synchroner Suchvorgang wird blockiert, bis der Server das gesamte Ergebnis oder für eine seitenweise Suche die gesamte Seite zurückgibt. Ein asynchroner Suchvorgang blockiert, bis eine Zeile der Suchergebnisse verfügbar ist, oder bis die durch die Timeout-Eigenschaft angegebene Zeit abläuft.                           |
| "Cache Ergebnisse"     | Ein boolescher Wert, der angibt, ob das Ergebnis auf der Clientseite zwischengespeichert werden soll. Der Standardwert ist " **true**". ADSI speichert das Resultset zwischen. Das Deaktivieren dieser Option kann für große Resultsets wünschenswert sein.                                                                                                                                                                                                    |
| "Verweigerungen"   | Ein Wert aus der [**Werbe \_ \_ \_ Einblendungen referenziert**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) die Enumeration, die angibt, wie die Suche auf Verweise verweist. Der Standardwert ist " **ADS \_ Chase \_ verweirals \_**". Weitere Informationen zu dieser Eigenschaft finden Sie unter [referenrals](/windows/desktop/AD/referrals).<br/>                                                                                                                                           |
| "Nur Spaltennamen" | Ein boolescher Wert, der angibt, dass bei der Suche nur der Name der Attribute abgerufen werden soll, denen Werte zugewiesen wurden. Der Standardwert ist **FALSE**.                                                                                                                                                                                                                                                       |
| "Deref-Aliase"     | Ein boolescher Wert, der angibt, ob Aliase von gefundenen Objekten aufgelöst werden. Der Standardwert ist **FALSE**.                                                                                                                                                                                                                                                                                                        |
| "Seitengröße"         | Ein ganzzahliger Wert, der das Paging schaltet und die maximale Anzahl von Objekten angibt, die in einem Resultset zurückgegeben werden sollen. Der Standardwert ist keine Seitengröße. Weitere Informationen finden Sie unter [Abrufen großer Resultsets](retrieving-large-results-sets.md).                                                                                                                                                                       |
| SearchScope       | Ein Wert aus der [**ADS- \_ scopeenumeration**](/windows/win32/api/iads/ne-iads-ads_scopeenum) -Enumeration, der den Suchbereich angibt. Der Standardwert ist die **AD- \_ Bereichs \_ Teilstruktur**.                                                                                                                                                                                                                                                                  |
| "Größenbeschränkung"        | Ein ganzzahliger Wert, der die Größenbeschränkung für die Suche angibt. Für Active Directory gibt die Größenbeschränkung die maximale Anzahl von zurückgegebenen Objekten an. Der Server beendet die Suche, wenn die Größenbeschränkung erreicht ist, und gibt die gesammelten Ergebnisse zurück. Der Standardwert ist "No Limit".                                                                                                                                  |
| "Sortieren nach"           | Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste von Attributen angibt, die als Sortierschlüssel verwendet werden sollen. Diese Eigenschaft funktioniert nur für Verzeichnisserver, die das LDAP-Steuerelement für die serverseitige Sortierung unterstützen. Active Directory unterstützt das Sortier Steuerelement, kann sich jedoch auf die Serverleistung auswirken, insbesondere dann, wenn das Resultset groß ist. Beachten Sie, dass Active Directory nur einen einzelnen Sortierschlüssel unterstützt. Der Standardwert ist keine Sortierung. |
| "Zeitlimit"        | Ein ganzzahliger Wert, der das Zeitlimit für die Suche in Sekunden angibt. Wenn das Zeitlimit erreicht ist, beendet der Server die Suche und gibt die gesammelten Ergebnisse zurück. Der Standardwert ist kein Zeit Limit.                                                                                                                                                                                                      |
| Zeit           | Ein ganzzahliger Wert, der den Client seitigen Timeout Wert in Sekunden angibt. Dieser Wert gibt die Zeit an, die der Client auf Ergebnisse vom Server wartet, bevor die Suche beendet wird. Der Standardwert ist kein Timeout.                                                                                                                                                                                                  |



 

Im folgenden Codebeispiel wird gezeigt, wie Suchoptionen festgelegt werden.


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



Das dritte ADO-Objekt ist **Recordset**. Sie erhalten dieses Objekt, wenn Sie die **Execute** -Methode für ein **Command** -Objekt aufrufen. Die primäre Funktion des **Recordset** -Objekts ist das Aufzählen des Resultsets und das Abrufen der Daten. Das Resultset kann Werte für Attribute enthalten, die sowohl einzelne als auch mehrere Werte aufweisen. Das erhalten eines einwertigen Attributs ist einfach, ähnlich wie beim erhalten des Spaltenwerts in der relationalen Datenbank, z. b.:


```VB
Fields('name').Value
```



Es ist jedoch schwieriger, ein Attribut mit mehreren Werten zu erhalten. In diesem Fall ist " **field. Value** " ein Array, und Sie müssen die untere und obere Grenze des Arrays überprüfen, wie im folgenden Codebeispiel gezeigt.


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

 

