---
title: Weitergeben von Fehlerinformationen
description: Durch die Weitergabe erweiterter Fehlerinformationen können Server, die einen RPC- \_ \_ Fehler oder einen anderen Fehlercode erhalten, die von der RPC-Laufzeit empfangenen Informationen an die Aufrufer weitergeben.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd20575cee304c0a1693ae4bc6442de4837caa0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856668"
---
# <a name="propagating-error-information"></a>Weitergeben von Fehlerinformationen

Das weitergeben erweiterter Fehlerinformationen ermöglicht Servern, die einen RPC- \_ \_ \* Fehler oder einen anderen Fehlercode erhalten, das Weitergeben der empfangenen Informationen an die Aufrufer durch die RPC-Laufzeit. Der Server muss beim Auftreten eines schwerwiegenden Fehlers [**rpcraiseexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) oder [**rpcasyncabortcallaufgerufen**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) werden. Die RPC-Laufzeit übernimmt ggf. die Verkettung der erweiterten Fehlerinformationen, was den schwerwiegenden Fehler verursacht, um den schwerwiegenden Fehler zu melden, sofern der Fehlercode für **rpcraiseexception** oder **rpcasyncabortcallcenter** mit dem Fehlercode übereinstimmt, der den schwerwiegenden Fehler verursacht hat.

 

 




