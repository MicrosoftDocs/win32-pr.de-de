---
title: Ändern eines ADSI-Objekts aus ADO
description: ADSI für Windows 2000 und der DS-Client enthalten einen schreibgeschützten OLE DB Anbieter. Dies bedeutet, dass Sie derzeit nicht die Update-Anweisung im SQL-Dialekt ausgeben können.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Ändern eines ADSI-Objekts aus ADO ADSI
- ActiveX-Datenobjekt-ADSI, Ändern eines ADSI-Objekts aus ADO
- ADSI ADSI, Beispielcode C/C++, Ändern eines ADSI-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7291088915a537231077e1d75161b57684caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707409"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Ändern eines ADSI-Objekts aus ADO

ADSI für Windows 2000 und der DS-Client enthalten einen schreibgeschützten OLE DB Anbieter. Dies bedeutet, dass Sie derzeit nicht die Update-Anweisung im SQL-Dialekt ausgeben können.

**So ändern Sie ein von einer ADO-Abfrage zurück gegebenes Objekt**

1.  Fordern Sie den **ADsPath** beim Angeben eines Attribut namens an, wie in "Select ADsPath,...".
2.  Führen Sie die Abfrage aus, und erhalten Sie das **ADsPath** -Attribut.
3.  Binden Sie die Bindung an den Daten Satz Satz mithilfe von **ADsPath**, und ändern Sie die Attribute.

Im folgenden Codebeispiel wird gezeigt, wie ein ADSI-Objekt geändert wird, nachdem die im vorherigen Beispiel beschriebenen Schritte ausgeführt wurden.


```VB
Dim Con As New Connection
Dim rs As New Recordset
Dim command As New Command
Dim usr As IADsUser

' Replace department for all users in OU=sales.
Set con = Server.CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
 
Set command = CreateObject("ADODB.Command")
Set command.ActiveConnection = con
 
command.CommandText = "SELECT AdsPath, cn FROM 'LDAP://OU=Sales,DC=Fabrikam,DC=com' WHERE objectClass = 'user'"
 
command.Properties("searchscope") = ADS_SCOPE_ONELEVEL
Set rs = command.Execute
While Not rs.EOF
    Set usr = GetObject(rs.Fields("AdsPath").Value)
    usr.Put "department", "1001"
    usr.SetInfo
    rs.MoveNext
Wend
```



 

 




