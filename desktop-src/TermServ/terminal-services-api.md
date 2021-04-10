---
title: Remotedesktopdienste-API
description: Die Remotedesktopdienste-API ist in erster Linie für Client/Server-Anwendungen und-Anwendungen zur Remotedesktopdienste Verwaltung nützlich.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855900"
---
# <a name="remote-desktop-services-api"></a>Remotedesktopdienste-API

Die meisten Anwendungen werden unverändert in einer Remotedesktopdienste (ehemals Terminaldiensteumgebung) ausgeführt und müssen nicht die Remotedesktopdienste-API verwenden. Die Remotedesktopdienste-API ist in erster Linie für Client/Server-Anwendungen und-Anwendungen zur Remotedesktopdienste Verwaltung nützlich.

Die Remotedesktopdienste-API ist ein Satz von Funktionsaufrufen in Wtsapi32.dll. Wenn Sie Ihre Anwendung so entwerfen möchten, dass Sie sowohl in Remotedesktopdienste-als auch in einer nicht-Remotedesktopdienste-Umgebung ausgeführt wird, verwenden Sie die dynamische Verknüpfung zur Laufzeit, um das vorhanden sein Wtsapi32.dll Weitere Informationen finden Sie unter [Lauf Zeit Verknüpfung mit Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

Die Remotedesktopdienste-API ermöglicht es Anwendungen, die folgenden Aufgaben in einer Remotedesktopdienste Umgebung auszuführen:

-   [Remotedesktopdienste Verwaltung](terminal-services-administration.md), z. b. das Auflisten und Verwalten von Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern (früher als Terminal Server bezeichnet) in einer Domäne oder das Auflisten und Verwalten von Sitzungen und Prozessen auf einem RD-Sitzungshost Server.
-   Verbessern von Client/Server-Anwendungen in einer Remotedesktopdienste Umgebung.
-   Verwenden von [Remotedesktopdienste virtuellen Kanälen](terminal-services-virtual-channels.md) für die Kommunikation zwischen Client-und Server Modulen einer Anwendung.
-   [Festlegen und Abrufen Remotedesktopdienste spezifischer Benutzer Konfigurationsinformationen](terminal-services-user-configuration.md).

 

 




