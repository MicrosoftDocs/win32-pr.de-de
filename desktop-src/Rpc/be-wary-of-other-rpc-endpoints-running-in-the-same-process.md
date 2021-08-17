---
title: Seien Sie vorsichtig bei anderen RPC-Endpunkten, die im gleichen Prozess ausgeführt werden
description: Wenn sich eine Anwendung in einem Prozess mit anderen RPC-Servern befindet, lauschen alle Anwendungen an allen Protokollen.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2044b83de96a352546d90c45cd54879fc87923786b7852133ffeb28dbf9cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932351"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Seien Sie vorsichtig bei anderen RPC-Endpunkten, die im gleichen Prozess ausgeführt werden

Wenn sich eine Anwendung in einem Prozess mit anderen RPC-Servern befindet, lauschen alle Anwendungen an allen Protokollen. Wenn also eine Komponente [**rpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* nur für LRPC aufruft, ist sie nicht notwendigerweise nur über LRPC zugänglich. Sie kann über andere Protokolle zugänglich sein, da andere RPC-Server im Prozess möglicherweise an Pipes oder Sockets lauschen (z. B. ).

Ähnlich wie bei strikten Kontexthandles bedeutet das Nicht-Setzen eines anderen Endpunkts in den Prozess nicht, dass kein anderer Endpunkt vorhanden ist. Unabhängig davon, wie Sie Ihren Server registrieren, besteht keine besondere Zuordnung zwischen Ihrer Schnittstelle und Ihrem Endpunkt. alle Schnittstellen können auf allen Endpunkten in diesem Prozess aufgerufen werden. Dies ist ein weiterer Grund, warum das Endpunktsicherheitsmodell ineffektiv ist. Wenn eine Sicherheitsbeschreibung auf einem Endpunkt platziert wird, können Angreifer die Schnittstelle auf einem anderen Endpunkt aufrufen.

Um sicherzustellen, dass ein Prozess nur für eine bestimmte Protokollsequenz aufgerufen wird, registrieren Sie eine Sicherheitsrückruffunktion, und überprüfen Sie in dieser Funktion, welche Protokollsequenz der Aufruf erfolgt.

 

 




