---
title: Seien Sie vorsichtig mit anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden.
description: Wenn sich eine Anwendung in einem Prozess mit anderen RPC-Servern befindet, lauschen alle Anwendungen an allen Protokollen.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711573"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Seien Sie vorsichtig mit anderen RPC-Endpunkten, die im selben Prozess ausgeführt werden.

Wenn sich eine Anwendung in einem Prozess mit anderen RPC-Servern befindet, lauschen alle Anwendungen an allen Protokollen. Wenn eine Komponente z. b. [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* nur für LRPC aufruft, ist nicht notwendigerweise nur über LRPC zugänglich. Möglicherweise ist über andere Protokolle darauf zugegriffen werden, da andere RPC-Server im Prozess möglicherweise an Pipes oder Sockets lauschen (z. b.).

Ähnlich wie bei strengen Kontext Handles bedeutet das Platzieren eines anderen Endpunkts im Prozess nicht, dass kein anderer Endpunkt vorhanden ist. Unabhängig davon, wie Sie den Server registrieren, gibt es keine besondere Zuordnung zwischen Ihrer Schnittstelle und dem Endpunkt. alle Schnittstellen können für alle Endpunkte in diesem Prozess aufgerufen werden. Dies ist ein weiterer Grund, warum das Endpunkt Sicherheitsmodell nicht wirksam ist. Wenn eine Sicherheits Beschreibung für einen Endpunkt platziert wird, können Angreifer die-Schnittstelle auf einem anderen Endpunkt abrufen.

Um sicherzustellen, dass ein Prozess nur für eine bestimmte Protokoll Sequenz aufgerufen wird, registrieren Sie eine Sicherheits Rückruffunktion, und überprüfen Sie in dieser Funktion, welche Protokoll Sequenz der Aufruf durchgeführt hat.

 

 




