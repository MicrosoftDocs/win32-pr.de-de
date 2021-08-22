---
title: Hostnamen und IP-Adressen
description: TCP/IP-Netzwerke erfordern, dass Hostnamen in IP-Adressen aufgelöst werden, bevor die Adressinformationen zum Erstellen einer Verbindung verwendet werden können.
ms.assetid: f077e7d0-2e2c-4a2b-b5cd-1c7f43f7743b
keywords:
- Hostnamen und IP-Adressen SNMP
- Hostnamen, Auflösen von SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53f884f8ed681a5fc4864665f4c2a97ef8ed9fc0d81756d51848428b76163f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009508"
---
# <a name="host-names-and-ip-addresses"></a>Hostnamen und IP-Adressen

TCP/IP-Netzwerke erfordern, dass Hostnamen in IP-Adressen aufgelöst werden, bevor die Adressinformationen zum Erstellen einer Verbindung verwendet werden können. Computer, die auf dem Windows Betriebssystem ausgeführt werden, verwenden eine Hostdatei, die zu diesem Zweck Hostnamen IP-Adressen zulistet.

Die Hostdatei ist eine Textdatei, die explizite Hostnamen und IP-Adressen auflistet. Die Hostdatei wird beim Start automatisch in den Arbeitsspeicher geladen und abgefragt, wenn ein Hostname eine Auflösung erfordert. Wenn die Hostdatei nicht die Zuordnungsinformationen enthält, die zum Auflösen eines bestimmten Hostnamens in seine IP-Adresse erforderlich sind, wird eine Auflösungsabfrage an einen DNS-Server durchgeführt.

SNMP verwendet die Windows Internet Naming Service (WINS) für die Hostnamensauflösung. WINS ermöglicht das Zuordnen von NetBIOS-Namen oder Computernamen zu IP-Adressen in TCP/IP-Netzwerken. Wenn der Computer nicht auf einen WINS-Server zugreifen kann, verwendet der SNMP-Dienst die Hostdatei, um Hostnamen in IP-Adressen aufzulösen.

Der SNMP-Dienst unterstützt die Verwendung von Hostnamen und IP-Adressen. Wenn Sie jedoch zwischen Hostnamen oder IP-Adressen zum Identifizieren von Netzwerkadressen wählen können, sollten Ihre SNMP-Verwaltungsanwendungen Hostnamen verwenden. Wenn Sie Hostnamen verwenden, fügen Sie der Hostdatei alle Zuordnungen von Hostnamen und IP-Adressen der beteiligten Systeme hinzu.

 

 




