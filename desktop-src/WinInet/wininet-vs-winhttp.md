---
title: WinInet im Vergleich zu WinHTTP
description: Mit einigen Ausnahmen ist WinInet eine supermenge von WinHTTP. Bei der Auswahl zwischen den beiden sollten Sie WinInet verwenden, es sei denn, Sie planen die Durchführung innerhalb eines Dienst-oder Dienst ähnlichen Prozesses, der Identitätswechsel und Sitzungs Isolation erfordert.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinInet im Vergleich zu WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: c4d161992c2202505e8c84c660ca1edc92cc7993
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339900"
---
# <a name="wininet-vs-winhttp"></a>WinInet im Vergleich zu WinHTTP

Mit einigen Ausnahmen ist [WinInet](portal.md) eine supermenge von [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page). Bei der Auswahl zwischen den beiden sollten Sie WinInet verwenden, es sei denn, Sie planen die Durchführung innerhalb eines Dienst-oder Dienst ähnlichen Prozesses, der Identitätswechsel und Sitzungs Isolation erfordert.

## <a name="comparison-of-features"></a>Vergleich der Features

| Funktion | WinInet | WinHTTP |
|-|-|-|
| Anmelde Informations **Cache** Ermöglicht allen integrierten Anwendungen in Windows Internet Explorer, Anmelde Informationen automatisch zu erhalten. Außerdem kann eine Anwendung, die außerhalb von Internet Explorer ausgeführt wird, die Anmelde Informationen für den Server nur einmal auffordern bzw. angeben. Ab werden die Anforderungen automatisch angezeigt. | ja | nein |
| Eingabe **Aufforderung** für Anmelde Informationen Stellt eine API bereit, die es dem aufrufenden Code ermöglicht, den Benutzer zur Eingabe von Anmelde Informationen aufzufordern. | ja | nein |
| **FTP** | ja | nein |
| **Unterstützung für AutoDial/RAS** Dabei handelt es sich um Legacy Funktionen. Verwenden Sie stattdessen den [Remote Zugriff](/windows/desktop/RRAS/portal) . | ja | nein |
| **Zonen** Automatische Integration in Internet Explorer-Sicherheitszonen. | ja | nein |
| **IDNA-Unterstützung** Integrierte Unterstützung für IDNA RFC/Punycode. | ja | ja |
| **Cookie-jar-APIs** Persistente und nicht persistente Cookies werden unterstützt. Alle Anwendungen oder Skripts können dies verwenden, um dieselben Cookies wie der Browser anzuzeigen. | ja | nein |
| **Unterstützung für den geschützten Modus** | ja | nein |
| **Dekomprimierungsunterstützung** Unterstützung für das gzip-und Deflate-Komprimierungs Schema. | ja | ja |
| **Unterstützung** für aufgeteilte Uploads Der Client Code muss die Segmentierung ausführen. | nein | ja |
| **Unterstützung für SOCKS v4** Umfasst weder V4A noch V5. | ja | nein |
| **Bidirektionales senden und empfangen** | nein | nein |
| **Überlappende e/a** | nein | nein |
| **Datei Schema Unterstützung** Nützlich für Proxy Skripts mit einem Datei Schema. | ja | nein |
| **InternetOpenUrl** Vereinfachter Code zum Öffnen einer URL. | ja | nein |
| **Unterstützung von Diensten** Kann über einen Dienst oder ein Dienst Konto ausgeführt werden. | nein | ja |
| **Sitzungs Isolation** Separate Sitzungen wirken sich nicht gegenseitig aus. | nein | ja |
|  Identitätswechsel Unterstützt das Aufrufen von, während der Thread die Identität eines anderen Benutzers annimmt. | nein | ja |

## <a name="related-topics"></a>Zugehörige Themen

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [WinInet](/windows/desktop/WinInet/about-wininet)