---
title: Erweitern von ADSI
description: Mit dem ADSI-Erweiterungs Modell können Sie Ihrem eigenen com-Objekt eine Verzeichnis Klasse zuordnen.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707427"
---
# <a name="extending-adsi"></a>Erweitern von ADSI

Mit dem ADSI-Erweiterungs Modell können Sie Ihrem eigenen com-Objekt eine Verzeichnis Klasse zuordnen. Aus der Perspektive eines ADSI-Programmierers oder Skripts wird die Erweiterung zu einem integralen Bestandteil von ADSI. Wenn ein neuer Mitarbeiter z. b. mit Fabrikam verbunden ist, erstellt der Windows NT-Administrator ein Benutzerobjekt im Verzeichnis, und der Gehalts Erstellungs Administrator muss einige Einträge in den Personalressourcen Systemen für diesen Benutzer einrichten. Mit einer ADSI-Erweiterung kann dieser Prozess in einem einzelnen Skript optimiert werden.


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



Weitere Informationen finden Sie unter [ADSI Extensions](adsi-extensions.md).

 

 




