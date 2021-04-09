---
title: Verschieben von Objekten
description: Verschieben von Objekten
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Verschieben von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038747"
---
# <a name="moving-objects"></a>Verschieben von Objekten

Verwenden Sie die [**IADsContainer. movehere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) -Methode, um ein Objekt innerhalb einer Domäne zu verschieben.

**So verschieben Sie ein Objekt innerhalb einer Domäne**

1.  Binden an die [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle des zu verschiebenden Objekts.
2.  Ruft den ADsPath des Objekts ab, das aus der [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) -Eigenschaft verschoben werden soll.
3.  Binden Sie an die [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Schnittstelle des Containers, in den das Objekt verschoben wird.
4.  Verschieben Sie das Objekt mit der [**IADsContainer. movehere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) -Methode.

Wenn eine Schnittstelle für das Objekt vorhanden ist, das verschoben wurde, ist die Schnittstelle nach dem Verschieben des Objekts ungültig, da das Verzeichnis Objekt, das die Schnittstelle darstellt, nicht mehr vorhanden ist.

Weitere Informationen und ein Codebeispiel, das zeigt, wie ein Objekt verschoben wird, finden Sie unter [Beispielcode zum Verschieben eines Objekts](example-code-for-moving-an-object.md).

 

 