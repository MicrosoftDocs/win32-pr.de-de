---
title: Bluetooth und WSALookupServiceNext
description: Bluetooth verwendet die WSALookupServiceNext-Funktion zum Abgleichen von Abfragen, die in einem vorherigen wsalookupservicebegin-Befehl angegeben wurden.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth und WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858283"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth und WSALookupServiceNext

Bluetooth verwendet die [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zum Abgleichen von Abfragen, die in einem vorherigen [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)-Befehl angegeben wurden. Die Ergebnisse der **WSALookupServiceNext** -Funktion werden durch Einstellungen festgelegt, die in der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur festgelegt sind, die im anfänglichen **wsalookupservicebegin** -Funktions aufzurufen ist.

Die Schritte für die Geräte Anfrage und die Dienst Ermittlung in Bluetooth sind ausreichend verschieden, um eine separate Behandlung zu verdienen. Weitere Informationen zu Bluetooth und der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion für Geräte Anfragen finden Sie unter [Bluetooth und wsalookupservicebegin für die Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). Weitere Informationen zu Bluetooth und der **wsalookupservicebegin** -Funktion für die Dienst Ermittlung finden Sie unter [Bluetooth und wsalookupservicebegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin für Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin für die Dienst Ermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
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
</dt> </dl>

 

 