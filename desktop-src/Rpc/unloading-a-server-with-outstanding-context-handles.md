---
title: Entladen eines Servers mit ausstehenden Kontexthandles
description: In der Regel war das Entladen einer DLL, die RPC-Aufrufe mithilfe von Kontexthandles verarbeitet, ohne zuerst den Hostingprozess zu beenden, problematisch.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e581ff142c7453f4a9e9f1e40a5ab9991257a350a84b2fcb2ea08a0e157288cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010948"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Entladen eines Servers mit ausstehenden Kontexthandles

In der Regel war das Entladen einer DLL, die RPC-Aufrufe mithilfe von Kontexthandles verarbeitet, ohne zuerst den Hostingprozess zu beenden, problematisch. Dies liegt daran, dass die Run-Down-Routine nicht mehr gültig ist, wenn die DLL entladen wird. Wenn ein Client mit einem zuvor geöffneten Kontexthandle fehlschlägt und die RPC-Laufzeit versucht, das Kontexthandle zu schließen, verstößt der Versuch, den Routinezugriff für die Ausführung aufzurufen, und der Server stürzt ab.

Ab Windows XP wurde eine neue API namens [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) hinzugefügt. **RpcServerUnregisterIfEx** schließt Kontexthandles, die von der nicht registrierten Schnittstelle geöffnet werden. die [**RpcServerUnregisterIf-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) nicht. Die Verwendung von **RpcServerUnregisterIfEx** ist nicht erforderlich, wenn der gesamte Prozess heruntergefahren wird. Dies ist jedoch erforderlich, wenn eine oder mehrere DLLs, die die Run-Down-Routinen hosten, entladen werden, während ausstehende Kontexthandles vorhanden sind.

 

 




