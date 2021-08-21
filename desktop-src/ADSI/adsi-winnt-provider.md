---
title: ADSI WinNT-Anbieter
description: Der Microsoft ADSI-Anbieter implementiert eine Reihe von ADSI-Objekten zur Unterstützung verschiedener ADSI-Schnittstellen.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- adsi winnt provider ADSI
- WinNT-Dienstanbieter ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eb0984b150355099e1609481432f01d9b00be110b64bb82d08a938c02acb7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692790"
---
# <a name="adsi-winnt-provider"></a>ADSI WinNT-Anbieter

Der Microsoft ADSI-Anbieter implementiert eine Reihe von ADSI-Objekten zur Unterstützung verschiedener ADSI-Schnittstellen. Der Namespacename für den Windows-Anbieter lautet "WinNT", und dieser Anbieter wird häufig als WinNT-Anbieter bezeichnet. Um auf den WinNT-Anbieter zuzugreifen, binden Sie mithilfe von [WinNT AdsPath](winnt-adspath.md)an eines der [ADSI-Objekte von WinNT.](adsi-objects-of-winnt.md)

Der WinNT-Anbieter ist in der ADSI-Systemkomponente für Windows und Windows Server enthalten.

> [!Note]  
> Der WinNT-Standardanbieter kann nicht als vollständig threadsicher angenommen werden. Writer von Multithreadanwendungen sollten Multithreading verarbeiten, um den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungsobjekten wie Semaphoren, Mutexen, kritischen Abschnitten usw. ordnungsgemäß zu koordinieren.

 

 

 




