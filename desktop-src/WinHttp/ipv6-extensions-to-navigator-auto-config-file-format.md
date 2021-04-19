---
description: Microsoft hat ein Array von Erweiterungen für das Auto-config-Datei Format des Navigators implementiert, um die IPv6-Unterstützung in WinInet-und WinHTTP WPAD-Hilfsfunktionen hinzuzufügen.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b57fce93caaf7790136ee9ac7db04017d9ac11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373267"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>IPv6-Erweiterungen für das Auto-config-Datei Format des Navigators

Microsoft hat ein Array von Erweiterungen für das Auto-config-Datei Format des Navigators implementiert, um die IPv6-Unterstützung in WinInet-und WinHTTP WPAD-Hilfsfunktionen hinzuzufügen.

Die Explosion des Internets in den späten 90er Jahren hat einen unerwarteten Mangel an IPv4-Adressen verursacht, wobei der Pool täglich erschöpft ist. IPv6 bietet eine Lösung für dieses Problem, und obwohl es zurzeit nicht weit bereitgestellt ist, wird seine Verwendung in Zukunft definitiv stärker verbreitet. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) ist ein Protokoll, mit dem Webclients automatisch erkennen können, welche Proxykonfiguration für den ausgehenden Datenverkehr vorgesehen sein sollte. Dies ist für Unternehmens Bereitstellungen sehr nützlich, da IT-Administratoren komplexe Skripts einrichten können, die den Datenverkehr für alle Clients basierend auf dem Zielserver, mit dem die Clients eine Verbindung herstellen möchten, an bestimmte Proxys weiterleiten können. WinInet und WinHTTP unterstützen WPAD-Hilfsobjekte entsprechend der Definition der [PAC-Datei Format Spezifikation (Navigator Proxy Auto-config)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), die zu einem Standardwert geworden ist. Leider wurde diese Spezifikation in 1996 geschrieben und definiert nicht, was das Verhalten der Funktion sein sollte, wenn ein WPAD-Skript in einem IPv6-fähigen Netzwerk bereitgestellt wird.

Da IPv6 die Welle der Zukunft ist, unterstützen alle Windows-Komponenten jetzt Dual Stack-(IPv4-und IPv6-) und reine IPv6-Netzwerke. Um IPv6 zu unterstützen, ohne die vorhandene Bereitstellung zu beeinträchtigen, hat Microsoft sechs neue Hilfsklassen Funktionen als Erweiterung der PAC-Datei Format Spezifikation (Navigator Proxy Auto-config) hinzugefügt und außerdem eine neue IPv6-fähige Funktion namens " **findproxyforurlex** " hinzugefügt, die Administratoren im WPAD-Skript implementieren können.

<dl> <dt>

[IPv6-abhängige proxyhilfsobjekts-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Unterschiede zwischen IPv6-Aware WPAD-Hilfsfunktionen und älteren WPAD-Hilfsfunktionen](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.

 

 

 



