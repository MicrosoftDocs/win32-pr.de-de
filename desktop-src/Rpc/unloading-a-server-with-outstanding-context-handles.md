---
title: Entladen eines Servers mit ausstehenden Kontext Handles
description: Normalerweise war das Entladen einer DLL, die RPC-Aufrufe mithilfe von Kontext Handles verarbeitet, ohne den Hostingprozess zu beenden, problematisch.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207280"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>Entladen eines Servers mit ausstehenden Kontext Handles

Normalerweise war das Entladen einer DLL, die RPC-Aufrufe mithilfe von Kontext Handles verarbeitet, ohne den Hostingprozess zu beenden, problematisch. Dies liegt daran, dass die Lauf Zeit Routine nicht mehr gültig ist, wenn die DLL entladen wird. Wenn ein Client mit einem zuvor geöffneten Kontext Handle fehlschlägt und die RPC-Laufzeit versucht, das Kontext Handle zu schließen, verstößt der Versuch, den Zugriff auf die Lauf Zeit Routine aufzurufen, und der Server stürzt ab.

Ab Windows XP wurde eine neue API mit dem Namen " [**rpcserverunregisterifex**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) " hinzugefügt. **Rpcserverunregisterifex** schließt Kontext Handles, die von der Schnittstelle geöffnet werden, deren Registrierung aufgehoben wird. die Funktion [**rpcserverunregisterif**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) ist nicht verfügbar. Die Verwendung von **rpcserverunregisterifex** ist nicht erforderlich, wenn der gesamte Prozess heruntergefahren wird. Dies ist jedoch notwendig, wenn mindestens eine DLLs, die die Lauf Zeit Routinen gehostet, entladen wird, während ausstehende Kontext Handles vorhanden sind.

 

 




