---
title: Suchen nach Objekten
description: Julie Bankert muss Telefonnummern für alle Programmleiter finden, die in Abteilung 101 arbeiten. Sie kann dazu ein Skript erstellen, das ADO und ADSI verwendet.
ms.assetid: c6325068-4ae2-4348-9938-96402262cd43
ms.tgt_platform: multiple
keywords:
- Suchen nach Objekten ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd41e87ad3396694b2f87158b15278c1dfbe28b044ad03ebbb09ddded705910a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973502"
---
# <a name="searching-for-objects"></a>Suchen nach Objekten

Julie Bankert muss Telefonnummern für alle Programmleiter finden, die in Abteilung 101 arbeiten. Sie kann dazu ein Skript erstellen, das ADO und ADSI verwendet.

Wenn der ADO-Anbieter zum Ausführen einer Abfrage verwendet wird, gibt das Resultset nur die ersten 1000 Objekte zurück. Aus diesem Grund ist es wichtig, eine ausgelagerungte Abfrage zu verwenden, damit Sie alle Objekte im Resultset abrufen können, solange der Verzeichnisdienst nicht festgelegt wurde, um die Anzahl der Elemente in einem Resultset einzuschränken. Rückgabesätze enthalten die Anzahl der Elemente, die Sie in der Seitengröße angeben, und ausgelagerungssätze werden weiterhin zurückgegeben, bis alle Elemente im Resultset zurückgegeben wurden.


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



Um eine ADSI-Suche in Visual Basic oder einer Skriptumgebung durchzuführen, sind drei ADO-Komponenten erforderlich: **Connection**, **Command** und **Recordset**. Mit dem **Connection-Objekt** können Sie den Anbieternamen, ggf. alternative Anmeldeinformationen und andere Flags angeben. Mit dem **Command-Objekt** können Sie Sucheinstellungen und die Abfragezeichenfolge angeben. Sie müssen das **Connection-Objekt** vor der Ausführung der Abfrage einem **Command-Objekt** zuordnen. Schließlich wird das **Recordset-Objekt** verwendet, um das Resultset zu iterieren.

ADSI unterstützt zwei Arten von Abfragezeichenfolgen oder Dialekten. Im obigen Codebeispiel wird der SQL Dialekt verwendet. Sie können auch den LDAP-Dialekt verwenden. Die LDAP-Dialektabfragezeichenfolge basiert auf [RFC 2254](https://www.ietf.org/rfc/rfc2254.txt) (ein RFC ist ein Dokument zum Anfordern von Kommentaren, das die Grundlage für die Entwicklung von LDAP-Standards bildet). Das vorherige Beispiel kann in das folgende Codebeispiel übersetzt werden.


```VB
oCommand1.CommandText = "<LDAP://DC=fabrikam,DC=COM>;" & _
"(&(objectCategory=Person)" & _
"(objectClass=user)" & _
"(title=ProgramManager)" & _
"(department=101));" & _
"name,telephoneNumber;subTree"
```



Warum befindet sich das Wort "subtree" am Ende der Zeichenfolge? In der Verzeichniswelt können Sie den Suchbereich angeben. Folgende Optionen stehen zur Auswahl: "base", "onelevel" und "subtree". "base" wird verwendet, um das Objekt selbst zu lesen. "onelevel" bezieht sich auf die unmittelbar untergeordneten Elemente, ähnlich wie der **Dir-Befehl.** "subtree" wird verwendet, um mehrere Ebenen zu durchsuchen (ähnlich wie **dir /s**).

Mit dem SQL Dialekt können Sie den Bereich in der Befehlseigenschaft angeben, z. B. im folgenden Codebeispiel.


```VB
oCommand1.Properties("SearchScope") = ADS_SCOPE_ONELEVEL
```



Wenn scope nicht angegeben ist, wird standardmäßig eine Unterstruktursuche verwendet.

> [!Note]  
> Wenn Sie C++ verwenden, können Sie die [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) von ADSI verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Reorganisation](reorganization.md)
</dt> </dl>

 

 




