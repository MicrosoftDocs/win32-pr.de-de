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
# <a name="extending-adsi"></a><span data-ttu-id="10a17-103">Erweitern von ADSI</span><span class="sxs-lookup"><span data-stu-id="10a17-103">Extending ADSI</span></span>

<span data-ttu-id="10a17-104">Mit dem ADSI-Erweiterungs Modell können Sie Ihrem eigenen com-Objekt eine Verzeichnis Klasse zuordnen.</span><span class="sxs-lookup"><span data-stu-id="10a17-104">With the ADSI extension model, you can associate a directory class with your own COM object.</span></span> <span data-ttu-id="10a17-105">Aus der Perspektive eines ADSI-Programmierers oder Skripts wird die Erweiterung zu einem integralen Bestandteil von ADSI.</span><span class="sxs-lookup"><span data-stu-id="10a17-105">From an ADSI programmer or script writer's perspective, the extension becomes an integral part of ADSI.</span></span> <span data-ttu-id="10a17-106">Wenn ein neuer Mitarbeiter z. b. mit Fabrikam verbunden ist, erstellt der Windows NT-Administrator ein Benutzerobjekt im Verzeichnis, und der Gehalts Erstellungs Administrator muss einige Einträge in den Personalressourcen Systemen für diesen Benutzer einrichten.</span><span class="sxs-lookup"><span data-stu-id="10a17-106">For example, when a new employee joins Fabrikam, the Windows NT administrator will create a user object in the directory and the payroll administrator will need to set up some entries in the human resource systems for this user.</span></span> <span data-ttu-id="10a17-107">Mit einer ADSI-Erweiterung kann dieser Prozess in einem einzelnen Skript optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="10a17-107">With an ADSI extension, this process can be streamlined into one single script.</span></span>


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



<span data-ttu-id="10a17-108">Weitere Informationen finden Sie unter [ADSI Extensions](adsi-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="10a17-108">For more information, see [ADSI Extensions](adsi-extensions.md).</span></span>

 

 




