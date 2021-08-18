---
title: Remotedesktopdienste-API
description: Die Remotedesktopdienste-API ist in erster Linie für Client-/Serveranwendungen und Anwendungen für Remotedesktopdienste Verwaltung nützlich.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbdaff1f09a0de3fad20f4de334af1030c52e16ef795b1ece51cdaead639825a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000110"
---
# <a name="remote-desktop-services-api"></a>Remotedesktopdienste-API

Die meisten Anwendungen werden ohne Änderungen in einer Remotedesktopdienste -Umgebung (früher als Terminaldienste bezeichnet) ausgeführt und müssen nicht die Remotedesktopdienste-API verwenden. Die Remotedesktopdienste-API ist in erster Linie für Client-/Serveranwendungen und Anwendungen für Remotedesktopdienste Verwaltung nützlich.

Die Remotedesktopdienste-API besteht aus einer Reihe von Funktionsaufrufen in Wtsapi32.dll. Um Ihre Anwendung so zu entwerfen, dass sie sowohl in Remotedesktopdienste- als auch in nicht Remotedesktopdienste Umgebungen ausgeführt wird, verwenden Sie die dynamische Laufzeitverknüpfung, um zu überprüfen, ob Wtsapi32.dll vorhanden ist. Weitere Informationen finden Sie unter [Laufzeitverknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Mit der Remotedesktopdienste-API können Anwendungen die folgenden Aufgaben in einer Remotedesktopdienste Umgebung ausführen:

-   [Remotedesktopdienste Verwaltung,](terminal-services-administration.md)z. B. Aufzählen und Verwalten von Remotedesktop-Sitzungshost -Servern (RD-Sitzungshost) (früher als Terminalserver bezeichnet) in einer Domäne oder Aufzählen und Verwalten von Sitzungen und Prozessen auf einem RD-Sitzungshost-Server.
-   Erweitern von Client-/Serveranwendungen in einer Remotedesktopdienste-Umgebung.
-   Verwenden von [Remotedesktopdienste virtuellen Kanälen](terminal-services-virtual-channels.md) für die Kommunikation zwischen Client- und Servermodulen einer Anwendung.
-   [Festlegen und Abrufen Remotedesktopdienste spezifischen Benutzerkonfigurationsinformationen.](terminal-services-user-configuration.md)

 

 




