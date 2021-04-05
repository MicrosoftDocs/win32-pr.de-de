---
description: Name der Dienst Abfrage in Windows Sockets (Winsock).
ms.assetid: 94d77f7b-824a-4686-b270-9c662976bbc0
title: Dienst Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951ad1950c0f1d97ab0ca6d06f79ed6ff0180d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042062"
---
# <a name="service-query"></a>Dienst Abfrage

-   [**Nsplookupservicebegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin)
-   [**Nsplookupservicenext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext)
-   [**Nsplookupserviceend**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)

Eine Name Service-Abfrage umfasst eine Reihe von aufrufen: [**nsplookupservicebegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin), gefolgt von einem oder mehreren Aufrufen von [**nsplookupservicenext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) und endet mit einem Aufruf von [**nsplookupserviceend**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend). [**Nsplookupservicebegin**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicebegin) nimmt eine [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur als Eingabe an, um die Abfrage Parameter zusammen mit einem Satz von Flags zu definieren, um eine zusätzliche Kontrolle über den Suchvorgang bereitzustellen. Es wird ein Abfrage Handle zurückgegeben, das in den nachfolgenden Aufrufen von **nsplookupservicenext** und **nsplookupserviceend** verwendet wird.

Der-Namespace-SPI-Client ruft [**nsplookupservicenext**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupservicenext) auf, um Abfrageergebnisse abzurufen, wobei Ergebnisse in einem vom Client bereitgestellten [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Puffer bereitgestellt werden. Der Client ruft weiterhin **nsplookupservicenext** auf, bis der Fehlercode WSA \_ E \_ nicht \_ mehr zurückgegeben wird, was darauf hinweist, dass alle Ergebnisse abgerufen wurden. Die Suche wird dann durch einen [**nsplookupserviceend**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnsplookupserviceend)-Befehl beendet. Die **nsplookupserviceend** -Funktion kann auch verwendet werden, um einen aktuell ausstehenden **nsplookupservicenext** abzubrechen, wenn er von einem anderen Thread aufgerufen wird.

In Windows Sockets 2 werden widersprüchliche Fehlercodes für wsaumomore (10102) und WSA \_ E \_ nicht \_ mehr (10110) definiert. Der Fehlercode wsaeromore wird in einer zukünftigen Version entfernt, und nur WSA \_ E \_ \_ bleibt erhalten. Namespace Anbieter sollten so bald wie möglich auf die Verwendung des WSA \_ E- \_ \_ Fehlercodes umstellen, um die Kompatibilität mit der größtmöglichen Anzahl von Anwendungen aufrechtzuerhalten.

 

 



