---
title: WinINet im Vergleich zu WinHTTP
description: Erfahren Sie, wie Sie zwischen WinInet und WinHTTP wählen. Lesen Sie einen Vergleich der Features, und lesen Sie verwandte Themen.
ms.assetid: 77386b54-2c86-4a30-8c4c-88d5f15313d7
keywords:
- WinINet im Vergleich zu WinHTTP
ms.topic: article
ms.date: 02/22/2019
ms.openlocfilehash: 8ced80dd048559fee483e8cf121918eed75fc462
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118795"
---
# <a name="wininet-vs-winhttp"></a>WinINet im Vergleich zu WinHTTP

Mit einigen Ausnahmen ist [WinINet](portal.md) eine Obermenge von [WinHTTP.](/windows/desktop/WinHttp/winhttp-start-page) Wenn Sie zwischen den beiden auswählen, sollten Sie WinINet verwenden, es sei denn, Sie planen die Ausführung in einem dienst- oder dienstspezifischen Prozess, der Identitätswechsel und Sitzungsisolation erfordert.

## <a name="comparison-of-features"></a>Vergleich der Features

| Funktion | Wininet | WinHTTP |
|-|-|-|
| **Anmeldeinformationscache** Ermöglicht allen integrierten Anwendungen in Windows Internet Explorer automatisches Erhalten von Anmeldeinformationen. Außerdem kann eine Anwendung, die außerhalb von Internet Explorer, die Anmeldeinformationen für den Server nur einmal auffordern/angeben. Ab dann werden die Anforderungen automatisch. | Ja | Nein |
| **Eingabeaufforderung für Anmeldeinformationen** Stellt eine API bereit, mit der der aufrufende Code den Benutzer zur Eingabe von Anmeldeinformationen auffordern kann. | Ja | Nein |
| **FTP** | Ja | Nein |
| **Autodial/RAS-Unterstützung** Dies ist eine Legacyfunktion. Verwenden [Sie stattdessen Remotezugriff.](/windows/desktop/RRAS/portal) | Ja | Nein |
| **Zonen** Automatische Integration in Internet Explorer Sicherheitszonen. | Ja | Nein |
| **IDNA-Unterstützung** Integrierte Unterstützung für IDNA RFC/Punycode. | Ja | Ja |
| **Cookie-JAR-APIs** Persistente und nicht persistente Cookies werden unterstützt. Jede Anwendung oder jedes Skript kann dies verwenden, um die gleichen Cookies wie der Browser zu sehen. | Ja | Nein |
| **IE-Unterstützung im geschützten Modus** | Ja | Nein |
| **Dekomprimierungsunterstützung** Unterstützung für das gzip- und deflate-Komprimierungsschema. | Ja | Ja |
| **Unterstützung für blockierte Uploads** Der Clientcode muss die Blockierung ausführen. | Nein | Ja |
| **SOCKS v4-Unterstützung** Enthält nicht v4a oder v5. | Ja | Nein |
| **Bidirektionales Senden und Empfangen** | Nein | Nein |
| **Überlappende E/A** | Nein | Nein |
| **Dateischemaunterstützung** Nützlich für Proxyskripts mit einem Dateischema. | Ja | Nein |
| **InternetOpenUrl** Vereinfachter Code zum Öffnen einer URL. | Ja | Nein |
| **Unterstützung von Diensten** Kann über einen Dienst oder ein Dienstkonto ausgeführt werden. | Nein | Ja |
| **Sitzungsisolation** Separate Sitzungen wirken sich nicht gegenseitig aus. | Nein | Ja |
| **Identitätswechsel** Unterstützt das Aufrufen von , während der Thread die Identität eines anderen Benutzers anspricht. | Nein | Ja |

## <a name="related-topics"></a>Zugehörige Themen

* [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
* [Wininet](/windows/desktop/WinInet/about-wininet)