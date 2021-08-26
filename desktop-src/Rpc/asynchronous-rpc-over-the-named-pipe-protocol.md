---
title: Asynchroner RPC über das Named-Pipe Protokoll
description: Wenn Sie Named Pipes (ncacn np) als Transportprotokoll verwenden, sollten Sie vermeiden, eine große Anzahl ausstehender Aufrufe im Leerlauf auf \_ dem Server zu erlauben.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1dade78846bc978abeb8bbbe5c324144db2645177722ca5afd1a62f99a3ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023670"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>Asynchroner RPC über das Named-Pipe Protokoll

Wenn Sie Named Pipes ([**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)) als Transportprotokoll verwenden, sollten Sie vermeiden, eine große Anzahl ausstehender Aufrufe im Leerlauf auf dem Server zu erlauben. Bei Named Pipes wird jedem Client, der auf eine Antwort wartet, eine ausstehende Named Pipe auf dem Server gelesen, von der jeder eine bestimmte Menge an Kernelspeicher benötigt.

Sie möchten beispielsweise keinen Benachrichtigungsaufruf für neue E-Mails mit dem Named Pipe-Transport verwenden, da ein solcher Aufruf auch dann aussteht, wenn clients sich im Leerlauf befinden, und der Kernelspeicher erschöpft sein könnte. Beachten Sie, dass dies kein Problem mit den anderen verbindungsorientierten Protokollen ist, z. B. [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp).

Da Named Pipes ein Transportprotokoll sind, kann Ihre Anwendung sie verwenden, indem [**sie ncacn \_ np**](/windows/desktop/Midl/ncacn-np) als Protokoll in einer Zeichenfolgenbindung angibt. Weitere Informationen zu Named Pipes finden Sie unter [Named Pipes](/windows/desktop/ipc/named-pipes). Weitere Informationen zum Erstellen von Zeichenfolgenbindungen finden Sie unter [Verwenden von Zeichenfolgenbindungen.](finding-server-host-systems.md)

 

 