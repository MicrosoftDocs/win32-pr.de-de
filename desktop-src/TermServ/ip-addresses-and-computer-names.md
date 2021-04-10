---
title: IP-Adressen und Computernamen
description: Es darf nicht davon ausgegangen werden, dass der Computername oder die dem Computer zugewiesene IP-Adresse mit einem einzelnen Benutzer zusammenhängen, da mehrere Benutzer gleichzeitig an einem Remote Desktop Session Host-Server (RD Session Host) angemeldet sein können.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316196"
---
# <a name="ip-addresses-and-computer-names"></a>IP-Adressen und Computernamen

Mehrere Benutzer können gleichzeitig an einem Remotedesktop-Sitzungshost Server (RD-Sitzungshost) angemeldet werden. Folglich ist es nicht sicher anzunehmen, dass der Computername oder die IP-Adresse, die dem Computer zugewiesen ist, einem einzelnen Benutzer zugeordnet ist. Dies unterscheidet sich von einer Einzelbenutzer-Windows-Umgebung, in der jeweils nur ein Benutzer angemeldet ist.

Anwendungen, die den Computernamen oder die IP-Adresse für die Lizenzierung oder die Identifizierung einer Iterations Iterations Anwendung im Netzwerk verwenden, funktionieren in einer Remotedesktopdienste Umgebung nicht ordnungsgemäß, da der Computername oder die IP-Adresse des Servers vielen Benutzern zugeordnet werden können.

In einer Remotedesktopdienste Umgebung hat jedes Client Terminal oder jeder Terminal Emulator eine separate IP-Adresse und einen anderen Computernamen. Rufen Sie zum Abrufen der IP-Adresse und des Computer namens eines Clients die [**wzquerysessioninformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) -Funktion auf. Andere Funktionen, die diese Netzwerkadressen und Computernamen abrufen, rufen den Namen und die Adresse des RD-Sitzungshost Servers ab. Die Funktion [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) gibt z. b. den Computernamen des Servers zurück.

 

 