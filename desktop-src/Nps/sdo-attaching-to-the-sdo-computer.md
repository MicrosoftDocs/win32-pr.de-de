---
title: Anfügen an den SDO-Computer
description: Mit dem Schnittstellen Zeiger, der von cokreateinstance zurückgegeben wurde, wird die isdomachine Attach-Methode aufgerufen.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d35b9088fc1848dcf581bf69db036dce57cdd2b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948816"
---
# <a name="attaching-to-the-sdo-computer"></a>Anfügen an den SDO-Computer

Mit dem Schnittstellen Zeiger, der von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)zurückgegeben wurde, können Sie die [**isdomachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) -Methode aufrufen. Übergeben Sie **null** als Parameter an die **Attach** -Methode. Der Wert **null** gibt an, dass **Attach** das Computer Objekt dem lokalen Computer zuordnen soll. Das Anfügen an einen Remote Computer wird nicht unterstützt.

Um festzustellen, ob der lokale Computer bereits angefügt ist, müssen Sie die [**isdomachine:: getattachedcomputer**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) -Methode aufrufen.

Beispielcode, der das Anfügen an den lokalen Computer veranschaulicht, finden [Sie unter Anfügen an einen SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) .

 

 