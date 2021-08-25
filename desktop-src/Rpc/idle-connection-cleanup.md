---
title: Leerlaufverbindungsbereinigung
description: Verbindungen im Threadpool werden standardmäßig erst geschlossen, wenn die gesamte Zuordnung beendet wurde.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc7a7d4cefcead53e9b92678867cd76ceb6fab7f1ab5f1a573cf75378cf2a5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020800"
---
# <a name="idle-connection-cleanup"></a>Leerlaufverbindungsbereinigung

Verbindungen im Threadpool werden standardmäßig erst geschlossen, wenn die gesamte Zuordnung beendet wurde. Diese Richtlinie ermöglicht Clients mit einer großen Anzahl von Threads oder Sicherheitsidentitäten, RPC-Aufrufe an den Server effizient durchzuführen. Der Nachteil besteht darin, dass für eine übermäßige Menge von Ressourcen ein Commit ausgeführt werden kann, um diese Verbindungen aufrechtzuerhalten. Zum Verwalten des Prozesses stellt RPC die [**RpcMgmtEnableIdleCleanup-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) bereit. Diese Funktion ermöglicht die Bereinigung von Verbindungen im Leerlauf. Der Client scannt den Verbindungspool regelmäßig und schließt Verbindungen, die nicht kürzlich verwendet wurden. Wenn die Zuordnung Kontexthandles beibehalten hat, schließt die Verbindungsbereinigung im Leerlauf alle Verbindungen im Leerlauf, stellt aber sicher, dass mindestens eine Verbindung geöffnet bleibt, auch wenn sich die Verbindung im Leerlauf befindet (andernfalls wird das Kontexthandle heruntergefahren). Wenn die Zuordnung keine Kontexthandles beibehalten hat, schließt die Leerlauf-Verbindungsbereinigung alle Verbindungen im Leerlauf, auch wenn dadurch keine Verbindungen im Pool bestehen bleiben.

Auf Windows XP verfolgt die RPC-Laufzeit die Anzahl der geöffneten Verbindungen in einer Zuordnung nach und aktiviert automatisch die Bereinigung von Verbindungen im Leerlauf, wenn die Anzahl der Verbindungen in einer Zuordnung einen bestimmten Schwellenwert überschreitet.

 

 




