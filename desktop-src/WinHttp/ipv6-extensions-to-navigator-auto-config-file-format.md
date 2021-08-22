---
description: Microsoft hat ein Array von Erweiterungen für das Navigator Auto-Config File Format implementiert, um IPv6-Unterstützung in den WinINet- und WinHTTP WPAD-Hilfsfunktionen hinzuzufügen.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6db6d687cfde0c3289026e8fa36c77c3ff5372727d1604652160b0683169b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644010"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>IPv6-Erweiterungen für das Navigator-Dateiformat für die automatische Konfiguration

Microsoft hat ein Array von Erweiterungen für das Navigator Auto-Config File Format implementiert, um IPv6-Unterstützung in den WinINet- und WinHTTP WPAD-Hilfsfunktionen hinzuzufügen.

Die Explosion des Internets ende der 1990er Jahre hat zu einer unerwarteten Beeinträchtigung der IPv4-Adressen geführt, und der Pool ist täglich erschöpft. IPv6 bietet eine Lösung für dieses Problem, und obwohl es derzeit nicht weit verbreitet ist, wird seine Verwendung in Zukunft definitiv häufiger auftreten. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) ist ein Protokoll, mit dem Webclients automatisch erkennen können, wie die richtige Proxykonfiguration für ihren ausgehenden Datenverkehr aussehen sollte. Dies ist sehr nützlich für Unternehmensbereitstellungen, da IT-Administratoren komplexe Skripts einrichten können, die Datenverkehr für alle Clients basierend auf dem Zielserver, mit dem die Clients eine Verbindung herstellen möchten, an bestimmte Proxys weiterleiten können. WinINet und WinHTTP unterstützen WPAD-Hilfsfunktionen gemäß der [PAC-Dateiformatspezifikation (Navigator Proxy Auto-Config),](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html)die zu einem defacto-Standard geworden ist. Leider wurde diese Spezifikation im Jahr 1996 geschrieben und definiert nicht, was das Funktionsverhalten sein sollte, wenn ein WPAD-Skript in einem IPv6-fähigen Netzwerk bereitgestellt wird.

Da IPv6 die Welle der Zukunft ist, unterstützen alle Windows-Komponenten jetzt duale Stapelnetzwerke (IPv4 und IPv6) und nur IPv6-Netzwerke. Um IPv6 ohne Auswirkungen auf die vorhandene Bereitstellung zu unterstützen, hat Microsoft sechs neue Hilfsfunktionen als Erweiterung zur Spezifikation des PAC-Dateiformats (Navigator Proxy Auto-Config) hinzugefügt und außerdem eine neue IPv6-fähige Funktion namens **FindProxyForURLEx** hinzugefügt, die Administratoren im WPAD-Skript implementieren können.

<dl> <dt>

[IPv6-fähige Proxyhilfs-API-Definitionen](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Unterschiede zwischen IPv6-Aware WPAD-Hilfsfunktionen und älteren WPAD-Hilfsfunktionen](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.

 

 

 



