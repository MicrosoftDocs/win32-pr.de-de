---
title: Auflisten von Gruppen in einer Domäne
description: Gruppen können in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Auflisten von Gruppen in einer Domänen-AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3586b8c6d261c769cabe56def2aa9396a58fa3a5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724561"
---
# <a name="enumerating-groups-in-a-domain"></a>Auflisten von Gruppen in einer Domäne

Gruppen können in einem beliebigen Container oder einer Organisationseinheit (OE) in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden. Dies bedeutet, dass sich Gruppen an verschiedenen Speicherorten in der Verzeichnishierarchie befinden können. Daher haben Sie zwei Möglichkeiten zum Auflisten von Gruppen:

1.  Listet die Gruppen auf, die direkt in einem Container, in einer Organisationseinheit oder im Stammverzeichnis der Domäne enthalten sind.

    Binden Sie explizit an das Container Objekt, das die aufzuzählenden Gruppen enthält, legen Sie mithilfe der [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Eigenschaft einen Filter fest, der "Groups" als Klasse enthält, und verwenden Sie die [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) -Methode, um die Gruppen Objekte aufzuzählen.

    Diese Technik listet Gruppen auf, die direkt in einem Container-oder OU-Objekt enthalten sind. Wenn der Container andere Container enthält, die potenziell andere Gruppen enthalten können, müssen Sie eine Bindung an diese Container durchlaufen und die Gruppen für diese Container rekursiv aufzählen. Wenn Sie die Gruppen Objekte und schreibgeschützte Eigenschaften bearbeiten möchten, verwenden Sie die in Option 2 beschriebene Tiefe Suche.

    Da die Enumeration Zeiger auf ADSI COM-Objekte zurückgibt, die die einzelnen Gruppen Objekte darstellen, können Sie [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) zum Abrufen von [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)und [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) -Schnittstellen Zeigern auf das Group-Objekt abrufen. Das heißt, Sie können Schnittstellen Zeiger auf jedes enumerierte Gruppen Objekt in einem Container aufrufen, ohne explizit eine Bindung an jedes Group-Objekt durchführen zu müssen. Zum Ausführen von Vorgängen für alle Gruppen direkt innerhalb eines Containers erfordert die Enumeration keine Bindung an jede Gruppe, um **IADs** oder **IADsGroup** -Methoden aufzurufen. Um bestimmte Eigenschaften aus Gruppen abzurufen, verwenden Sie [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) , wie in der zweiten Option beschrieben.

    Eine Ausnahme hiervon tritt auf, wenn Sie versuchen, eine Gruppe aufzulisten, die Mitglieder mit bekannten Sicherheits Prinzipalen ist, z. b. "alle", "authentifizierte Benutzer", "Batch" usw. Da Sie keine Bindung an diese Objekttypen haben, werden Sie nicht aufgelistet, wenn Sie Gruppen im WinNT-Bereich auflisten, auch wenn Sie möglicherweise gebunden werden, da bestimmte IADs-Methoden wie Class, ADsPath und Name beim Aufruf für Enumerationsmember korrekte Ergebnisse zurückgeben.

2.  Führen Sie eine Tiefe Suche nach "objectCategory = Group" durch, um alle Gruppen in einer Struktur zu finden.

    Binden Sie zunächst an das Container Objekt, in dem die Suche beginnen soll. Um z. b. alle Gruppen in einer Domäne zu suchen, binden Sie an den Stamm der Domäne. Wenn Sie alle Gruppen in der Gesamtstruktur suchen möchten, binden Sie Sie an den globalen Katalog, und suchen Sie aus dem Stammverzeichnis der GC.

    Verwenden Sie dann [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) , um mithilfe eines Suchfilters, der (objectCategory = Group) enthält, und der Such Einstellung der **ADS- \_ Bereichs \_ Teilstruktur** eine Abfrage durchführen.

    > [!Note]  
    > Sie können eine Suche mit einer Such Einstellung von **ADS \_ Scope \_ onelevel** durchführen, um die Suche auf den direkten Inhalt des Container Objekts zu beschränken, an das Sie gebunden sind.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) ruft nur die Werte spezifischer Eigenschaften aus Gruppen ab. Um Werte abzurufen, verwenden Sie **idirector ysearch**. Um die von einer Suche zurückgegebenen Gruppen Objekte zu bearbeiten, d. h., um [**IADs**](/windows/desktop/api/iads/nn-iads-iads) oder [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Methoden zu verwenden, binden Sie explizit an Sie. Geben Sie zu diesem Zweck "Distinguished **shedname** " als eine der Eigenschaften an, die von der Suche zurückgegeben werden sollen, und verwenden Sie die zurückgegebenen Distinguished Names zum Binden an jede in der Suche zurückgegebene Gruppe.

    Es werden nur bestimmte Eigenschaften abgerufen. Sie können nicht alle Attribute abrufen, ohne explizit alle möglichen Attribute der Group-Klasse anzugeben.

 

 