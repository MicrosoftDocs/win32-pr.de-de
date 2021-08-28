---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Konfiguration und Installation des Namespaceanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d420e9322d1d39816cdb9b3812b23b1e7e72e945c3d0f2ef95e7edff77f12276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121370"
---
# <a name="namespace-provider-configuration-and-installation"></a>Konfiguration und Installation des Namespaceanbieters

-   [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**WSCWriteNameSpaceOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Wie bereits erwähnt, muss die Installationsanwendung für einen Namespaceanbieter [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) oder [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) aufrufen, um sich beim Ws2-32.dll zu registrieren \_ und statische Konfigurationsinformationen anzugeben. Zur Installation im 32-Bit-Katalog auf einer 64-Bit-Plattform muss der Namespaceanbieter [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) oder [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)aufrufen. Die \_ Ws2-32.dll verwendet diese Informationen, um die Routingfunktion und die Implementierung von [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) und [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa)auszuführen. Die [**WSCUnInstallNameSpace-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) wird verwendet, um einen Namespaceanbieter aus der Registrierung zu entfernen, und die [**WSCEnableNSProvider-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) wird verwendet, um einen Anbieter zwischen dem aktiven und dem inaktiven Status umzuschalten.

Auf einer 64-Bit-Plattform sind [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) und [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) ähnliche Funktionen für den Umgang mit dem 32-Bit-Katalog.

Die Ergebnisse dieser drei Vorgänge sind für Anwendungen, die derzeit geladen und ausgeführt werden, nicht sichtbar. Nur Anwendungen, die nach dem Auftreten dieser Vorgänge mit der Ausführung beginnen, sind von ihnen betroffen.

Diese Architektur unterstützt explizit die Instanziierung mehrerer Namespaceanbieter innerhalb einer einzelnen DLL. Jedem Anbieter muss jedoch ein eindeutiger Namespaceanbieterbezeichner (GUID) zugeordnet sein, und für jede Instanziierung muss ein separater Aufruf von [**WSCInstallNameSpaceSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) oder [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) erfolgen (auf 64-Bit-Plattformen sind die Funktionen für den 32-Bit-Katalog [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) und [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)). Ein solcher Anbieter kann bestimmen, welche Instanziierung aufgerufen wird, da der Namespaceanbieterbezeichner (NSP) in jeder NSP-Funktion als Parameter angezeigt wird.

 

 



