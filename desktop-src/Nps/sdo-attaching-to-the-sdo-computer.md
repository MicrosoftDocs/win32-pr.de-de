---
title: Anfügen an den SDO-Computer
description: Rufen Sie mit dem von CoCreateInstance zurückgegebenen Schnittstellenzeiger die ISdoMachine Attach-Methode auf.
ms.assetid: b28691ef-4054-4cd1-92aa-72ad9902fba3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5863302da3f213c1360c254782a31c0dfc4fcb9a946f5827155862bca01405cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362188"
---
# <a name="attaching-to-the-sdo-computer"></a>Anfügen an den SDO-Computer

Rufen Sie mit dem von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)zurückgegebenen Schnittstellenzeiger die [**ISdoMachine::Attach-Methode**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) auf. Übergeben **Sie NULL** als Parameter an die **Attach-Methode.** Der Wert **NULL gibt** an, dass **Attach** das Computerobjekt dem lokalen Computer zugibt. Das Anfügen an einen Remotecomputer wird nicht unterstützt.

Um festzustellen, ob der lokale Computer bereits angefügt ist, rufen Sie die [**ISdoMachine::GetAttachedComputer-Methode**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getattachedcomputer) auf.

[Beispielcode, der](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) das Anfügen an den lokalen Computer veranschaulicht, finden Sie unter Anfügen an einen SDO-Enabled Computer.

 

 