---
title: Verwenden der Remotedesktop-Virtualisierungs-API
description: Entwickler können diese API verwenden, um die Logik anzupassen, die der RD-Verbindungsbroker verwendet, um das beste Ziel für eine eingehende Clientverbindung zu bestimmen.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste mithilfe der Virtualisierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7075c3a0cfcabc2df0dcb8438b7de5a748eb2b0340e26bf3d1e51afdb182f81e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423630"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Verwenden der Remotedesktop-Virtualisierungs-API

Mit dem Rollendienst Terminal services Session Directory (TS Session Directory) können Terminalserver Benutzer- und Sitzungsinformationen in einer Datenbank speichern, die als Sitzungsverzeichnis bezeichnet wird. Wenn ein Benutzer eine Verbindung mit einem Terminalserver in einer Farm herstellt, bestimmt TS Session Directory, ob der Benutzer bereits über eine Sitzung verfügt, die auf einem Terminalserver ausgeführt wird, und leitet den Benutzer in diesem Falle an diesen Terminalserver um.

In Windows Server 2008 wurde der Rollendienst "TS-Sitzungsverzeichnis" erweitert und in Terminal services Session Broker (TS Session Broker) umbenannt. Zusätzlich zur Verwaltung eines Verzeichnisses vorhandener Sitzungen kann der TS-Sitzungsbroker auch eingehende Verbindungen vermitteln. Wenn der TS-Sitzungsbroker eine eingehende Verbindung von einem Benutzer empfängt, überprüft er seine Datenbank, um zu ermitteln, ob der Benutzer über eine vorhandene Sitzung auf einem Terminalserver verfügt. Wenn ja, leitet der TS-Sitzungsbroker die Verbindung an denselben Terminalserver um. Andernfalls bestimmt der TS-Sitzungsbroker, welcher Terminalserver über die wenigsten Verbindungen verfügt, und leitet die Verbindung an diesen Server um.

Ab Windows Server 2008 hat Microsoft auch eine öffentliche Api (Application Programming Interface) für die Überwachung und Interaktion mit Sitzungen auf Terminalservern veröffentlicht. Diese API wird in [Remotedesktopverbindung Broker-Plug-In-Referenz](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)beschrieben. Mit dieser API können Entwickler benutzerdefinierte Richtlinien-Plug-Ins erstellen, die die Standardumleitungslogik des TS-Sitzungsbrokers überschreiben. Die benutzerdefinierten Plug-Ins können Sitzungen an Terminalserver sowie an virtuelle Computer, virtuelle Desktops, Blattserver und physische Desktops umleiten.

In Windows Server 2008 R2 wurde die Architektur von Remotedesktopverbindung Broker (RD-Verbindungsbroker) (früher als TS-Sitzungsbroker bezeichnet) erweitert, um Verbindungen mit virtuellen Computern zu unterstützen. Die neue Architektur unterstützt die Sitzungsverwaltung für virtuelle Computer über die Remotedesktop-Virtualisierungs-API. Entwickler können diese API verwenden, um die Logik anzupassen, die der RD-Verbindungsbroker verwendet, um das beste Ziel für eine eingehende Clientverbindung zu bestimmen.

Remotedesktop-Virtualisierungs-API bietet Entwicklern mehrere Vorteile:

-   Die Schnittstellen für die Arbeit mit physischen Terminalservern ähneln denen für die Arbeit mit virtuellen Computern.
-   Entwickler können die Standardumleitungslogik ganz oder teilweise ersetzen. Entwickler können auf dem Code aufbauen, der mit dem Produkt ausgeliefert wird, und müssen nicht alles von Grund auf neu schreiben.
-   Auf dem Verwaltungsserver oder innerhalb der Sitzung ist kein zusätzlicher Verwaltungs-Agent erforderlich.
-   TS-Sitzungsbroker-Plug-Ins, die für die Verwendung mit Windows Server 2008 entwickelt wurden, werden weiterhin unterstützt.
-   Die API ermöglicht Entwicklern auch das Erstellen von Benutzeroberflächen für die Verwaltung von Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern (früher als "Terminalserver" bezeichnet) und virtuellen Computern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Remotedesktop Virtualization API Reference (Referenz zur Virtualisierungs-API)](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Referenz zum Remotedesktopverbindung Broker-Plug-In](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 