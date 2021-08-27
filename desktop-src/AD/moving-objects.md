---
title: Verschieben von Objekten
description: Verschieben von Objekten
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Active Directory-Beispiele Active Directory , Verschieben von Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1158bfc3fb85712b2ab52b6b69d86c7af52675d210b75b0c9974fc2da6359ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025858"
---
# <a name="moving-objects"></a>Verschieben von Objekten

Um ein Objekt innerhalb einer Domäne zu verschieben, verwenden Sie die [**IADsContainer.MoveHere-Methode.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

**So verschieben Sie ein Objekt innerhalb einer Domäne**

1.  Binden an die [**IADs-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iads) des zu verschiebenden Objekts.
2.  Get the ADsPath of the object to move from the IADs.ADsPath property. (Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.
3.  Binden Sie an die [**IADsContainer-Schnittstelle**](/windows/desktop/api/iads/nn-iads-iadscontainer) des Containers, in den das Objekt verschoben wird.
4.  Verschieben Sie das Objekt mit der [**IADsContainer.MoveHere-Methode.**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Wenn eine Schnittstelle für das objekt vorhanden ist, das verschoben wurde, ist die Schnittstelle nach dem Objekt verschoben ungültig, da das Verzeichnisobjekt, das die Schnittstelle darstellt, nicht mehr vorhanden ist.

Weitere Informationen und ein Codebeispiel zum Verschieben eines Objekts finden Sie unter [Beispielcode zum Verschieben eines Objekts.](example-code-for-moving-an-object.md)

 

 