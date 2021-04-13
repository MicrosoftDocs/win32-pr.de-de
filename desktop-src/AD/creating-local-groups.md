---
title: Erstellen von lokalen Gruppen
description: Für Mitglieds Server und Windows 2000 Professional können nur lokale Gruppen erstellt werden.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Erstellen von lokalen Gruppen Ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314637"
---
# <a name="creating-local-groups"></a>Erstellen von lokalen Gruppen

Für Mitglieds Server und Windows 2000 Professional können nur lokale Gruppen erstellt werden.

**So erstellen Sie eine lokale Gruppe für einen Mitglieds Server oder Computer, auf dem Windows 2000 Professional ausgeführt wird**

1.  Binden Sie den Computer mit den folgenden Regeln:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ".

        Der &lt; Parameter "Computername &gt; " ist der Name der Computer Gruppen, auf die zugegriffen werden soll.

        Der Parameter "Computer" weist ADSI in der Bindungs Zeichenfolge &lt; &gt; an, dass er an einen Computer gebunden wird. ADSI stellt diese Daten dem Parser des WinNT-Anbieters zur Verfügung, sodass er einige mehrdeutigkeits Auflösungs Abfragen überspringen kann, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.

    3.  Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.

2.  Geben Sie "localgroup" als Klasse an, indem Sie [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) verwenden, um die Gruppe hinzuzufügen.
    > [!Note]  
    > Wenn Sie "Group" als Klasse angeben, wird von ADSI "localgroup" verwendet. Geben Sie die Klasse nicht als "globalgroup" an. Gruppen der Klasse "globalgroup" können nicht auf Mitglieds Servern oder einem Computer erstellt werden, auf dem Windows NT Workstation/Windows 2000 Professional ausgeführt wird. Wenn Sie "globalgroup" angeben, erstellt [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) die Gruppe im Eigenschaften Cache, [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) schreibt die Gruppe jedoch nicht in die Sicherheitsdatenbank und gibt keinen Fehler zurück.

     

3.  Schreiben Sie die Gruppe mithilfe von " [**IADs. * tinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)" in die Computer Sicherheitsdatenbank.

 

 