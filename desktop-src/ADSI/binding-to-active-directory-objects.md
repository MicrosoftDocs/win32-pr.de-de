---
title: Binden an Active Directory Objekte
description: Bevor Sie mit diesem Szenario fortfahren, müssen Sie verstehen, wie ADSI-Objekte in Active Directory benannt werden und wie diese gebunden werden. Beim Binden eines ADSI-Objekts wird das Objekt mit dem Verzeichnisdienst verbunden, und Sie können auf die Methoden des Objekts zugreifen.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036321"
---
# <a name="binding-to-active-directory-objects"></a>Binden an Active Directory Objekte

Bevor Sie mit diesem Szenario fortfahren, müssen Sie verstehen, wie ADSI-Objekte in Active Directory benannt werden und wie diese gebunden werden. Beim Binden eines ADSI-Objekts wird das Objekt mit dem Verzeichnisdienst verbunden, und Sie können auf die Methoden des Objekts zugreifen.

## <a name="adspath"></a>ADsPath

Ein ADSI-Objekt wird durch die Bindungs Zeichenfolge, die auch als ADsPath bezeichnet wird, eindeutig identifiziert. Ein ADsPath ist eine Kombination aus einem programmatischen Bezeichner (ProgID) des ADSI-Anbieters und dem DN (Distinguished Name) des Objekts.

Dies ist das Format eines ADsPath:

"ProgID://DN"

-   pogid – der programmatische Bezeichner des ADSI-Anbieters, z. b. LDAP oder Winnt.

-   ://– trennt die ProgID vom DN.

-   DN – der Distinguished Name des ADSI-Objekts, bei dem es sich um den vollständigen Pfad des Objekts handelt, bei dem der Pfad aus den relativen Distinguished Names (rDNS) besteht.

Ein RDN ist der Name des Objekts ohne den Pfad und ist von seinen gleich geordneten Objekten eindeutig. Ein RDN besteht aus einer Attribut-ID und einem Wert, z. b. "DC = Fabrikam", wobei Domänen Controller das Attribut ist und Fabrikam der Wert ist. DC ist eine RDN-Attribut-ID, die für die Domänen Komponente steht.

Im folgenden finden Sie ein Beispiel für einen ADsPath:

"LDAP://DC = fabrikam, DC = com"

## <a name="binding-the-object"></a>Binden des Objekts

Im folgenden wird erläutert, wie Sie das Domänen Objekt in diesem Szenario binden können:


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



Wenn Sie dieses Codebeispiel ausführen, verwendet ADSI den DN, um die zu bindenden ADSI-Objekte zu bestimmen. Nachdem ADSI diese Objekte gebunden hat, können Sie auf die zugehörigen Methoden zugreifen. Im vorherigen Codebeispiel wird ein Domänen Objekt an [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) und [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)gebunden. Sie können jetzt Methoden für diese Schnittstellen verwenden, z. b. [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)und [**muvehere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).

Nachdem Sie ein Domänen Objekt gebunden haben, können Sie einige seiner Attribute ausdrucken:


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



Weitere Informationen zu ADsPath finden Sie unter [Bindungs Zeichenfolge](binding-string.md). Weitere Informationen zur Bindung finden Sie unter [binden an ein ADSI-Objekt](binding-to-an-adsi-object.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer Organisationseinheit](creating-an-organizational-unit.md)
</dt> </dl>

 

 




