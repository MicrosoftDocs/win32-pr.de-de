---
title: Aufzählen von Gruppen in einer Domäne
description: Gruppen können in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne sowie im Stamm der Domäne platziert werden.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Aufzählen von Gruppen in einem Domänen-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3723122ef2ab70a7396b2b2821c96a20b4d92419c1e10d1c00b11ff903cb6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429846"
---
# <a name="enumerating-groups-in-a-domain"></a>Aufzählen von Gruppen in einer Domäne

Gruppen können in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne sowie im Stamm der Domäne platziert werden. Dies bedeutet, dass Sich Gruppen an zahlreichen Speicherorten in der Verzeichnishierarchie befinden können. Daher haben Sie zwei Möglichkeiten zum Aufzählen von Gruppen:

1.  Aufzählen der Gruppen, die direkt in einem Container, einer Organisationseinheit oder im Stamm der Domäne enthalten sind.

    Binden Sie explizit an das Containerobjekt, das die aufzuzählenden Gruppen enthält, legen Sie mithilfe der [**IADsContainer.Filter-Eigenschaft**](/windows/desktop/api/iads/nn-iads-iadscontainer) einen Filter fest, der "groups" als Klasse enthält, und verwenden Sie die [**IADsContainer::get \_ \_ NewEnum-Methode,**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) um die Gruppenobjekte aufzuzählen.

    Dieses Verfahren listet Gruppen auf, die direkt in einem Container oder OU-Objekt enthalten sind. Wenn der Container andere Container enthält, die möglicherweise andere Gruppen enthalten können, müssen Sie eine Bindung an diese Container erstellen und die Gruppen in diesen Containern rekursiv aufzählen. Verwenden Sie die in Option 2 beschriebene umfassende Suche, um die Gruppenobjekte zu bearbeiten und nur bestimmte Eigenschaften zu lesen.

    Da enumeration Zeiger auf ADSI-COM-Objekte zurückgibt, die jedes Gruppenobjekt darstellen, können Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufrufen, um [**IADs-**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup-**](/windows/desktop/api/iads/nn-iads-iadsgroup)und [**IADsPropertyList-Schnittstellenzeiger**](/windows/desktop/api/iads/nn-iads-iadspropertylist) auf das Gruppenobjekt abzurufen. Das heißt, Sie können Schnittstellenzeiger auf jedes aufzählte Gruppenobjekt in einem Container abrufen, ohne explizit an jedes Gruppenobjekt binden zu müssen. Zum Ausführen von Vorgängen für alle Gruppen direkt in einem Container ist für die Enumeration keine Bindung an jede Gruppe erforderlich, um **IADs** oder **IADsGroup-Methoden** aufzurufen. Um bestimmte Eigenschaften aus Gruppen abzurufen, verwenden [**Sie IDirectorySearch,**](/windows/desktop/api/iads/nn-iads-idirectorysearch) wie in der zweiten Option beschrieben.

    Eine Ausnahme tritt auf, wenn Sie versuchen, eine Gruppe aufzuzählen, die Mitglieder enthält, die bekannte Sicherheitsprinzipale sind, z. B. Jeder, Authentifizierte Benutzer, BATCH usw. Da sie nicht an diese Objekttypen gebunden werden können, werden sie nicht aufgelistet, wenn Sie Gruppen im WinNT-Bereich aufzählen, obwohl dies möglicherweise zu binden scheint, da bestimmte IADs-Methoden wie Class, ADsPath und Name beim Aufrufen von aufgezählten Membern die richtigen Ergebnisse zurückgeben.

2.  Führen Sie eine umfassende Suche nach "objectCategory=group" durch, um alle Gruppen in einer Struktur zu finden.

    Binden Sie zunächst an das Containerobjekt, an dem mit der Suche begonnen werden soll. Um beispielsweise alle Gruppen in einer Domäne zu finden, binden Sie an den Stamm der Domäne. Um alle Gruppen in der Gesamtstruktur zu suchen, binden Sie an den globalen Katalog, und suchen Sie im Stammverzeichnis der GC.

    Verwenden Sie dann [**IDirectorySearch,**](/windows/desktop/api/iads/nn-iads-idirectorysearch) um abfragen, indem Sie einen Suchfilter verwenden, der (objectCategory=group) und die Suchpräferenz von **ADS SCOPE \_ \_ SUBTREE** enthält.

    > [!Note]  
    > Sie können eine Suche mit der Sucheinstellung **ADS \_ SCOPE \_ ONELEVEL** ausführen, um die Suche auf den direkten Inhalt des Containerobjekts zu beschränken, an das Sie gebunden sind.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ruft nur die Werte bestimmter Eigenschaften aus Gruppen ab. Verwenden Sie **IDirectorySearch,** um Werte abzurufen. Um die von einer Suche zurückgegebenen Gruppenobjekte zu bearbeiten, d. h. [**IADs**](/windows/desktop/api/iads/nn-iads-iads) oder [**IADsGroup-Methoden**](/windows/desktop/api/iads/nn-iads-iadsgroup) zu verwenden, binden Sie explizit an sie. Geben Sie hierzu **distinguishedName** als eine der Eigenschaften an, die von der Suche zurückgegeben werden sollen, und verwenden Sie die zurückgegebenen Distinguished Names, um eine Bindung an jede in der Suche zurückgegebene Gruppe zu verwenden.

    Es werden nur bestimmte Eigenschaften abgerufen. Sie können nicht alle Attribute abrufen, ohne jedes mögliche Attribut der Gruppenklasse explizit anzugeben.

 

 