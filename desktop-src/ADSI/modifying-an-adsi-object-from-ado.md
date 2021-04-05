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
# <a name="modifying-an-adsi-object-from-ado"></a><span data-ttu-id="0a276-107">Ändern eines ADSI-Objekts aus ADO</span><span class="sxs-lookup"><span data-stu-id="0a276-107">Modifying an ADSI Object from ADO</span></span>

<span data-ttu-id="0a276-108">ADSI für Windows 2000 und der DS-Client enthalten einen schreibgeschützten OLE DB Anbieter.</span><span class="sxs-lookup"><span data-stu-id="0a276-108">ADSI for Windows 2000 and DS Client includes a read-only OLE DB provider.</span></span> <span data-ttu-id="0a276-109">Dies bedeutet, dass Sie derzeit nicht die Update-Anweisung im SQL-Dialekt ausgeben können.</span><span class="sxs-lookup"><span data-stu-id="0a276-109">This means that you cannot, at present, issue the UPDATE statement in the SQL dialect.</span></span>

<span data-ttu-id="0a276-110">**So ändern Sie ein von einer ADO-Abfrage zurück gegebenes Objekt**</span><span class="sxs-lookup"><span data-stu-id="0a276-110">**To modify an object returned from an ADO query**</span></span>

1.  <span data-ttu-id="0a276-111">Fordern Sie den **ADsPath** beim Angeben eines Attribut namens an, wie in "Select ADsPath,...".</span><span class="sxs-lookup"><span data-stu-id="0a276-111">Request the **ADsPath** when specifying an attribute name, as in "SELECT ADsPath, ..."</span></span>
2.  <span data-ttu-id="0a276-112">Führen Sie die Abfrage aus, und erhalten Sie das **ADsPath** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="0a276-112">Execute the query and get the **ADsPath** attribute.</span></span>
3.  <span data-ttu-id="0a276-113">Binden Sie die Bindung an den Daten Satz Satz mithilfe von **ADsPath**, und ändern Sie die Attribute.</span><span class="sxs-lookup"><span data-stu-id="0a276-113">Bind to the record set using **ADsPath**, and modify the attributes.</span></span>

<span data-ttu-id="0a276-114">Im folgenden Codebeispiel wird gezeigt, wie ein ADSI-Objekt geändert wird, nachdem die im vorherigen Beispiel beschriebenen Schritte ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="0a276-114">The following code example shows how to modify an ADSI object after performing the steps outlined in the preceding example.</span></span>


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



 

 




