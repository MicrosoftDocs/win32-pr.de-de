---
title: Beispielwebseite im Remotedesktop ActiveX-Steuerelement
description: Eine Beispielwebseite (Default.htm) befindet sich im Verzeichnis, in dem Remotedesktop-Webverbindung installiert ist.
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c175bafe1ebde3367c20529a6d76d7933a42f343de56216649735c942105aa65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058538"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>Beispielwebseite im Remotedesktop ActiveX-Steuerelement

Wenn Sie das Remotedesktop ActiveX-Steuerelement von Remotedesktop-Webverbindung installieren, wird eine Beispielwebseite (Default.htm) in das Verzeichnis kopiert, in dem Remotedesktop-Webverbindung installiert ist. Diese Seite kann in der vorliegenden Form ausgeführt oder an die Anforderungen eines Benutzers oder einer Organisation angepasst werden.

Die Beispielwebseite muss auf einem Webserver installiert sein, auf dem Windows Server und Internetinformationsserver 4.0 oder höher ausgeführt wird. Außerdem sollte der Browser auf dem Clientcomputer Internet Explorer Version 4.0 oder höher sein. Weitere Informationen finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

Default.htm ist eine Standardanmeldewebseite, die Verbindungsinformationen vom Benutzer sammelt. Die Anmeldeseite enthält ein Pflichtfeld, in das der Benutzer den Namen des Remotedesktop-Sitzungshost (RD-Sitzungshost) Servers oder Remotecomputers eingibt, mit dem eine Verbindung hergestellt werden soll. Die Anmeldeseite enthält auch optionale Felder für die Bildschirmgröße und Benutzeranmeldungsinformationen, einschließlich Benutzername und Domäne.

Nach dem Sammeln der Benutzerdaten übergibt Default.htm sie an das Remotedesktop ActiveX-Steuerelement (Msrdp.ocx), um eine Remotedesktopsitzung zu initiieren. Beim Initiieren der Sitzung sind die folgenden Schritte erforderlich:

1.  Bei Bedarf lädt Internet Explorer die .cab-Datei herunter und installiert sie auf dem Computer des Benutzers.
2.  Der Benutzer gibt den vollqualifizierten Domänennamen oder die IP-Adresse des Remotecomputers in das entsprechende Feld ein.

    -   Der Benutzer kann optional eine Bildschirmgröße für die Verbindung angeben. Wenn der Benutzer keine Bildschirmgröße angibt, wird die Sitzung im Vollbildmodus geöffnet, wenn sich der Benutzer in einer vertrauenswürdigen URL-Sicherheitszone befindet. Andernfalls wird die Sitzung im Fenstermodus geöffnet.
    -   Der Benutzer kann optional automatische Anmeldeinformationen (Benutzername, Domäne) für die Remotesitzung bereitstellen.

3.  Wenn der Benutzer auf die Schaltfläche **Verbinden** klickt, übergibt Default.htm die vom Benutzer bereitgestellten Daten als Parameter an das Remotedesktop ActiveX-Steuerelement.
4.  Der Remotedesktop wird im Browserfenster oder im Vollbildmodus geöffnet, wie vom Benutzer angegeben.

Wenn Default.htm zum ersten Mal mit Internet Explorer geöffnet wird, wird ein Dialogfeld angezeigt, in dem der Benutzer das Remotedesktop ActiveX-Steuerelement (Msrdp.ocx) herunterladen kann. Das Dialogfeld wird unter den folgenden Bedingungen angezeigt:

-   Der Computer, der auf die Webseite zugegriffen hat, verfügt nicht über eine vollständige Installation des Remotedesktop-Webverbindung-Clients (oder des Remotedesktopdienste Erweiterter Client) mit Webunterstützung.
-   Die installierte Version der .cab-Datei auf dem Clientcomputer ist älter als die Version auf der Default.htm Webseite.

Die Größe der Remotedesktopsitzung, die im Browserfenster angezeigt wird, entspricht der Größe, die auf der Default.htm Webseite angegeben ist. Um die Bildschirmgröße zu ändern, muss der Benutzer die Verbindung mit der Sitzung trennen, zur Default.htm Webseite zurückkehren und die Verbindungsinformationen bearbeiten. Wenn keine Bildschirmgröße angegeben wurde, wird die Sitzung im Browserfenster im Standard-Vollbildmodus geöffnet. Bei dieser Auflösung wird der Remotedesktop so erweitert, dass er den vollständigen Abmessungen des Bildschirms des Benutzers entspricht und die Internet Explorer Browsersymbolleisten und Fensterrahmen nicht angezeigt werden. Wie beim vollständigen Remotedesktopverbindung Client kann der Benutzer zwischen Vollbild- und Fenstermodus wechseln, indem er die [Tastenkombination](terminal-services-shortcut-keys.md) für den Vollbildmodus (STRG+ALT+BREAK) drückt.

Aus Sicherheitsgründen sind einige Optionen, die in der Remotedesktopdienste Verbindungs-Manager verfügbar sind, im Remotedesktop ActiveX-Steuerelement auf bestimmte Internet Explorer URL-Sicherheitszonen beschränkt. Weitere Informationen zu diesen Optionen und zum Angeben eines Programms, das bei der Verbindung ausgeführt werden soll, finden Sie unter Bereitstellen der [RDP-Clientsicherheit.](providing-for-rdp-client-security.md)

 

 




