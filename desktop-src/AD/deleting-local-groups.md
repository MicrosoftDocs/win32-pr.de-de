---
title: Löschen von lokalen Gruppen
description: In diesem Thema wird gezeigt, wie Sie eine lokale Gruppe von einem Mitgliedsserver oder Computer löschen, der auf Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Löschen von lokalen Gruppen (AD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe960804e083ecaf8ef12e412a43b7b8db4800f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881481"
---
# <a name="deleting-local-groups"></a>Löschen von lokalen Gruppen

In diesem Thema wird gezeigt, wie Sie eine lokale Gruppe von einem Mitgliedsserver oder Computer löschen, der auf Windows 2000 Professional.

**So löschen Sie eine lokale Gruppe**

1.  Binden Sie mithilfe der folgenden Regeln an den Computer:
    1.  Verwenden Sie ein Konto mit ausreichenden Rechten für den Zugriff auf diesen Computer.
    2.  Verwenden Sie das folgende Bindungszeichenfolgenformat unter Verwendung des WinNT-Anbieters, des Computernamens und eines zusätzlichen Parameters, um ADSI anweisen zu können, dass es an einen Computer WinNT:// ist: "WinNT:// <computer name> , &lt; computer &gt; ". Der Parameter &lt; "Computername" &gt; ist der Name der Computergruppe, auf die sie zugreifen soll. Dieser Parameter weist ADSI an, an einen Computer zu binden, und ermöglicht es dem Parser des WinNT-Anbieters, einige Abfragen zur Mehrdeutigkeitsauflösung zu überspringen, um zu bestimmen, an welchen Objekttyp Sie binden.
    3.  Binden sie an die [**IADsContainer-Schnittstelle.**](/windows/desktop/api/iads/nn-iads-iadscontainer)
2.  Geben Sie "group" als Klasse an, indem [**Sie IADsContainer.Delete verwenden,**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)um die Gruppe zu löschen.

    Sie müssen [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) nicht aufrufen, um die Änderung an den Container zu commiten. Der [**IADsContainer.Delete-Aufruf**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) committ das Löschen der Gruppe direkt im Verzeichnis.

 

 
