---
title: Auflisten von lokalen Gruppen
description: Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, können Sie alle lokalen Gruppen auflisten.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Auflisten von lokalen Gruppen anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724553"
---
# <a name="enumerating-local-groups"></a>Auflisten von lokalen Gruppen

Auf Mitglieds Servern und Computern, die unter Windows 2000 Professional ausgeführt werden, können Sie alle lokalen Gruppen auflisten.

Auf Mitglieds Servern und Windows 2000 Professional können nur lokale Gruppen erstellt werden. Diese lokalen Gruppen können jedoch Folgendes enthalten:

-   Universelle und globale Gruppen aus der Gesamtstruktur, die die Domäne enthält, der der Computer angehört.
-   Lokale Domänen Gruppen aus der Domäne dieses Computers.
-   Benutzer aus einer beliebigen Domäne in der Gesamtstruktur.

**So zählen Sie die lokalen Gruppen auf einem Mitglieds Server oder Computer auf, auf dem Windows 2000 Professional ausgeführt wird**

1.  Binden Sie den Computer mit den folgenden Regeln:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".

        "Der <computer name> "-Parameter ist der Name der Computergruppe, auf die zugegriffen werden soll. Dieser Parameter weist ADSI an, dass er an einen Computer gebunden wird, und ermöglicht es dem Parser des WinNT-Anbieters, einige Abfragen zur mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.

    3.  Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.

2.  Legen Sie mithilfe der [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Eigenschaft einen Filter fest, der "Groups" enthält. Dies ermöglicht es Ihnen, den Container aufzuzählen und nur Gruppen abzurufen.
3.  Zählen Sie die Gruppen Objekte mithilfe der [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) -Methode auf.
4.  Verwenden Sie für jedes Group-Objekt die [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) -Schnittstelle, um den Namen und die Mitglieder der Gruppe zu lesen.

 

 