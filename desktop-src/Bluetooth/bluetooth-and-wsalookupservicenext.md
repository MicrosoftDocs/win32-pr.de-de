---
title: Bluetooth und WSALookupServiceNext
description: Bluetooth verwendet die WSALookupServiceNext-Funktion, um Abfragen zu erfüllen, die in einem vorherigen Aufruf von WSALookupServiceBegin angegeben wurden.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth und WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010392"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth und WSALookupServiceNext

Bluetooth verwendet die [**WSALookupServiceNext-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) um Abfragen zu erfüllen, die in einem vorherigen Aufruf von [**WSALookupServiceBegin angegeben wurden.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) Die Ergebnisse der **WSALookupServiceNext-Funktion** werden durch Einstellungen bestimmt, die in der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) festgelegt sind, die im ersten **WSALookupServiceBegin-Funktionsaufruf** übergeben wird.

Die Schritte für die Geräteanfrage und dienstermittlung in Bluetooth unterscheiden sich ausreichend, um eine separate Behandlung zu ersingen. Weitere Informationen zu Bluetooth und der [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) für Geräteanfragen finden Sie unter [Bluetooth und WSALookupServiceBegin für Geräteanfragen.](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) Weitere Informationen zu Bluetooth und der **WSALookupServiceBegin-Funktion** für die Dienstermittlung finden Sie unter [Bluetooth und WSALookupServiceBegin für die Dienstermittlung.](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin für die Geräteanfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin für die Dienstermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[**\_BTH-ABFRAGEDIENST \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**Verbinden**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 