---
title: Bluetooth und WSALookupServiceEnd
description: Bluetooth verwendet die WSALookupServiceEnd-Funktion, um eine Abfrage zu beenden, die in einem vorherigen Aufruf von wsalookupservicebegin initiiert wurde, und möglicherweise in nachfolgenden Aufrufen von WSALookupServiceNext erweitert wurde.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth und WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948827"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth und WSALookupServiceEnd

Bluetooth verwendet die [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) -Funktion, um eine Abfrage zu beenden, die in einem vorherigen Aufruf von [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)initiiert wurde, und möglicherweise in nachfolgenden Aufrufen von [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)erweitert wurde. Der **WSALookupServiceEnd** -Befehl beendet die Abfrage und bereinigt den Kontext.

Die Schritte für die Geräte Anfrage und die Dienst Ermittlung in Bluetooth sind ausreichend verschieden, um eine separate Behandlung zu verdienen. Weitere Informationen zu Bluetooth und der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion für Geräte Anfragen finden Sie unter [Bluetooth und wsalookupservicebegin für die Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). Weitere Informationen zu Bluetooth und der **wsalookupservicebegin** -Funktion für die Dienst Ermittlung finden Sie unter [Bluetooth und wsalookupservicebegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin für Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin für die Dienst Ermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**herzustellen**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 