---
title: Auflisten von Objekten
description: Zum Anzeigen des untergeordneten Objekts eines Containers, z. b. einer Organisationseinheit (OE), zählen Sie das Container Objekt.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Auflisten von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855320"
---
# <a name="enumerating-objects"></a>Auflisten von Objekten

Zum Anzeigen des untergeordneten Objekts eines Containers, z. b. einer Organisationseinheit (OE), zählen Sie das Container Objekt. Um eine Analogie zu einem Dateisystem zu erstellen, entspricht das untergeordnete Objekt den Dateien im Verzeichnis, während der Container, der das übergeordnete Objekt ist, dem Verzeichnis selbst entspricht. Sie können auch den auflisten-Vorgang verwenden, wenn Sie das übergeordnete Objekt eines Objekts abrufen möchten.

Wenn Sie ein Objekt auflisten, binden Sie tatsächlich an ein Objekt im Verzeichnis, und für jedes Objekt wird eine [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle zurückgegeben.

Im folgenden Codebeispiel wird gezeigt, wie die untergeordneten Elemente eines Containers aufgelistet werden.


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



Sie können die Typen von Objekten filtern, die von der-Enumeration zurückgegeben werden. Wenn Sie z. b. nur Benutzer und Gruppen anzeigen möchten, verwenden Sie das folgende Codebeispiel vor der-Enumeration.


```VB
Ou.Filter = Array("user", "group")
```



Wenn Sie über einen Objekt Verweis verfügen, können Sie das übergeordnete Objekt des Objekts mit der über [**geordneten**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Eigenschaft erhalten. Im folgenden Codebeispiel wird gezeigt, wie eine Bindung an das übergeordnete Objekt erfolgen kann.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Weitere Informationen finden Sie unter Auflisten von [ADSI-Objekten](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen nach Objekten](searching-for-objects.md)
</dt> </dl>

 

 




