---
title: Endpunkt Sicherheit nicht verwenden
description: Endpoint Security ist ein Sicherheitsmodell, bei dem eine Sicherheits Beschreibung angegeben wird, wenn ein Endpunkt mit der RpcServerUseProtseq \-Gruppe von RPC-Funktionen erstellt wird.
ms.assetid: 5b8841c4-5b65-417f-b790-e8c2dabb44a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289513810ba7e67e0da625151c3c2975e0eaaf99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709960"
---
# <a name="do-not-use-endpoint-security"></a>Endpunkt Sicherheit nicht verwenden

Endpoint Security ist ein Sicherheitsmodell, bei dem eine Sicherheits Beschreibung angegeben wird, wenn ein Endpunkt mit der [**rpcserveruseprotabq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) - \* Gruppe der RPC-Funktionen erstellt wird. Verwenden Sie dieses Sicherheitsmodell nicht. Weisen Sie diesen Funktionen keine Sicherheits Beschreibungen zu. Diese Methode ist am besten eine Verschwendung von CPU-Ressourcen. Im schlimmsten Fall kann es in vielen Umgebungen vorkommen, dass die Sicherheits Beschreibung umgangen werden kann, da die auf [anderen RPC-Endpunkten, die im gleichen Prozessabschnitt ausgeführt werden](be-wary-of-other-rpc-endpoints-running-in-the-same-process.md) , ein Blick darauf hat.

Die Endpunkt Sicherheit ist nur aus Gründen der Abwärtskompatibilität vorhanden.

 

 




