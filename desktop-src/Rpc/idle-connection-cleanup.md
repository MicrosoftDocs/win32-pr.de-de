---
title: Cleanup für Leerlaufverbindung
description: Standardmäßig werden Verbindungen im Thread Pool erst geschlossen, wenn die gesamte Zuordnung heruntergefahren wird.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855623"
---
# <a name="idle-connection-cleanup"></a>Cleanup für Leerlaufverbindung

Standardmäßig werden Verbindungen im Thread Pool erst geschlossen, wenn die gesamte Zuordnung heruntergefahren wird. Diese Richtlinie ermöglicht es Clients mit einer großen Anzahl von Threads oder Sicherheits Identitäten, RPC-Aufrufe an den Server auf effiziente Weise durchführen zu lassen. Der Nachteil ist, dass eine unordinalmenge von Ressourcen für die Verwaltung dieser Verbindungen zugesichert werden kann. Um den Prozess zu verwalten, stellt RPC die [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) -Funktion bereit. Diese Funktion ermöglicht das Cleanup für Leerlaufverbindungen. der Client scannt den Verbindungspool in regelmäßigen Abständen und schließt Verbindungen, die noch nicht verwendet wurden. Wenn die Zuordnung über Kontext Handles verfügt, werden bei der Bereinigung der Leerlaufverbindung alle Verbindungen im Leerlauf geschlossen. es wird jedoch sichergestellt, dass mindestens eine Verbindung offen bleibt, auch wenn sich die Verbindung im Leerlauf befindet (andernfalls erhält der Server die Durchführung von Kontext Handles). Wenn die Zuordnung keine Kontext Handles beibehalten hat, werden bei der Bereinigung der Leerlaufverbindung alle Verbindungen im Leerlauf geschlossen, auch wenn keine Verbindungen im Pool bestehen.

Unter Windows XP wird die Anzahl der geöffneten Verbindungen in einer Zuordnung von der RPC-Laufzeit nachverfolgt. wenn die Anzahl der Verbindungen in einer Zuordnung einen bestimmten Schwellenwert überschreitet, wird automatisch die Verbindungs Bereinigung im Leerlauf übernommen.

 

 




