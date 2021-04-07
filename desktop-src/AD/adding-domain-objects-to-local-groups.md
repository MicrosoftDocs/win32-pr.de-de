---
title: Hinzufügen von Domänen Objekten zu lokalen Gruppen
description: Die Benutzer und Gruppen, die der Domäne angehören, können Gruppen auf dem lokalen Computer hinzugefügt werden, um dem Domänen Benutzer oder der Gruppe auf dem jeweiligen Computer Rechte zu erteilen.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Hinzufügen von Domänen Objekten zu lokalen Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52e956d1cf076f4c33c46700e52798463b7e1d2c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724664"
---
# <a name="adding-domain-objects-to-local-groups"></a>Hinzufügen von Domänen Objekten zu lokalen Gruppen

Wenn ein Mitglieds Server oder ein Computer unter Windows 2000 Professional Mitglied einer Windows 2000-Domäne ist, können die Benutzer und Gruppen, die der Domäne angehören, Gruppen auf dem lokalen Computer hinzugefügt werden, um dem Domänen Benutzer oder der Gruppe auf dem jeweiligen Computer Rechte zu erteilen.

Beim Verwalten von lokalen Domänen Gruppen in einer Windows 2000-Domäne mithilfe von ADSI wird der LDAP-Anbieter normalerweise verwendet. Beim Verwalten lokaler Gruppen auf Mitglieds Servern und einem Computer, auf dem Windows 2000 Professional ausgeführt wird, muss jedoch der WinNT-Anbieter verwendet werden.

Auf Mitglieds Servern und Windows 2000 Professional können nur lokale Gruppen erstellt werden. Die lokalen Gruppen können jedoch Folgendes enthalten:

-   Universelle und globale Gruppen aus der Gesamtstruktur, die die Domäne enthält, der der Computer angehört.
-   Lokale Domänen Gruppen aus dieser Computer Domäne.
-   Benutzer aus einer beliebigen Domäne in der Gesamtstruktur.

**So fügen Sie einer lokalen Gruppe ein Domänen Objekt hinzu**

1.  Binden Sie an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle des Computers, der die lokale Gruppe enthält, der ein Mitglied hinzugefügt werden soll. Die Bindung muss mit einem Konto erfolgen, das über ausreichende Rechte für den Zugriff auf den Computer verfügt. Die Bindungs Zeichenfolge muss das Format "Winnt:// <computer name> , Computer" annehmen, wobei " &lt; Computername &gt; " der Name der Computergruppe ist, der ein Mitglied hinzugefügt werden soll. Der Parameter ", Computer" weist ADSI an, dass er an einen Computer gebunden wird. ADSI macht diese Daten für den Parser des WinNT-Anbieters verfügbar, sodass er einige mehrdeutigkeits Auflösungs Abfragen überspringen kann, um zu bestimmen, an welchen Objekttyp Sie gebunden sind. Dadurch kann der Benutzer eine Wartezeit von 5 bis 20 Sekunden speichern, um die Mehrdeutigkeit aufzulösen.
2.  Verwenden Sie die [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) -Methode mit "Group" als Klasse und den lokalen Gruppennamen als Namen des Objekts, das an die Gruppe gebunden werden soll.
3.  Binden Sie an die [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Schnittstelle der lokalen Gruppe, der ein Mitglied hinzugefügt wird.
4.  Erstellen Sie den ADsPath des Objekts, das der lokalen Gruppe im Format "Winnt://" hinzugefügt <domain> / <name> werden soll, wobei " &lt; Domäne &gt; " der Name der Domäne ist, die das hinzu zufügende Objekt enthält, und " &lt; Name &gt; " der Name des hinzu zufügenden Objekts ist.
5.  Fügen Sie den Benutzer oder die Gruppe der lokalen Gruppe mit der [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) -Methode hinzu, und übergeben Sie dabei den ADsPath, der in Schritt 4 erstellt wurde.

Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Domänen Benutzer-oder ein Gruppen Objekt einer lokalen Gruppe hinzugefügt wird, finden Sie unter [Beispielcode zum Hinzufügen eines Domänen Benutzers oder einer Gruppe zu einer lokalen Gruppe](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md).

 

 