---
title: Asynchroner RPC über das Named-Pipe Protokoll
description: Wenn Sie Named Pipes (ncacn \_ NP) als Transportprotokoll verwenden, sollten Sie eine große Anzahl von ausstehenden aufrufen auf dem Server vermeiden.
ms.assetid: a1d0f758-91bc-4821-9a82-64ba6ce575ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf46f9e1c2ea5eb3fe20203db274233f5c10dec5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949039"
---
# <a name="asynchronous-rpc-over-the-named-pipe-protocol"></a>Asynchroner RPC über das Named-Pipe Protokoll

Wenn Sie Named Pipes ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)) als Transportprotokoll verwenden, sollten Sie eine große Anzahl von ausstehenden aufrufen auf dem Server vermeiden. Bei Named Pipes weist jeder Client, der auf eine Antwort wartet, eine ausstehende Named Pipe auf dem Server auf, für die jeweils eine bestimmte Menge an Kernel Speicher erforderlich ist.

Beispielsweise möchten Sie keinen Benachrichtigungs Befehl für eine neue e-Mail-Adresse mit dem Named Pipe-Transport verwenden, da ein solcher aufrufener auch dann aussteht, wenn sich Clients im Leerlauf befinden und der Kernel Speicher erschöpft sein könnte. Beachten Sie, dass dies kein Problem mit den anderen Verbindungs orientierten Protokollen ist, wie z. b. [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp).

Da Named Pipes ein Transportprotokoll sind, kann Sie von Ihrer Anwendung verwendet werden, indem [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) als Protokoll in einer Zeichen folgen Bindung angegeben wird. Weitere Informationen zu Named Pipes finden Sie unter [Named Pipes](/windows/desktop/ipc/named-pipes). Ausführliche Informationen zum Erstellen von Zeichen folgen Bindungen finden [Sie unter Verwenden von Zeichen folgen Bindungen](finding-server-host-systems.md).

 

 