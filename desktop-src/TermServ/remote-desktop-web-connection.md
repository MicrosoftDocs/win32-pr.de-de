---
title: Remotedesktop-Webverbindung
description: Remotedesktop-Webverbindung ist eine Webanwendung, die aus einem ActiveX-Steuerelement und einer Beispiel Verbindungs Seite besteht.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Remotedesktop-Webverbindung Remotedesktopdienste
- Remotedesktopprotokoll (RDP) Remotedesktopdienste Remotedesktop-Webverbindung Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338474"
---
# <a name="remote-desktop-web-connection"></a>Remotedesktop-Webverbindung

Remotedesktop-Webverbindung ist eine Webanwendung, die aus einem ActiveX-Steuerelement und einer Beispiel Verbindungs Seite besteht. Wenn Sie Remotedesktop-Webverbindung auf einem Webserver bereitstellen, können Sie mithilfe von Internet Explorer und TCP/IP Client Konnektivität für Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server und andere Computer bereitstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

Listet die Anforderungen für eine Remotedesktop-Webverbindung auf.

</dd> <dt>

[Skript fähige virtuelle Kanäle](scriptable-virtual-channels.md)
</dt> <dd>

Beschreibt Änderungen am Programmiermodell zum Implementieren von virtuellen channelanwendungen, die vom Terminal Dienste-erweiterter Client (Terminal Services, SAC) bereitgestellt werden.

</dd> </dl>

Das Referenzmaterial für Remotedesktop-Webverbindung ist im Abschnitt [Remotedesktop-Webverbindung Reference](remote-desktop-web-connection-reference.md) enthalten.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Implementieren von Skript fähigen virtuellen Kanälen mithilfe von Remotedesktop-Webverbindung](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [Einbetten des Remotedesktop ActiveX-Steuer Elements in eine Webseite](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   [Herunterladen und Verwenden des Remotedesktop ActiveX-Steuer Elements](/previous-versions//aa380808(v=vs.85))
-   [Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md)
-   [Deaktivieren von Remotedesktopdienste Features](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a>Installieren von Remotedesktop-Webverbindung

Mit den folgenden Schritten können Sie das Remotedesktop ActiveX-Steuerelement und die Beispiel Webseite im Verzeichnis "% SystemRoot% Web-Web" installieren \\ \\ . Sie geben die Webseite im Verzeichnis "" von "" auf Ihrem Server frei, z. b. unter https://*myserver*/Tsweb. Das-Steuerelement (Msrdp. ocx) und der Remotedesktop-Webverbindung-Code befinden sich in Msrdp.cab.

**So installieren Sie Remotedesktop-Webverbindung**

1.  Installieren Sie in der Systemsteuerung unter "Software" in der Systemsteuerung unter "Windows-Komponenten hinzufügen/entfernen" Microsoft Internetinformationsdienste (IIS).
2.  Installieren Sie die Unterkomponente des World Wide Web Dienstanbieter von IIS.
3.  Installieren Sie die Remotedesktop-Webverbindung Unterkomponente World Wide Web Dienstanbieter.

Eine Beschreibung der Webseite, die in der Installation von Remotedesktop-Webverbindung enthalten ist, finden Sie unter [Sample-Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten](sample-web-page-included-with-the-remote-desktop-activex-control.md)ist.

 

 