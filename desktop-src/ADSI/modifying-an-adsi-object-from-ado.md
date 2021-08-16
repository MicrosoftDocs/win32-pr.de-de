---
title: Ändern eines ADSI-Objekts aus ADO
description: ADSI für Windows 2000 und DS-Client enthält einen schreibgeschützten OLE DB Anbieter. Dies bedeutet, dass Sie derzeit die UPDATE-Anweisung nicht im dialektischen SQL können.
ms.assetid: b0a107ed-0271-45ab-b971-f589f34472e2
ms.tgt_platform: multiple
keywords:
- Ändern eines ADSI-Objekts aus ADO ADSI
- ActiveX Datenobjekt ADSI , ändern eines ADSI-Objekts aus ADO
- ADSI ADSI , Beispielcode C/C++ , Ändern eines ADSI-Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4562e67043ea168a0b158088ffe3c2772f3ae28a0a2fa8881e102574cf2eb97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839450"
---
# <a name="modifying-an-adsi-object-from-ado"></a>Ändern eines ADSI-Objekts aus ADO

ADSI für Windows 2000 und DS-Client enthält einen schreibgeschützten OLE DB Anbieter. Dies bedeutet, dass Sie derzeit die UPDATE-Anweisung nicht im dialektischen SQL können.

**So ändern Sie ein von einer ADO-Abfrage zurückgegebenes Objekt**

1.  Fordern Sie **den ADsPath** an, wenn Sie einen Attributnamen angeben, wie in "SELECT ADsPath, ..."
2.  Führen Sie die Abfrage aus, und erhalten Sie **das ADsPath-Attribut.**
3.  Binden Sie mithilfe von **ADsPath** an den Datensatzsatz, und ändern Sie die Attribute.

Das folgende Codebeispiel zeigt, wie Sie ein ADSI-Objekt ändern, nachdem Sie die im vorherigen Beispiel beschriebenen Schritte ausführen.


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



 

 




