---
title: Suchen nach Objekten
description: Julie Bankert muss Telefonnummern für alle Programm-Manager finden, die in der Abteilung 101 arbeiten. Sie können ein Skript erstellen, das ADO und ADSI verwendet, um dies zu erreichen.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Suchen nach Objekten ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3c26f05b63524e3a657c0c460efb921978bd19
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103858040"
---
# <a name="searching-for-objects"></a>Suchen nach Objekten

Julie Bankert muss Telefonnummern für alle Programm-Manager finden, die in der Abteilung 101 arbeiten. Sie können ein Skript erstellen, das ADO und ADSI verwendet, um dies zu erreichen.

Wenn der ADO-Anbieter zum Ausführen einer Abfrage verwendet wird, gibt das Resultset nur die ersten 1000-Objekte zurück. Aus diesem Grund ist es wichtig, eine auslagerbare Abfrage zu verwenden, damit Sie alle Objekte im Resultset abrufen können, solange der Verzeichnisdienst nicht so festgelegt wurde, dass die Anzahl der Elemente in einem Resultset beschränkt wird. Rückgabe Sätze enthalten die Anzahl der Elemente, die Sie im Seiten Format angeben, und Auslagerungs Gruppen werden weiterhin zurückgegeben, bis alle Elemente im Resultset zurückgegeben wurden.


```VB
' Create the connection and command object.
Set oConnection1 = CreateObject("ADODB.Connection")
Set oCommand1 = CreateObject("ADODB.Command")
' Open the connection.
oConnection1.Provider = "ADsDSOObject"  ' This is the ADSI OLE-DB provider name
oConnection1.Open "Active Directory Provider"
' Create a command object for this connection.
Set oCommand1.ActiveConnection = oConnection1

' Compose a search string.
oCommand1.CommandText = "select name,telephoneNumber " & _
"from 'LDAP://DC=Fabrikam,DC=com'" & _
"WHERE objectCategory='Person'" & _
"AND objectClass='user'" & _
"AND title='Program Manager'" & _
"AND department=101"

' Execute the query.
Set rs = oCommand1.Execute
'--------------------------------------
' Navigate the record set
'--------------------------------------
While Not rs.EOF
    Debug.Print rs.Fields("Name") & " , " & rs.Fields("telephoneNumber")
    rs.MoveNext
Wend
```



Zum Ausführen einer ADSI-Suche in Visual Basic oder einer Skript Umgebung sind drei ADO-Komponenten erforderlich: **Connection**, **Command** und **Recordset**. Das **Connection** -Objekt ermöglicht Ihnen, ggf. den Anbieter Namen, Alternative Anmelde Informationen und andere Flags anzugeben. Das **Command** -Objekt ermöglicht es Ihnen, Sucheinstellungen und die Abfrage Zeichenfolge anzugeben. Sie müssen das **Verbindungs** Objekt einem **Befehls** Objekt vor der Ausführung der Abfrage zuordnen. Zum Schluss wird das **Recordset** -Objekt verwendet, um das Resultset zu durchlaufen.

ADSI unterstützt zwei Typen von Abfrage Zeichenfolgen oder-Dialekten. Im vorangehenden Codebeispiel wird der SQL-Dialekt verwendet. Sie können auch den LDAP-Dialekt verwenden. Die Abfrage Zeichenfolge des LDAP-Dialekts basiert auf [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (eine RFC ist eine Anforderung für ein Kommentar Dokument, das die Grundlage für die Entwicklung von LDAP-Standards ist). Das vorangehende Beispiel kann in das folgende Codebeispiel übersetzt werden.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Warum ist das Wort "subtree" am Ende der Zeichenfolge? In der Verzeichnis Welt können Sie den Suchbereich angeben. Folgende Optionen stehen zur Auswahl: "Base", "onelevel" und "subtree". "Base" wird verwendet, um das Objekt selbst zu lesen. "onelevel" bezieht sich auf die unmittelbaren untergeordneten Elemente, ähnlich wie der **dir** -Befehl. "subtree" wird verwendet, um Tiefe oder mehrere Ebenen zu durchsuchen (ähnlich wie **dir/s**).

Mit dem SQL-Dialekt können Sie den Bereich in der Befehls Eigenschaft angeben, z. b. im folgenden Codebeispiel.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Wenn der Bereich nicht angegeben wird, wird standardmäßig eine Unterstruktur Suche verwendet.

> [!Note]  
> Wenn Sie C++ verwenden, können Sie die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle von ADSI verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuorganisation](reorganization.md)
</dt> </dl>

 

 




