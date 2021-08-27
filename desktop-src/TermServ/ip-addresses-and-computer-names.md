---
title: IP-Adressen und Computernamen
description: Es darf nicht davon ausgegangen werden, dass der Computername oder die dem Computer zugewiesene IP-Adresse mit einem einzelnen Benutzer zusammenhängen, da mehrere Benutzer gleichzeitig an einem Remote Desktop Session Host-Server (RD Session Host) angemeldet sein können.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45aa6027a5cf7714d2d88fd3527182d5586982e02417e5ddb26ea3c086b9219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129537"
---
# <a name="ip-addresses-and-computer-names"></a>IP-Adressen und Computernamen

Mehrere Benutzer können gleichzeitig bei einem Remotedesktop-Sitzungshost (RD-Sitzungshost) angemeldet werden. Daher kann nicht davon ausgegangen werden, dass der Computername oder die ip-Adresse, die dem Computer zugewiesen ist, einem einzelnen Benutzer zugeordnet sind. Dies unterscheidet sich von einer umgebungsbasierten Windows, in der immer nur ein Benutzer gleichzeitig angemeldet ist.

Anwendungen, die den Computernamen oder die IP-Adresse für die Lizenzierung oder zur Identifizierung einer Iteration der Anwendung im Netzwerk verwenden, funktionieren in einer Remotedesktopdienste-Umgebung nicht ordnungsgemäß, da der Computername oder die IP-Adresse des Servers vielen Benutzern zugeordnet werden kann.

In einer Remotedesktopdienste verfügt jedes Clientterminal oder jeder Terminalemulator über eine separate IP-Adresse und einen separaten Computernamen. Um die IP-Adresse und den Computernamen eines Clients abzurufen, rufen Sie die [**WTSQuerySessionInformation-Funktion**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) auf. Andere Funktionen, die diese Netzwerkadressen und Computernamen abrufen, rufen den Namen und die Adresse des RD-Sitzungshost ab. Die [**GetComputerNameEx-Funktion gibt**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) beispielsweise den Computernamen des Servers zurück.

 

 