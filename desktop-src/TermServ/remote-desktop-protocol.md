---
title: Remotedesktopprotokoll
description: Das Microsoft-Remotedesktop-Protokoll (RDP) bietet Remoteanzeige- und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Remotedesktopprotokoll (RDP) Remotedesktopdienste
- RDP (siehe Remotedesktopprotokoll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a322e90bd036533e357925607fac6a78c364eababad5f353b4d53dfa51df735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756171"
---
# <a name="remote-desktop-protocol"></a>Remotedesktopprotokoll

Das Microsoft-Remotedesktop-Protokoll (RDP) bietet Remoteanzeige- und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden. RDP ist für die Unterstützung verschiedener Arten von Netzwerktopologien und mehrerer LAN-Protokolle konzipiert.

> [!Note]  
> Dieses Thema richtet sich an Softwareentwickler. Benutzerinformationen für Remotedesktop finden Sie unter [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8). Informationen zu IT-Experten für Remotedesktop finden Sie unter [Remotedesktopdienste auf TechNet.](/windows/deployment/deploy-whats-new)

 

## <a name="basic-architecture"></a>Grundlegende Architektur

RDP basiert auf und einer Erweiterung der ITU T.120-Protokollfamilie. RDP ist ein mehrkanalfähiges Protokoll, das separate virtuelle Kanäle zum Übertragen von Gerätekommunikations- und Präsentationsdaten vom Server sowie verschlüsselte Clientmaus- und Tastaturdaten ermöglicht. RDP bietet eine erweiterbare Basis und unterstützt bis zu 64.000 separate Kanäle für die Datenübertragung und Stellt für die Mehrpunktübertragung bereit.

Auf dem Server verwendet RDP einen eigenen Videotreiber, um die Anzeigeausgabe zu rendern, indem die Renderinginformationen mithilfe des RDP-Protokolls in Netzwerkpaketen erstellt und über das Netzwerk an den Client gesendet werden. Auf dem Client empfängt RDP Renderingdaten und interpretiert die Pakete in entsprechende Microsoft Windows GDI-API-Aufrufe (Graphics Device Interface). Für den Eingabepfad werden Clientmaus- und Tastaturereignisse vom Client an den Server umgeleitet. Auf dem Server verwendet RDP einen eigenen Tastatur- und Maustreiber, um diese Tastatur- und Mausereignisse zu empfangen.

In einer Remotedesktop Sitzung werden alle Umgebungsvariablen , z. B. Variablen, die die Farbtiefe bestimmen und Hintergrundbilder aktivieren und deaktivieren, durch die RCP-Tcp Verbindungseinstellungen bestimmt. Dies gilt für alle Funktionen und Methoden, die Umgebungsvariablen im [Remotedesktop-Webverbindung Reference](remote-desktop-web-connection-reference.md) und der [Remotedesktopdienste WMI-Anbieterschnittstelle](terminal-services-wmi-provider-reference.md)festlegen.

## <a name="features"></a>Features

Microsoft RDP umfasst die folgenden Features und Funktionen:

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Verschlüsselung
</dt> <dd>

RDP verwendet die RC4-Verschlüsselung von RSA Security, eine Streamchiffre, mit der kleine Datenmengen effizient verschlüsselt werden können. RC4 ist für die sichere Kommunikation über Netzwerke konzipiert. Administratoren können Daten mit einem 56- oder 128-Bit-Schlüssel verschlüsseln.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Features zur Bandbreitenreduzierung
</dt> <dd>

RDP unterstützt verschiedene Mechanismen, um die Datenmenge zu reduzieren, die über eine Netzwerkverbindung übertragen wird. Zu den Mechanismen gehören die Datenkomprimierung, das persistente Zwischenspeichern von Bitmaps und das Zwischenspeichern von Glyphen und Fragmenten im RAM. Der persistente Bitmapcache kann eine erhebliche Leistungsverbesserung gegenüber Verbindungen mit geringer Bandbreite bieten, insbesondere bei der Ausführung von Anwendungen, die große Bitmaps umfassend verwenden.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Roamingverbindung trennen
</dt> <dd>

Ein Benutzer kann die Verbindung mit einer Remotedesktopsitzung manuell trennen, ohne sich abzumelden. Der Benutzer wird automatisch wieder mit seiner getrennten Sitzung verbunden, wenn er sich entweder vom gleichen Gerät oder von einem anderen Gerät aus beim System anmeldet. Wenn die Sitzung eines Benutzers unerwartet durch einen Netzwerk- oder Clientfehler beendet wird, wird der Benutzer getrennt, aber nicht abgemeldet.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Zuordnung der Zwischenablage
</dt> <dd>

Benutzer können Text und Grafiken zwischen Anwendungen, die auf dem lokalen Computer ausgeführt werden, und Anwendungen, die in einer Remotedesktopsitzung ausgeführt werden, und zwischen Sitzungen löschen, kopieren und einfügen.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Druckumleitung
</dt> <dd>

Anwendungen, die in einer Remotedesktopsitzung ausgeführt werden, können auf einem Drucker drucken, der an das Clientgerät angeschlossen ist.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Virtuelle Kanäle
</dt> <dd>

Mithilfe der RDP-Architektur für virtuelle Kanäle können vorhandene Anwendungen erweitert und neue Anwendungen entwickelt werden, um Features hinzuzufügen, die eine Kommunikation zwischen dem Clientgerät und einer Anwendung erfordern, die in einer Remotedesktopsitzung ausgeführt wird.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Fernbedienung
</dt> <dd>

Computersupportmitarbeiter können eine Remotedesktopsitzung anzeigen und steuern. Das Freigeben von Eingabe- und Anzeigegrafiken zwischen zwei Remotedesktopsitzungen bietet einer Supportperson die Möglichkeit, Probleme remote zu diagnostizieren und zu beheben.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Netzwerklastenausgleich
</dt> <dd>

RDP nutzt den Netzwerklastenausgleich (Network Load Balancing, NLB), sofern verfügbar.

</dd> </dl>

Darüber hinaus enthält RDP die folgenden Features:

-   Unterstützung für 24-Bit-Farben.
-   Verbesserte Leistung bei DFÜ-Verbindungen mit niedriger Geschwindigkeit durch reduzierte Bandbreite.
-   Smartcard-Authentifizierung über Remotedesktopdienste.
-   Tastaturhooking. Die Möglichkeit, spezielle Windows Tastenkombinationen im Vollbildmodus an den lokalen Computer oder an einen Remotecomputer weiterzuleiten.
-   Sound, Laufwerk, Anschluss und Netzwerkdruckerumleitung. Sounds, die auf dem Remotecomputer auftreten, sind auf dem Clientcomputer zu hören, auf dem der RDC-Client ausgeführt wird, und lokale Clientlaufwerke sind für die Remotedesktopsitzung sichtbar.

 

 