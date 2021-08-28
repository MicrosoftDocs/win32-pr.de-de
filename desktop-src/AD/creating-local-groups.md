---
title: Erstellen von lokalen Gruppen
description: Es können nur lokale Gruppen für Mitgliedsserver und Windows 2000-Professional.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Erstellen von lokalen Gruppen (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06410572e6e5897280b2a03c99b387dbf81b3cca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881583"
---
# <a name="creating-local-groups"></a>Erstellen von lokalen Gruppen

Es können nur lokale Gruppen für Mitgliedsserver und Windows 2000-Professional.

**So erstellen Sie eine lokale Gruppe für einen Mitgliedsserver oder Computer mit Windows 2000 Professional**

1.  Binden Sie mithilfe der folgenden Regeln an den Computer:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungszeichenfolgenformat unter Verwendung des WinNT-Anbieters, des Computernamens und eines zusätzlichen Parameters, um ADSI anweisen zu können, dass es an einen Computer WinNT:// ist: "WinNT:// <computer name> , &lt; computer &gt; ".

        Der Parameter &lt; "Computername" &gt; ist der Name der Computergruppen, auf die sie zugreifen möchten.

        In der Bindungszeichenfolge weist der Parameter " computer " ADSI an, &lt; dass es an einen Computer binden &gt; soll. ADSI stellt diese Daten für den Parser des WinNT-Anbieters zur Verfügung, sodass einige Abfragen zur Mehrdeutigkeitsauflösung übersprungen werden können, um zu bestimmen, an welchen Objekttyp Sie binden.

    3.  Binden sie an die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadscontainer)

2.  Geben Sie "localGroup" als Klasse an, indem [**Sie IADsContainer.Create verwenden,**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) um die Gruppe hinzuzufügen.
    > [!Note]  
    > Wenn Sie "group" als Klasse angeben, verwendet ADSI "localGroup". Geben Sie die Klasse nicht als "globalGroup" an. Gruppen der Klasse "globalGroup" können nicht auf Mitgliedsservern oder einem Computer erstellt werden, auf dem Windows NT Workstation/Windows 2000 Professional. Wenn Sie "globalGroup" angeben, erstellt [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) die Gruppe im Eigenschaftencache, [**aber IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) schreibt die Gruppe nicht in die Sicherheitsdatenbank und gibt keinen Fehler zurück.

     

3.  Schreiben Sie die Gruppe mit [**IADs.SetInfo in die Computersicherheitsdatenbank.**](/windows/desktop/api/iads/nf-iads-iads-setinfo)

 

 
