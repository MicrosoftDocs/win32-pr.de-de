---
title: Aufzählen von Objekten
description: Um das untergeordnete Objekt eines Containers anzuzeigen, z. B. eine Organisationseinheit (OE), müssen Sie das Containerobjekt aufzählen.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Aufzählen von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e4bcead2d3fc8f98daeada89cdd10b3ad30bed855563efd89b3eebce8995f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961949"
---
# <a name="enumerating-objects"></a>Aufzählen von Objekten

Um das untergeordnete Objekt eines Containers anzuzeigen, z. B. eine Organisationseinheit (OE), müssen Sie das Containerobjekt aufzählen. Um eine Analogie zu einem Dateisystem herzustellen, würde das untergeordnete Objekt Dateien im Verzeichnis entsprechen, während der Container, bei dem es sich um das übergeordnete Objekt handelt, dem Verzeichnis selbst entspricht. Sie können auch den Enumerate-Vorgang verwenden, wenn Sie das übergeordnete Objekt eines Objekts abrufen möchten.

Wenn Sie ein Objekt auflisten, binden Sie tatsächlich an ein Objekt im Verzeichnis, und für jedes Objekt wird eine [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) zurückgegeben.

Das folgende Codebeispiel zeigt, wie die untergeordneten Elemente eines Containers aufzählt werden.


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



Sie können die Typen von Objekten filtern, die von der -Enumeration zurückgegeben werden. Um beispielsweise nur Benutzer und Gruppen anzuzeigen, verwenden Sie das folgende Codebeispiel vor der -Enumeration.


```VB
Ou.Filter = Array("user", "group")
```



Wenn Sie über einen Objektverweis verfügen, können Sie das übergeordnete Objekt des Objekts mithilfe der [**übergeordneten IADs-Eigenschaft**](/windows/desktop/api/Iads/nn-iads-iads) [](iads-property-methods.md) abrufen. Das folgende Codebeispiel zeigt, wie eine Bindung an das übergeordnete Objekt erfolgen kann.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Weitere Informationen finden Sie unter [Aufzählen von ADSI-Objekten.](enumerating-adsi-objects.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen nach Objekten](searching-for-objects.md)
</dt> </dl>

 

 




