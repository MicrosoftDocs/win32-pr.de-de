---
title: Bluetooth und WSALookupServiceEnd
description: Bluetooth verwendet die WSALookupServiceEnd-Funktion, um eine Abfrage zu beenden, die in einem vorherigen Aufruf von WSALookupServiceBegin initiiert und möglicherweise in nachfolgenden Aufrufen von WSALookupServiceNext erweitert wurde.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth und WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd6c893a06fbf586d07e3a2581d1d25626e161508e505dc089d7660267bae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081094"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth und WSALookupServiceEnd

Bluetooth verwendet die [**WSALookupServiceEnd-Funktion,**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) um eine Abfrage zu beenden, die in einem vorherigen Aufruf von [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)initiiert wurde, und wurde möglicherweise in nachfolgenden Aufrufen von [**WSALookupServiceNext erweitert.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) Der Aufruf von **WSALookupServiceEnd** beendet die Abfrage und bereinigt den Kontext.

Die Schritte für die Geräteanfrage und dienstermittlung in Bluetooth unterscheiden sich ausreichend, um eine separate Behandlung zu ersingen. Weitere Informationen zu Bluetooth und der [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) für Geräteanfragen finden Sie unter [Bluetooth und WSALookupServiceBegin für Geräteanfragen.](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) Weitere Informationen zu Bluetooth und der **WSALookupServiceBegin-Funktion** für die Dienstermittlung finden Sie unter [Bluetooth und WSALookupServiceBegin für die Dienstermittlung.](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin für die Geräteanfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin für die Dienstermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
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
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 