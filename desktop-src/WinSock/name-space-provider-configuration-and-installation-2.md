---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Konfiguration und Installation von Namespace Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c87de8fee4ccaea0fb6978037e1e41684b56267
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526141"
---
# <a name="namespace-provider-configuration-and-installation"></a>Konfiguration und Installation von Namespace Anbietern

-   [**Wscenablensprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**Wscinstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**Wscinstallnamespaceex**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**Wscuninstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**Wscschreitenamespaceorder**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Wie bereits erwähnt, muss die Installationsanwendung für einen Namespace Anbieter [**wscinstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) oder [**wscinstallnamespaceex**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) aufrufen, um sich bei der Ws2 \_ -32.dll zu registrieren und statische Konfigurationsinformationen bereitzustellen. Der Namespace Anbieter muss [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) oder [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)aufgerufen werden, um auf einer 64-Bit-Plattform im 32-Bit-Katalog zu installieren. Die Ws2 \_ -32.dll verwendet diese Informationen, um die Routing Funktion und die Implementierung von [**wsaenumnamespaceproviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) und [**wsaenumnamespaceprovidersex**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa)auszuführen. Die [**wscuninstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) -Funktion wird verwendet, um einen Namespace Anbieter aus der Registrierung zu entfernen, und die [**wscenablensprovider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) -Funktion wird verwendet, um einen Anbieter zwischen den aktiven und inaktiven Zuständen zu wechseln.

Auf einer 64-Bit-Plattform sind [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) und [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) ähnliche Funktionen für den Umgang mit dem 32-Bit-Katalog.

Die Ergebnisse dieser drei Vorgänge sind für Anwendungen, die zurzeit geladen sind und ausgeführt werden, nicht sichtbar. Nur Anwendungen, die nach dem Ausführen dieser Vorgänge ausgeführt werden, sind von diesen betroffen.

Diese Architektur unterstützt explizit die Instanziierung von mehreren Namespace Anbietern innerhalb einer einzelnen dll. jedem solchen Anbieter muss jedoch ein eindeutiger Namespace Anbieter Bezeichner (GUID) zugeordnet sein, und für jede Instanziierung muss ein separater [**wscinstallnamespace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) -oder [**wscinstallnamespaceex**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) -Befehl vorhanden sein (auf 64-Bit-Plattformen sind die Funktionen für den 32-Bit-Katalog [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) und [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)). Ein solcher Anbieter kann ermitteln, welche Instanziierung aufgerufen wird, da der Namespace Anbieter-Bezeichner (NSP) in jeder NSP-Funktion als Parameter angezeigt wird.

 

 



