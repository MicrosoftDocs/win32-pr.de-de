---
title: Auflisten von Benutzern
description: Anders als Windows NT 4,0-Domänen können Windows 2000-Benutzer in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Auflisten von Benutzern anzeigen
- Benutzer AD, Auflisten eines Benutzers
- Active Directory, verwenden von Benutzern, Auflisten eines Benutzers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e922d92f4313ed0238ff068f7ae1c0fbf693d497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106340695"
---
# <a name="enumerating-users"></a>Auflisten von Benutzern

Anders als Windows NT 4,0-Domänen können Windows 2000-Benutzer in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden. Dies bedeutet, dass sich Benutzer an zahlreichen Orten in der Verzeichnishierarchie befinden können. Daher haben Sie zwei Möglichkeiten zum Auflisten von Benutzern:

-   Listet die Benutzer auf, die direkt in einem Container, in einer Organisationseinheit oder im Stammverzeichnis der Domäne enthalten sind:

    Binden Sie explizit an das Container Objekt, das die Benutzer enthält, die Sie aufzählen möchten, legen Sie mithilfe der [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) -Eigenschaft einen Filter mit "User" als Klasse fest, und verwenden Sie die [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) -Methode, um die Benutzer Objekte aufzuzählen.

    Dieses Verfahren kann zum Auflisten von Benutzern verwendet werden, die direkt in einem Container-oder OU-Objekt enthalten sind. Wenn der Container andere Container enthält, die potenziell andere Benutzer enthalten können, müssen Sie eine Bindung an diese Container durchlaufen und die Benutzer in diesen Containern rekursiv auflisten. Wenn es nicht erforderlich ist, dass Sie die Benutzer Objekte bearbeiten und nur bestimmte Eigenschaften lesen müssen, verwenden Sie die in Option 2 beschriebene Deep-Suche.

    Da die Enumeration Zeiger auf ADSI COM-Objekte zurückgibt, die die einzelnen Benutzer Objekte darstellen, können Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zum Abrufen von [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)und [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) -Schnittstellen Zeigern auf das User-Objekt abrufen. Dies bedeutet, dass Sie Schnittstellen Zeiger auf jedes enumerationsbenutzerobjekt in einem Container erhalten können, ohne explizit eine Bindung an jedes Benutzerobjekt durchführen zu müssen. Zum Ausführen von Vorgängen für alle Benutzer, die sich direkt in einem Container befinden, vermeidet die Enumeration die Bindung an jeden Benutzer, um **IADs** oder **IADsUser** -Methoden aufrufen zu können. Um bestimmte Eigenschaften von Benutzern abzurufen, verwenden Sie [**idirectoriysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) , wie in Option 2 beschrieben.

-   Führen Sie eine Tiefe Suche nach (& (objectClass = User) (objectCategory = Person)) aus, um alle Benutzer in einer Struktur zu finden:

    Binden Sie zunächst an das Container Objekt, in dem die Suche beginnen soll. Wenn Sie z. b. alle Benutzer in einer Domäne suchen möchten, binden Sie die Bindung an den Stamm der Domäne ein. um alle Benutzer in der Gesamtstruktur zu suchen, binden Sie an den globalen Katalog, und suchen Sie aus dem Stammverzeichnis der GC.

    Verwenden Sie dann [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) zum Abfragen mithilfe eines Suchfilters, der (& (objectClass = User) (objectCategory = Person)) und der Such Einstellung der \_ Unterstruktur des ADS-Bereichs enthält \_ .

    Sie können eine Suche mit einer Such Einstellung von ADS \_ Scope \_ onelevel durchführen, um die Suche auf den direkten Inhalt des Container Objekts zu beschränken, an das Sie gebunden sind.

    [**Idirector ysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ruft nur die Werte spezifischer Eigenschaften von Benutzern ab. Um Werte abzurufen, verwenden Sie **idirector ysearch**. Um die von einer Suche zurückgegebenen Benutzer Objekte zu bearbeiten, d. h., Sie möchten [**IADs**](/windows/desktop/api/iads/nn-iads-iads) oder [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) -Methoden verwenden, müssen Sie Sie explizit binden. Geben Sie zu diesem Zweck "Distinguished **shedname** " als eine der Eigenschaften an, die von der Suche zurückgegeben werden sollen, und verwenden Sie die zurückgegebenen Distinguished Names zum Binden an jeden Benutzer, der in der Suche zurückgegeben

    Es werden nur bestimmte Eigenschaften abgerufen. Sie können nicht alle Attribute abrufen, ohne explizit alle möglichen Attribute der Benutzerklasse anzugeben.

 

 