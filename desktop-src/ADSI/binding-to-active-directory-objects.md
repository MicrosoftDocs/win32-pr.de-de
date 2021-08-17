---
title: Binden an Active Directory-Objekte
description: Bevor Sie mit diesem Szenario fortfahren, müssen Sie verstehen, wie ADSI-Objekte in Active Directory benannt werden und wie sie gebunden werden. Durch das Binden eines ADSI-Objekts wird das Objekt mit dem Verzeichnisdienst verbunden, und Sie können auf die Methoden des Objekts zugreifen.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b473c9e3370c3d1739fc904b8c6409d756f62b5c358db200c3de821f55349f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962259"
---
# <a name="binding-to-active-directory-objects"></a>Binden an Active Directory-Objekte

Bevor Sie mit diesem Szenario fortfahren, müssen Sie verstehen, wie ADSI-Objekte in Active Directory benannt werden und wie sie gebunden werden. Durch das Binden eines ADSI-Objekts wird das Objekt mit dem Verzeichnisdienst verbunden, und Sie können auf die Methoden des Objekts zugreifen.

## <a name="adspath"></a>ADsPath

Ein ADSI-Objekt wird durch seine Bindungszeichenfolge eindeutig identifiziert, die auch als ADsPath bezeichnet wird. Ein ADsPath ist eine Kombination aus einem programmgesteuerten Bezeichner (progID) des ADSI-Anbieters und dem Distinguished Name (DN) des Objekts.

Dies ist das Format eines ADsPath:

"progID://DN"

-   pogID: Der programmgesteuerte Bezeichner des ADSI-Anbieters, z. B. LDAP oder WinNT.

-   :// – trennt die ProgID vom DN.

-   DN: Der Distinguished Name des ADSI-Objekts, der der vollständige Pfad des Objekts ist, wobei der Pfad aus relativen Distinguished Names (RDNs) besteht.

Ein RDN ist der Name des Objekts ohne den Pfad und ist von seinen gleichgeordneten Objekten eindeutig. Ein RDN besteht aus einer Attribut-ID und einem Wert, z. B. "DC=Fabrikam", wobei DC das Attribut und Fabrikam der Wert ist. DC ist eine RDN-Attribut-ID, die für Domänenkomponente steht.

Hier sehen Sie ein Beispiel für einen ADsPath:

"LDAP://DC=Fabrikam,DC=Com"

## <a name="binding-the-object"></a>Binden des Objekts

So können Sie das Domänenobjekt in diesem Szenario binden:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Wenn Sie dieses Codebeispiel ausführen, verwendet ADSI den DN, um die zu bindende ADSI-Objekte zu bestimmen. Nachdem ADSI diese Objekte gebunden hat, können Sie auf ihre Methoden zugreifen. Im vorherigen Codebeispiel wird ein Domänenobjekt an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)gebunden. Sie können jetzt Methoden für diese Schnittstellen verwenden, z. [**B. Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)und [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

Nachdem Sie ein Domänenobjekt gebunden haben, können Sie einige seiner Attribute drucken:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Weitere Informationen zu ADsPath finden Sie unter [Bindungszeichenfolge.](binding-string.md) Weitere Informationen zur Bindung finden Sie unter [Binden an ein ADSI-Objekt.](binding-to-an-adsi-object.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Organisationseinheit](creating-an-organizational-unit.md)
</dt> </dl>

 

 




