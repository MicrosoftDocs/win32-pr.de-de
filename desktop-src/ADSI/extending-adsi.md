---
title: Erweitern von ADSI
description: Mit dem ADSI-Erweiterungsmodell können Sie eine Verzeichnisklasse Ihrem eigenen COM-Objekt zuordnen.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428453"
---
# <a name="extending-adsi"></a>Erweitern von ADSI

Mit dem ADSI-Erweiterungsmodell können Sie eine Verzeichnisklasse Ihrem eigenen COM-Objekt zuordnen. Aus Sicht eines ADSI-Programmierers oder Skriptwriters wird die Erweiterung zu einem integralen Bestandteil von ADSI. Wenn beispielsweise ein neuer Mitarbeiter fabrikam beitritt, erstellt der Windows NT-Administrator ein Benutzerobjekt im Verzeichnis, und der Gehaltsadministrator muss einige Einträge in den Personalsystemen für diesen Benutzer einrichten. Mit einer ADSI-Erweiterung kann dieser Prozess in einem einzigen Skript optimiert werden.


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



Weitere Informationen finden Sie unter [ADSI-Erweiterungen.](adsi-extensions.md)

 

 




