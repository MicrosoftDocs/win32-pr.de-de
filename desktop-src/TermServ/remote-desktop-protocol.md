---
title: Remotedesktopprotokoll
description: Das Microsoft-Remotedesktop Protokoll (RDP) bietet Remote Anzeige-und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Remotedesktopprotokoll (RDP) Remotedesktopdienste
- RDP (siehe Remotedesktopprotokoll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7895163a5ee92a6cc756dca9b097db8498d02e70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338467"
---
# <a name="remote-desktop-protocol"></a>Remotedesktopprotokoll

Das Microsoft-Remotedesktop Protokoll (RDP) bietet Remote Anzeige-und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden. RDP wurde entwickelt, um unterschiedliche Arten von Netzwerktopologien und mehreren LAN-Protokollen zu unterstützen.

> [!Note]  
> Dieses Thema ist für Softwareentwickler konzipiert. Wenn Sie nach Benutzerinformationen für Remotedesktop suchen, finden Sie weitere Informationen [unter Windows-Support](https://windows.microsoft.com/windows/support#1TC=windows-8). Informationen zu Remotedesktop finden Sie unter [Remotedesktopdienste auf TechNet](/windows/deployment/deploy-whats-new).

 

## <a name="basic-architecture"></a>Grundlegende Architektur

RDP basiert auf und einer Erweiterung von, der ITU T. 120-Familie von Protokollen. RDP ist ein Verwaltungs Protokoll mit mehreren Kanälen, das getrennte virtuelle Kanäle für das Ausführen von Gerätekommunikation und Präsentationsdaten vom Server sowie verschlüsselte clientmaus-und Tastatur Daten ermöglicht. RDP stellt eine erweiterbare Basis bereit und unterstützt bis zu 64.000 separate Kanäle für die Datenübertragung und die Bereitstellung von Multipoint-Übertragungen.

Auf dem Server verwendet RDP seinen eigenen Videotreiber zum Rendern der Anzeige Ausgabe, indem die Renderinginformationen mithilfe des RDP-Protokolls in Netzwerkpakete erstellt und über das Netzwerk an den Client gesendet werden. Auf dem Client empfängt RDP Renderingdaten und interpretiert die Pakete in entsprechende API-Aufrufe von Microsoft Windows Graphics Device Interface (GDI). Für den Eingabe Pfad werden Client Maus-und Tastatur Ereignisse vom Client an den Server umgeleitet. Auf dem Server verwendet RDP seinen eigenen Tastatur-und Maustreiber, um diese Tastatur-und Mausereignisse zu empfangen.

In einer Remotedesktop Sitzung werden alle Umgebungsvariablen – z. b. Variablen, die die Farb Tiefe und das Aktivieren und Deaktivieren von – festlegen, durch die RCP-Tcp Verbindungseinstellungen bestimmt. Dies gilt für alle Funktionen und Methoden, die Umgebungsvariablen in der [Remotedesktop-Webverbindung-Referenz](remote-desktop-web-connection-reference.md) und der [Remotedesktopdienste WMI-Anbieter Schnittstelle](terminal-services-wmi-provider-reference.md)festlegen.

## <a name="features"></a>Features

Microsoft RDP umfasst die folgenden Features und Funktionen:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Verschlüsselungs
</dt> <dd>

RDP verwendet die RC4-Verschlüsselung der RSA-Sicherheit, eine streamchiffre, die zum effizienten Verschlüsseln kleiner Datenmengen konzipiert ist. RC4 ist für die sichere Kommunikation über Netzwerke konzipiert. Administratoren können die Verschlüsselung von Daten mithilfe eines 56-oder 128-Bit-Schlüssels auswählen.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Features zur Bandbreiten Reduzierung
</dt> <dd>

RDP unterstützt verschiedene Mechanismen, um die Datenmenge zu reduzieren, die über eine Netzwerkverbindung übertragen wird. Zu den Mechanismen zählen die Datenkomprimierung, das persistente Zwischenspeichern von Bitmaps und das Zwischenspeichern von Symbolen und Fragmenten im RAM. Der persistente Bitmap-Cache kann eine deutliche Verbesserung der Leistung gegenüber Verbindungen mit geringer Bandbreite bieten, insbesondere bei der Ausführung von Anwendungen, die große Bitmaps umfassend nutzen.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roaming getrennt
</dt> <dd>

Ein Benutzer kann die Verbindung mit einer Remote Desktop Sitzung manuell trennen, ohne sich abzumelden. Der Benutzer wird automatisch erneut mit der getrennten Sitzung verbunden, wenn er sich wieder beim System anmeldet, entweder vom gleichen Gerät oder von einem anderen Gerät aus. Wenn die Sitzung eines Benutzers unerwartet durch einen Netzwerk-oder Client Fehler beendet wird, wird der Benutzer getrennt, aber nicht abgemeldet.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Zwischenablage Zuordnung
</dt> <dd>

Benutzer können Text und Grafiken zwischen Anwendungen, die auf dem lokalen Computer ausgeführt werden, und die, die in einer Remote Desktop Sitzung ausgeführt werden, sowie zwischen Sitzungen löschen, kopieren und einfügen.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Druck Umleitung
</dt> <dd>

Anwendungen, die in einer Remote Desktop Sitzung ausgeführt werden, können auf einen Drucker drucken, der an das Client Gerät angeschlossen ist.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtuelle Kanäle
</dt> <dd>

Mithilfe der virtuellen RDP-Kanal Architektur können vorhandene Anwendungen erweitert werden, und neue Anwendungen können entwickelt werden, um Funktionen hinzuzufügen, für die eine Kommunikation zwischen dem Client Gerät und einer Anwendung erforderlich ist, die in einer Remote Desktop Sitzung ausgeführt wird.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Remote Steuerung
</dt> <dd>

Computer Supportmitarbeiter können eine Remote Desktop Sitzung anzeigen und steuern. Das Freigeben von Eingabe-und Anzeige Grafiken zwischen zwei Remote Desktop Sitzungen bietet einem Supportmitarbeiter die Möglichkeit, Probleme Remote zu diagnostizieren und zu beheben.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Netzwerk Lastenausgleich
</dt> <dd>

RDP nutzt den Netzwerk Lastenausgleich (Network Load Balancing, NLB), sofern verfügbar.

</dd> </dl>

Darüber hinaus enthält RDP die folgenden Features:

-   Unterstützung für 24-Bit-Farben.
-   Verbesserte Leistung gegenüber niedriger Geschwindigkeit bei DFÜ-Verbindungen durch reduzierte Bandbreite.
-   Smartcardauthentifizierung über Remotedesktopdienste.
-   Tastatur Einbindung. Die Möglichkeit, spezielle Windows-Tastenkombinationen im Vollbildmodus an den lokalen Computer oder einen Remote Computer weiterzuleiten.
-   Audio-, Laufwerk-, Port-und Netzwerkdrucker Umleitung. Sounds, die auf dem Remote Computer auftreten, können auf dem Client Computer, auf dem der RDC-Client ausgeführt wird, und lokale Client Laufwerke für die Remote Desktop Sitzung angezeigt werden.

 

 