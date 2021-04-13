---
title: Verarbeiten von asynchronen Aufrufen
description: Die Manager-Routine einer asynchronen Funktion empfängt immer das asynchrone Handle als ersten Parameter. Der Server muss dieses Handle nachverfolgen und zum Senden der Antwort verwenden, wenn der asynchrone Remote Prozedur Aufrufvorgang abgeschlossen ist.
ms.assetid: 4f38b68b-0bea-4fa7-8c7e-dd09e7daf8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e04dc7feed0d7bee47f6fa51583cf8de3a8e42f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388420"
---
# <a name="handling-asynchronous-calls"></a>Verarbeiten von asynchronen Aufrufen

Die Manager-Routine einer asynchronen Funktion empfängt immer das asynchrone Handle als ersten Parameter. Der Server muss dieses Handle nachverfolgen und zum Senden der Antwort verwenden, wenn der asynchrone Remote Prozedur Aufrufvorgang abgeschlossen ist.

Wenn der Server einen asynchronen RPC abbrechen muss, wird [**rpcasyncabortcallaufgerufen**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall). Diese Funktion führt dieselbe serverseitige Bereinigung wie [**rpcasynccompletecalldurch**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) und gibt einen Ausnahme Code (von der Serveranwendung bereitgestellt) an den Client zurück, mit dem Unterschied, dass er keine Marshalling der out-Argumente ausführt.

Ein Beispiel für eine asynchrone Prozedur finden Sie unter [Senden der asynchronen Antwort](sending-the-asynchronous-reply.md).

 

 




