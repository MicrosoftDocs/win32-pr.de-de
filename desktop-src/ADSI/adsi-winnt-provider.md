---
title: ADSI WinNT-Anbieter
description: Der Microsoft ADSI-Anbieter implementiert eine Reihe von ADSI-Objekten, um verschiedene ADSI-Schnittstellen zu unterstützen.
ms.assetid: 6341be08-2e53-4708-a403-09c86fcc31a8
ms.tgt_platform: multiple
keywords:
- ADSI-WinNT-Anbieter ADSI
- WinNT-Dienstanbieter ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9748e17185417eb382281774c31554cb983742
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387966"
---
# <a name="adsi-winnt-provider"></a>ADSI WinNT-Anbieter

Der Microsoft ADSI-Anbieter implementiert eine Reihe von ADSI-Objekten, um verschiedene ADSI-Schnittstellen zu unterstützen. Der Namespace Name für den Windows-Anbieter ist "Winnt", und dieser Anbieter wird häufig als WinNT-Anbieter bezeichnet. Um auf den WinNT-Anbieter zuzugreifen, binden Sie mithilfe von [Winnt ADsPath](winnt-adspath.md)an eines der [ADSI-Objekte von Winnt](adsi-objects-of-winnt.md).

Der WinNT-Anbieter ist in der ADSI-Systemkomponente für Windows und Windows Server enthalten.

> [!Note]  
> Der standardmäßige WinNT-Anbieter kann nicht als vollständig Thread sicher angesehen werden. Writer von Multithreadanwendungen sollten Multithreading verarbeiten, um den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungs Objekten, wie Semaphore, Mutexen, kritischen Abschnitten usw., ordnungsgemäß zu koordinieren.

 

 

 




