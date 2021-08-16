---
title: Aufzählen von lokalen Gruppen
description: Auf Mitgliedsservern und Computern, die Windows 2000 Professional, können Sie alle lokalen Gruppen aufzählen.
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- Aufzählen von lokalen Gruppen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f1584cf8650b3fa341e7a314e0b6f94120b28c50226f16230c53206d6e14b80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191330"
---
# <a name="enumerating-local-groups"></a>Aufzählen von lokalen Gruppen

Auf Mitgliedsservern und Computern, die Windows 2000 Professional, können Sie alle lokalen Gruppen aufzählen.

Nur lokale Gruppen können auf Mitgliedsservern erstellt werden, und Windows 2000 Professional. Diese lokalen Gruppen können jedoch Folgendes enthalten:

-   Universelle und globale Gruppen aus der Gesamtstruktur, die die Domäne enthält, der der Computer mitglied ist.
-   Lokale Domänengruppen aus der Domäne dieses Computers.
-   Benutzer aus einer beliebigen Domäne in der Gesamtstruktur.

**So enumerieren Sie die lokalen Gruppen auf einem Mitgliedsserver oder Computer mit Windows 2000 Professional**

1.  Binden Sie mithilfe der folgenden Regeln an den Computer:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungszeichenfolgenformat unter Verwendung des WinNT-Anbieters, des Computernamens und eines zusätzlichen Parameters, um ADSI anweisen zu können, dass es an einen Computer <computer name> <computer> WinNT://, ".

        Der <computer name> Parameter "" ist der Name der Computergruppe, auf die sie zugreifen soll. Dieser Parameter weist ADSI an, an einen Computer zu binden, und ermöglicht es dem Parser des WinNT-Anbieters, einige Abfragen zur Mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie binden.

    3.  Binden sie an die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Legen Sie mithilfe der [**IADsContainer.Filter-Eigenschaft**](/windows/desktop/api/iads/nn-iads-iadscontainer) einen Filter fest, der "Gruppen" enthält. Dadurch können Sie den Container aufzählen und nur Gruppen abrufen.
3.  Aufzählen der Gruppenobjekte mithilfe der [**IADsContainer::get \_ \_ NewEnum-Methode.**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)
4.  Verwenden Sie für jedes Gruppenobjekt die [**IADsGroup-Schnittstelle,**](/windows/desktop/api/iads/nn-iads-iadsgroup) um den Namen und die Mitglieder der Gruppe zu lesen.

 

 