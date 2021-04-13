---
title: Anzeigen von Containern als Blattknoten
description: Jedes Objekt in Active Directory Domain Services kann ein Container anderer Objekte sein.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Anzeigen von Containern als Blattknoten
- Container AD, anzeigen als Blattknoten
- Blatt Anzeige, Anzeigen von Containern als Blattknoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314600"
---
# <a name="viewing-containers-as-leaf-nodes"></a>Anzeigen von Containern als Blattknoten

Jedes Objekt in Active Directory Domain Services kann ein Container anderer Objekte sein. Dadurch kann die Benutzeroberfläche überladen werden. Daher ist es möglich, zu deklarieren, dass ein Objekt einer bestimmten Klasse nur als Blatt in der Benutzeroberfläche angezeigt wird. Das **treatAsLeaf** -Attribut ist ein einwertiges Anzeige spezifiziererattribut, das bestimmt, ob Objekte dieser Klasse nur als Blattobjekte angezeigt werden sollen. Dieses Attribut ist ein boolescher Wert, der angibt, dass Objekte der Klasse nur als Blatt Elemente angezeigt werden sollen, wenn der Wert **true** ist. Wenn der Wert **false** ist, wird angegeben, dass Objekte der Klasse als Container oder als Blatt angezeigt werden können. Wie bei allen bezeichnerspezifiziererattributen wird das **treatAsLeaf** -Attribut pro Gebiets Schema festgelegt, sodass dieses Attribut nach Bedarf lokalisiert werden kann. Beispielsweise ist für die **Benutzer Anzeige** für das englische Gebiets Schema (0409) der Anzeige Spezifizierer das Attribut " **treatAsLeaf** " standardmäßig auf " **true** " festgelegt. Dies bewirkt, dass die Benutzeroberfläche alle **Benutzer** Objekte als Blattobjekte anzeigt.

**So legen Sie den Wert des **treatAsLeaf** -Attributs fest**

1.  Binden Sie an das gewünschte Anzeige Attribut im gewünschten Gebiets Schema. Weitere Informationen und ein Codebeispiel finden Sie unter [displayspecifieres Container](displayspecifiers-container.md).
2.  Verwenden Sie die [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) -Methode, um das **treatAsLeaf** -Attribut auf " **true** " oder " **false**" festzulegen.
3.  Um die Änderungen im Verzeichnis zu übertragen, müssen Sie die [**IADs:: abtinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) -Methode abrufen.

 

 