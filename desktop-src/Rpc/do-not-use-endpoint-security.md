---
title: Endpunktsicherheit nicht verwenden
description: Endpunktsicherheit ist ein Sicherheitsmodell, bei dem ein Sicherheitsdeskriptor angegeben wird, wenn ein Endpunkt mit der RpcServerUseProtseq\-Gruppe von RPC-Funktionen erstellt wird.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241d302ec0d331eaadb3291e36b30084264b4a6331745110fc642dd2ede02c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930697"
---
# <a name="do-not-use-endpoint-security"></a>Endpunktsicherheit nicht verwenden

Endpunktsicherheit ist ein Sicherheitsmodell, bei dem ein Sicherheitsdeskriptor angegeben wird, wenn ein Endpunkt mit der [**RpcServerUseProtseq-Gruppe**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* von RPC-Funktionen erstellt wird. Verwenden Sie dieses Sicherheitsmodell nicht. Geben Sie diesen Funktionen keine Sicherheitsbeschreibungen. Im besten Beispiel ist diese Methode eine Verschwendung von CPU-Ressourcen. Im schlimmsten Fall ist es in vielen Umgebungen möglich, den Sicherheitsdeskriptor zu umgehen, wie im Abschnitt [Be Wary of Other RPC Endpoints Running In the Same Process (Im gleichen Prozess ausgeführte RPC-Endpunkte)](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) veranschaulicht wird.

Endpunktsicherheit ist nur aus Gründen der Abwärtskompatibilität vorhanden.

 

 




