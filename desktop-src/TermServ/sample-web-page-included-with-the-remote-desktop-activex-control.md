---
title: Beispiel Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten ist
description: Eine Beispiel Webseite (Default.htm) befindet sich im Verzeichnis, in dem Remotedesktop-Webverbindung installiert ist.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec07ee86dcb5d10dc289e8095c83771ebe9a8b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310243"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Beispiel Webseite, die im Remotedesktop ActiveX-Steuerelement enthalten ist

Wenn Sie das Remotedesktop ActiveX-Steuerelement von Remotedesktop-Webverbindung installieren, wird eine Beispiel Webseite (Default.htm) in das Verzeichnis kopiert, in dem Remotedesktop-Webverbindung installiert ist. Diese Seite kann unverändert oder angepasst werden, um den Anforderungen eines Benutzers oder einer Organisation gerecht zu werden.

Die Beispiel Webseite muss auf einem Webserver installiert sein, auf dem Windows Server und Internet Information Server 4,0 oder höher ausgeführt werden. Außerdem sollte der Browser auf dem Client Computer Internet Explorer Version 4,0 oder höher sein. Weitere Informationen finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

Default.htm ist eine Standard Anmelde Webseite, die Verbindungsinformationen vom Benutzer sammelt. Die Anmeldeseite enthält ein Pflichtfeld, in das der Benutzer den Namen des Remotedesktop-Sitzungshost (RD-Sitzungshost) oder Remote Computers eingibt, mit dem eine Verbindung hergestellt werden soll. Die Anmeldeseite enthält auch optionale Felder für Bildschirmgröße und Benutzer Anmelde Informationen, einschließlich Benutzername und Domäne.

Nachdem Sie die Benutzerdaten gesammelt haben, Default.htm Sie an das Remotedesktop ActiveX-Steuerelement (Msrdp. ocx) weitergeleitet, um eine Remote Desktop Sitzung zu initiieren. Die Schritte zum Initiieren der Sitzung lauten wie folgt:

1.  Falls erforderlich, lädt Internet Explorer die CAB-Datei herunter und installiert Sie auf dem Computer des Benutzers.
2.  Der Benutzer gibt den voll qualifizierten Domänen Namen oder die IP-Adresse des Remote Computers in das entsprechende Feld ein.

    -   Der Benutzer kann optional eine Bildschirmgröße für die Verbindung angeben. Wenn der Benutzer keine Bildschirmgröße angibt, wird die Sitzung im Vollbildmodus geöffnet, wenn sich der Benutzer in einer vertrauenswürdigen URL-Sicherheitszone befindet. Andernfalls wird die Sitzung im Fenstermodus geöffnet.
    -   Der Benutzer kann optional automatische Anmelde Informationen (Benutzername, Domäne) für die Remote Sitzung angeben.

3.  Wenn der Benutzer auf die Schaltfläche **verbinden** klickt, übergibt Default.htm die vom Benutzer bereitgestellten Daten als Parameter an das Remotedesktop ActiveX-Steuerelement.
4.  Der Remote Desktop wird im Browserfenster oder im Vollbildmodus geöffnet, wie er vom Benutzer angegeben wird.

Wenn Default.htm zum ersten Mal mit Internet Explorer geöffnet wird, wird ein Dialogfeld angezeigt, in dem der Benutzer die Möglichkeit bietet, das Remotedesktop ActiveX-Steuerelement (Msrdp. ocx) herunterzuladen. Das Dialogfeld wird unter den folgenden Bedingungen angezeigt:

-   Der Computer, auf den die Webseite zugegriffen hat, verfügt nicht über eine vollständige Installation des Remotedesktop-Webverbindung Clients (oder des Remotedesktopdienste erweiterter Client) mit Webunterstützung.
-   Die installierte Version der CAB-Datei auf dem Client Computer ist älter als die Version auf der Default.htm Webseite.

Die Größe der Remote Desktop Sitzung, die im Browserfenster angezeigt wird, entspricht der auf der Default.htm Webseite angegebenen Größe. Um die Bildschirmgröße zu ändern, muss der Benutzer die Verbindung mit der Sitzung trennen, zur Default.htm Webseite zurückkehren und die Verbindungsinformationen bearbeiten. Wenn keine Bildschirmgröße angegeben wurde, wird die Sitzung im Browserfenster im Standard Vollbildmodus geöffnet. Bei dieser Lösung wird der Remote Desktop entsprechend den vollständigen Dimensionen des Benutzer Bildschirms erweitert, und die Browser Symbolleisten und Fenster Frames von Internet Explorer werden nicht angezeigt. Wie bei der vollständigen Remotedesktopverbindung Client kann der Benutzer zwischen dem Vollbildmodus und dem Fenstermodus wechseln, indem er die [Tasten](terminal-services-shortcut-keys.md) Kombination für den Vollbildmodus (Strg + Alt + Pause) drückt.

Aus Sicherheitsgründen sind einige Optionen, die im Remotedesktopdienste-Verbindungs-Manager verfügbar sind, im Remotedesktop ActiveX-Steuerelement auf bestimmte Internet Explorer-URL-Sicherheitszonen beschränkt. Weitere Informationen zu diesen Optionen und zum Angeben eines Programms für die Verbindungs Herstellung finden Sie unter [Bereitstellen der RDP-Client Sicherheit](providing-for-rdp-client-security.md) .

 

 




