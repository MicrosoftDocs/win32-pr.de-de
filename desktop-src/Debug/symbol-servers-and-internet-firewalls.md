---
description: Einige Systeme verwenden Internetfirewalls oder Proxyserver, die eine Authentifizierung für den sämtlichen Internetdatenverkehr erfordern.
ms.assetid: b79e9a6f-2ffb-4ec0-ac2d-63e79ecfc26c
title: Symbolserver und Internetfirewalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a998b5bd2aea2685ac060df6ddd8acdcd904c9997a0da8dfbf8fdc636ac90f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004861"
---
# <a name="symbol-server-and-internet-firewalls"></a>Symbolserver und Internetfirewalls

Einige Systeme verwenden Internetfirewalls oder Proxyserver, die eine Authentifizierung für den sämtlichen Internetdatenverkehr erfordern. Frühe Versionen des Symbolservers konnten nur dann auf Symbole aus dem Internet zugreifen, wenn das System einen Firewallclient verwendet hat, der die Authentifizierung transparent verarbeitet hat.

Ab Dbghelp 6.1 unterstützt der Symbolserver Proxyserver, die eine solche Authentifizierung erfordern. Der Symbolserver verwendet den Server, der in den LAN-Einstellungen des Computers als Standard konfiguriert ist. Um dies zu finden, öffnen Sie das **Element Internetoptionen** in Systemsteuerung, klicken Sie auf die **Registerkarte** Verbindungen und dann **auf LAN Einstellungen.** Dies kann auch über Internet Explorer durch Klicken auf **Internetoptionen** im Menü **Extras** erfolgen. Der Symbolserver wurde auf vielen Marken von Proxyservern getestet, indem sowohl einfache als auch Challenge-Response-Methoden der Authentifizierung verwendet werden.

Um einen bestimmten Proxyserver für die Verwendung durch den Symbolserver zu definieren, legen Sie die NT SYMBOL PROXY-Umgebungsvariable auf den Namen (oder die IP-Adresse) des Proxyservers gefolgt von der \_ \_ \_ Portnummer fest. Trennen Sie die beiden Werte durch einen Doppelpunkt. Beispiel:

**set \_ NT \_ SYMBOL \_ PROXY=**_myproxyserver_*_:80_*

Wenn Sie den windbg-Debugger verwenden, konfigurieren Sie den Symbolpfad so, dass er auf den Symbolspeicher zeigt, den Sie verwenden möchten. Der einzige Unterschied besteht in der Anzeige eines Dialogfelds, in dem Sie Ihre Benutzer-ID und ihr Kennwort eingeben müssen, um sie an den Proxyserver zu übergeben. Wenn Sie falsche Informationen eingeben, wird das Dialogfeld erneut angezeigt. Wenn Sie auf die **Schaltfläche Abbrechen** klicken, wird das Dialogfeld verworfen, und der Symbolserver wird für die Verwendung über das Internet deaktiviert.

Wenn Sie die neuesten Versionen von cdb.exe oder ntsd.exe verwenden, ist diese Funktion standardmäßig deaktiviert. Sie können diese Funktionalität jedoch wie folgt mithilfe des Befehls !sym extension aktivieren oder deaktivieren:

-   So aktivieren Sie die Eingabeaufforderung für Benutzer-ID und Kennwort: **!sym fordert auf.**
-   So deaktivieren Sie die Eingabeaufforderung für Benutzer-ID und Kennwort: **!sym fordert aus.**

Wenn Sie die Eingabeaufforderung aktivieren, müssen Sie Symbole mit dem Befehl .reload erneut laden.

Die DbgHelp-API wurde erweitert, um diese Änderungen zu unterstützen. Die [**SymbolServerSetOptions-Funktion**](/previous-versions//ms680676(v=vs.85)) unterstützt die Option SSRVOPT \_ PROXY. Wenn der Datenparameter **NULL ist,** wird der unter **Internetoptionen definierte Standardproxy** verwendet. Andernfalls wird eine auf 0 (null) beendete Zeichenfolge übergeben, die den Namen und die Portnummer des Proxyservers angibt. Name und Port werden wie folgt durch einen Doppelpunkt getrennt: *myproxyserver*:80. Die [**SymSetOptions-Funktion**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) unterstützt die SYMOPT \_ NO \_ PROMPTS-Option. Dadurch werden alle Überprüfungsaufforderungen vom Symbolserver deaktiviert.

 

 
