---
title: Verwenden der Remotedesktop Virtualization-API
description: Entwickler können diese API verwenden, um die Logik anzupassen, die RD-Verbindungsbroker verwendet, um das beste Ziel für eine eingehende Client Verbindung zu ermitteln.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mit der Virtualisierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390435"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Verwenden der Remotedesktop Virtualization-API

Der Rollen Dienst "Terminaldienste-Sitzungs Verzeichnis (TS-Sitzungs Verzeichnis)" ermöglicht Terminal Servern das Speichern von Benutzer-und Sitzungsinformationen in einer Datenbank, die als Sitzungs Verzeichnis bezeichnet wird. Wenn ein Benutzer eine Verbindung mit einem Terminal Server in einer Farm herstellt, bestimmt das Terminaldienst Sitzungs Verzeichnis, ob der Benutzer bereits eine Sitzung auf einem Terminal Server ausgeführt hat. ist dies der Fall, wird der Benutzer an diesen Terminal Server umgeleitet.

In Windows Server 2008 wurde der Rollen Dienst "Terminal Dienste-Sitzungs Verzeichnis" erweitert und umbenannt in "Terminal Dienste-Sitzungs Broker" (Terminal Dienste-Sitzungs Broker). Zusätzlich zur Verwaltung eines Verzeichnisses vorhandener Sitzungen kann der terminaldienstesitzungbroker auch eingehende Verbindungen Broker. Wenn der Terminaldienst-Sitzungs Broker eine eingehende Verbindung von einem Benutzer empfängt, überprüft er seine Datenbank, um zu bestimmen, ob der Benutzer über eine vorhandene Sitzung auf einem Terminal Server verfügt. Wenn dies der Fall ist, leitet der Terminal Server-Sitzungs Broker die Verbindung an denselben Terminal Server um. Andernfalls ermittelt der Terminal Server-Sitzungs Broker, welcher Terminal Server über die geringsten Verbindungen verfügt und leitet die Verbindung zu diesem Server um.

Ab Windows Server 2008 hat Microsoft auch eine öffentliche API (Application Programming Interface) für die Überwachung und Interaktion mit Sitzungen auf Terminalservern veröffentlicht. Diese API wird in [Remotedesktopverbindung Broker-Plug-in-Referenz](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)beschrieben. Mithilfe dieser API können Entwickler benutzerdefinierte Richtlinien-Plug-ins erstellen, die die standardmäßige Umleitungs Logik des TS-Sitzungs Brokers überschreiben. Die benutzerdefinierten Plug-Ins können Sitzungen an Terminal Server sowie an virtuelle Maschinen, virtuelle Desktops, Blatt Server und physische Desktops umleiten.

In Windows Server 2008 R2 wurde die Architektur von Remotedesktopverbindung Broker (RD-Verbindungsbroker) (ehemals TS-Sitzungs Broker) erweitert, um Verbindungen mit virtuellen Maschinen zu unterstützen. Die neue Architektur unterstützt die Sitzungsverwaltung für virtuelle Computer über die Remotedesktop Virtualization-API. Entwickler können diese API verwenden, um die Logik anzupassen, die RD-Verbindungsbroker verwendet, um das beste Ziel für eine eingehende Client Verbindung zu ermitteln.

Remotedesktop virtualisierungsapi bietet Entwicklern verschiedene Vorteile:

-   Die Schnittstellen für die Arbeit mit physischen Terminalservern ähneln denen für das Arbeiten mit virtuellen Computern.
-   Entwickler können den gesamten oder einen Teil der Standard Umleitungs Logik ersetzen. Entwickler können auf dem Code aufbauen, der im Lieferumfang des Produkts enthalten ist, und nicht alles von Grund auf neu schreiben müssen.
-   Auf dem Verwaltungs Server oder innerhalb der Sitzung ist kein zusätzlicher Verwaltungs-Agent erforderlich.
-   TS-Sitzungs Broker-Plug-ins, die zur Verwendung mit Windows Server 2008 entwickelt wurden, werden weiterhin unterstützt.
-   Die API ermöglicht Entwicklern außerdem das Erstellen von Benutzeroberflächen für die Verwaltung von Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern (früher als "Terminal Server" bezeichnet) und virtuellen Computern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Remotedesktop virtualisierungsapi](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Remotedesktopverbindung Broker-Plug-in-Referenz](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 