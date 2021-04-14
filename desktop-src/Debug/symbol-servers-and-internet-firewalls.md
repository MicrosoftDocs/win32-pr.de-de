---
description: Einige Systeme verwenden Internet Firewalls oder Proxy Server, für die eine Authentifizierung für den gesamten Internet Datenverkehr erforderlich ist.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Symbol Server und Internet Firewalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e2a85a5d0ee2d41e6ffee40bbb275155bdf1e48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523067"
---
# <a name="symbol-server-and-internet-firewalls"></a>Symbol Server und Internet Firewalls

Einige Systeme verwenden Internet Firewalls oder Proxy Server, für die eine Authentifizierung für den gesamten Internet Datenverkehr erforderlich ist. Frühe Versionen des Symbol Servers konnten nicht auf Symbole aus dem Internet zugreifen, es sei denn, das System hat einen Firewallclient verwendet, der die Authentifizierung transparent verarbeitet hat.

Ab dbghelp 6,1 unterstützt der Symbol Server Proxy Server, für die eine solche Authentifizierung erforderlich ist. Der Symbol Server verwendet einen beliebigen Server, der als Standard in den LAN-Einstellungen des Computers konfiguriert ist. Öffnen Sie hierzu in der Systemsteuerung das Element **Internet Optionen** , klicken Sie auf die Registerkarte **Verbindungen** , und klicken Sie dann auf **LAN-Einstellungen**. Dies kann auch über Internet Explorer erfolgen, indem Sie **im Menü Extras** auf **Internetoptionen** klicken. Der Symbol Server wurde unter Verwendung von Basic-und Challenge-Response-Methoden für die Authentifizierung auf zahlreichen Marken von Proxy Servern getestet.

Um einen bestimmten Proxy Server zu definieren, der von Symbol Server verwendet werden soll, legen Sie die \_ NT \_ \_ -Symbol Proxy-Umgebungsvariable auf den Namen (oder die IP-Adresse) des Proxy Servers und dann auf die Portnummer fest. Trennen Sie die beiden Werte durch einen Doppelpunkt. Beispiel:

**festlegen \_ NT- \_ Symbol \_ Proxy =**_myProxyServer_*_: 80_*

Wenn Sie den WinDbg-Debugger verwenden, konfigurieren Sie den Symbol Pfad so, dass er auf den Symbol Speicher verweist, den Sie verwenden möchten. Der einzige Unterschied besteht darin, dass im System ein Dialogfeld angezeigt wird, in dem Sie Ihre Benutzer-ID und das Kennwort eingeben müssen, um Sie an den Proxy Server zu übergeben. Wenn Sie falsche Informationen eingeben, wird das Dialogfeld erneut angezeigt. Wenn Sie auf die Schaltfläche **Abbrechen** klicken, wird das Dialogfeld geschlossen, und der Symbol Server wird für die Verwendung über das Internet deaktiviert.

Wenn Sie die neuesten Versionen von cdb.exe oder ntsd.exe verwenden, ist diese Funktion standardmäßig deaktiviert. Sie können diese Funktion jedoch wie folgt mithilfe des Befehls "! SYM Extension" aktivieren oder deaktivieren:

-   So aktivieren Sie die Eingabeaufforderung für Benutzer-ID und Kennwort: **! SYM-Eingabe Aufforderungen**.
-   So deaktivieren Sie die Eingabeaufforderung für Benutzer-ID und Kennwort: **! SYM fordert aus**.

Wenn Sie die Eingabeaufforderung aktivieren, müssen Sie Symbole mit dem Befehl. Reload erneut laden.

Die dbghelp-API wurde erweitert, um diese Änderungen zu unterstützen. Die [**symbolserversetoptions**](/previous-versions//ms680676(v=vs.85)) -Funktion unterstützt die ssrvopt- \_ Proxy Option. Wenn der Data-Parameter **null** ist, wird der in den **Internet Optionen** definierte Standard Proxy verwendet. Andernfalls wird eine NULL terminierte Zeichenfolge mit Angabe des Namens und der Portnummer des Proxy Servers übermittelt. Der Name und der Port werden wie folgt durch einen Doppelpunkt getrennt: *myProxyServer*: 80. Die [**symsettoptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) -Funktion unterstützt die Option "symopt \_ No \_ Aufforderungen". Dadurch werden alle Eingabe Aufforderungen für die Validierung vom Symbol Server deaktiviert.

 

 
