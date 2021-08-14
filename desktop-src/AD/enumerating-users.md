---
title: Aufzählen von Benutzern
description: Im Gegensatz zu Windows NT 4.0-Domänen können Windows 2.000 Benutzer in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne sowie im Stamm der Domäne platziert werden.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Aufzählen von Benutzer-AD
- users AD , enumerating a user
- Active Directory, using,users, enumerating a user
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa43034c6c006c9c70531f25e2a838ecfc30520e9b42e0b9599e5714a29f225e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191340"
---
# <a name="enumerating-users"></a>Aufzählen von Benutzern

Im Gegensatz zu Windows NT 4.0-Domänen können Windows 2.000 Benutzer in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne sowie im Stamm der Domäne platziert werden. Dies bedeutet, dass sich Benutzer an zahlreichen Speicherorten in der Verzeichnishierarchie befinden können. Daher haben Sie zwei Möglichkeiten zum Aufzählen von Benutzern:

-   Aufzählen der Benutzer, die direkt in einem Container, einer Organisationseinheit oder im Stammverzeichnis der Domäne enthalten sind:

    Binden Sie explizit an das Containerobjekt, das die Benutzer enthält, die Sie aufzählen möchten, legen Sie mithilfe der [**IADsContainer.Filter-Eigenschaft**](/windows/desktop/ADSI/iadscontainer-property-methods) einen Filter mit "user" als Klasse fest, und verwenden Sie die [**IADsContainer::get \_ \_ NewEnum-Methode,**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) um die Benutzerobjekte aufzuzählen.

    Diese Technik kann verwendet werden, um Benutzer aufzuzählen, die direkt in einem Container oder ou-Objekt enthalten sind. Wenn der Container andere Container enthält, die möglicherweise andere Benutzer enthalten können, müssen Sie eine Bindung an diese Container erstellen und die Benutzer in diesen Containern rekursiv aufzählen. Wenn Sie die Benutzerobjekte nicht bearbeiten müssen und nur bestimmte Eigenschaften lesen müssen, verwenden Sie die in Option 2 beschriebene umfassende Suche.

    Da enumeration Zeiger auf ADSI-COM-Objekte zurückgibt, die jedes Benutzerobjekt darstellen, können Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufrufen, um [**IADs-,**](/windows/desktop/api/iads/nn-iads-iads) [**IADsUser-**](/windows/desktop/api/iads/nn-iads-iadsuser)und [**IADsPropertyList-Schnittstellenzeiger**](/windows/desktop/api/iads/nn-iads-iadspropertylist) auf das Benutzerobjekt abzurufen. Dies bedeutet, dass Sie Schnittstellenzeiger auf jedes aufzählte Benutzerobjekt in einem Container abrufen können, ohne explizit an jedes Benutzerobjekt binden zu müssen. Um Vorgänge für alle Benutzer direkt innerhalb eines Containers auszuführen, vermeidet die Enumeration die Bindung an jeden Benutzer, um **IADs** oder **IADsUser-Methoden** aufzurufen. Verwenden Sie [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) wie in Option 2 beschrieben, um bestimmte Eigenschaften von Benutzern abzurufen.

-   Führen Sie eine umfassende Suche nach (&(objectClass=user)(objectCategory=person)) durch, um alle Benutzer in einer Struktur zu finden:

    Binden Sie zunächst an das Containerobjekt, an dem mit der Suche begonnen werden soll. Um beispielsweise alle Benutzer in einer Domäne zu finden, binden Sie an den Stamm der Domäne. Um alle Benutzer in der Gesamtstruktur zu finden, binden Sie an den globalen Katalog, und suchen Sie im Stammverzeichnis der GC.

    Verwenden Sie anschließend [**IDirectorySearch,**](/windows/desktop/api/iads/nn-iads-idirectorysearch) um abfragen, indem Sie einen Suchfilter verwenden, der (&(objectClass=user)(objectCategory=person)) und die Sucheinstellung ADS \_ SCOPE \_ SUBTREE enthält.

    Sie können eine Suche mit der Sucheinstellung ADS \_ SCOPE \_ ONELEVEL ausführen, um die Suche auf den direkten Inhalt des Containerobjekts zu beschränken, an das Sie gebunden sind.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ruft nur die Werte bestimmter Eigenschaften von Benutzern ab. Verwenden Sie **IDirectorySearch,** um Werte abzurufen. Um die von einer Suche zurückgegebenen Benutzerobjekte zu bearbeiten, d. h., Sie möchten [**IADs**](/windows/desktop/api/iads/nn-iads-iads) oder [**IADsUser-Methoden**](/windows/desktop/api/iads/nn-iads-iadsuser) verwenden, müssen Sie explizit an sie binden. Geben Sie hierzu **distinguishedName** als eine der Eigenschaften an, die von der Suche zurückgegeben werden sollen, und verwenden Sie die zurückgegebenen Distinguished Names, um eine Bindung an jeden Benutzer zu erhalten, der in der Suche zurückgegeben wird.

    Es werden nur bestimmte Eigenschaften abgerufen. Sie können nicht alle Attribute abrufen, ohne jedes mögliche Attribut der Benutzerklasse explizit anzugeben.

 

 