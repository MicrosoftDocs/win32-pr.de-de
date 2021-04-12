---
title: Löschen von lokalen Gruppen
description: In diesem Thema wird gezeigt, wie Sie eine lokale Gruppe von einem Mitglieds Server oder Computer löschen, der unter Windows 2000 Professional ausgeführt wird.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Lokale Gruppen werden gelöscht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472604"
---
# <a name="deleting-local-groups"></a>Löschen von lokalen Gruppen

In diesem Thema wird gezeigt, wie Sie eine lokale Gruppe von einem Mitglieds Server oder Computer löschen, der unter Windows 2000 Professional ausgeführt wird.

**So löschen Sie eine lokale Gruppe**

1.  Binden Sie den Computer mit den folgenden Regeln:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungs Zeichen folgen Format mit dem WinNT-Anbieter, dem Computernamen und einem zusätzlichen Parameter, um ADSI anzuweisen, dass es an einen Computer gebunden ist: "Winnt:// <computer name> <computer> ". Der &lt; Parameter "Computername &gt; " ist der Name der Computergruppe, auf die zugegriffen werden soll. Dieser Parameter weist ADSI an, dass er an einen Computer gebunden wird, und ermöglicht es dem Parser des WinNT-Anbieters, einige Abfragen zur mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie gebunden sind.
    3.  Binden an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle.
2.  Geben Sie "Group" als Klasse an, indem Sie [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)zum Löschen der Gruppe verwenden.

    Sie müssen " [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) " nicht anrufen, um die Änderung im Container zu übernehmen. Der [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) -Befehl führt ein Commit für das Löschen der Gruppe direkt in das Verzeichnis aus.

 

 