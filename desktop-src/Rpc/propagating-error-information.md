---
title: Weitergeben von Fehlerinformationen
description: Durch die Weitergabe erweiterter Fehlerinformationen können Server, die einen RPC \_ S \_ \-Fehler oder einen anderen Fehlercode erhalten, der RPC-Laufzeit erlauben, die empfangenen Informationen an die Aufrufer weiterzuleiten.
ms.assetid: f0395f19-ceb1-4249-892e-9b688464d0d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 510ecf011dbac01d2b4c931a463bebb3739a92322059eb3a7a342160c42a9e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927158"
---
# <a name="propagating-error-information"></a>Weitergeben von Fehlerinformationen

Durch die Weitergabe erweiterter Fehlerinformationen können Server, die einen \_ RPC-S-Fehler \_ \* oder einen anderen Fehlercode erhalten, die RPC-Laufzeit in die Lage versetzen, die empfangenen Informationen an die Aufrufer weiterzuleiten. Der Server muss nur [**rpcRhouexception**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcraiseexception) oder [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) aufrufen, wenn ein schwerwiegender Fehler auftritt. Die RPC-Laufzeit übernimmt die Verkettung der erweiterten Fehlerinformationen, sofern vorhanden, wodurch der schwerwiegende Fehler selbst gemeldet wird, solange der Fehlercode, der **an RpcRaisException** oder **RpcAsyncAbortCall** übergeben wird, mit dem Fehlercode identisch ist, der den schwerwiegenden Fehler verursacht.

 

 




