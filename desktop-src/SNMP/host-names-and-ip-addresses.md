---
title: Hostnamen und IP-Adressen
description: Für TCP/IP-Netzwerke müssen Hostnamen in IP-Adressen aufgelöst werden, bevor die Adressinformationen zum Erstellen einer Verbindung verwendet werden können.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Hostnamen und IP-Adressen SNMP
- Hostnamen, Auflösen von SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f711be9e1fda5dc936db6628cccc21093aa09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709581"
---
# <a name="host-names-and-ip-addresses"></a>Hostnamen und IP-Adressen

Für TCP/IP-Netzwerke müssen Hostnamen in IP-Adressen aufgelöst werden, bevor die Adressinformationen zum Erstellen einer Verbindung verwendet werden können. Auf Computern, auf denen das Windows-Betriebssystem ausgeführt wird, wird eine Hostdatei verwendet, die zu diesem Zweck Hostnamen zu IP-Adressen zuordnet.

Die Hostdatei ist eine Textdatei, die explizite Hostnamen und IP-Adressen auflistet. Die Hostdatei wird beim Start automatisch in den Arbeitsspeicher geladen und für den Fall, dass ein Hostname aufgelöst werden muss, angezeigt. Wenn die Hostdatei nicht die zum Auflösen eines bestimmten Host namens in die IP-Adresse erforderlichen Mapping-Informationen enthält, wird eine Auflösungs Abfrage an einen DNS-Server vorgenommen.

SNMP verwendet Windows Internet Naming Service (WINS) für die Host Namensauflösung. WINS ermöglicht das Zuordnen von NetBIOS-Namen oder Computernamen zu IP-Adressen in TCP/IP-Netzwerken. Wenn der Computer nicht auf einen WINS-Server zugreifen kann, verwendet der SNMP-Dienst die Hostdatei, um Hostnamen in IP-Adressen aufzulösen.

Der SNMP-Dienst unterstützt die Verwendung von Hostnamen und IP-Adressen. Wenn Sie jedoch die Möglichkeit haben, Host Namen oder IP-Adressen zur Identifizierung von Netzwerk Standorten zu verwenden, sollten die SNMP-Verwaltungs Anwendungen Hostnamen verwenden. Wenn Sie Hostnamen verwenden, fügen Sie der Hostdatei alle Zuordnungen von Hostnamen und IP-Adressen der teilnehmenden Systeme hinzu.

 

 




