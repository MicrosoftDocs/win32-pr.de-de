---
title: Bluetooth und BLOB
description: Bluetooth verwendet die BLOB-Struktur, um transportspezifische Daten bei Aufrufen der WSASetService- oder WSALookupService\-Funktionen an die WSAQUERYSET-Struktur zu übergeben oder zu empfangen.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth und BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960362e7f6bc6388d3b93bd6e0329e405bdb33ed6e796a5ec5793d402ba0557c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081134"
---
# <a name="bluetooth-and-blob"></a>Bluetooth und BLOB

Bluetooth verwendet die [](/windows/desktop/api/nspapi/ns-nspapi-blob) BLOB-Struktur, um transportspezifische Daten bei Aufrufen der [**WSASetService-**](bluetooth-and-wsasetservice.md) oder **WSALookupService-Funktionen** an die [**WSAQUERYSET-Struktur**](bluetooth-and-wsaqueryset-for-set-service.md) zu übergeben oder zu \* empfangen.

Für die Verwendung mit Bluetooth und [**der WSASetService-Funktion**](bluetooth-and-wsasetservice.md) müssen die [**BLOB-Strukturmitglieder**](/windows/desktop/api/nspapi/ns-nspapi-blob) über die folgenden Einstellungen verfügen:

-   Das **cbsize-Element** muss auf die Größe der im **pBlobData-Element** verwendeten [**BTH \_ SET \_ SERVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) in Bytes festgelegt werden.
-   Der **pBlobData-Member** muss ein Zeiger auf eine [**BTH \_ SET \_ SERVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) sein.

Verwenden Sie für Bluetooth [und WSALookupServiceBegin für Die](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)Geräteanfrage die folgenden Einstellungen:

-   Das **cbsize-Element** muss auf die Größe der [**BTH \_ QUERY \_ DEVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) festgelegt werden, die im **pBlobData-Element** in Bytes verwendet wird.
-   Das **pBlobData-Element** muss ein Zeiger auf eine [**BTH \_ QUERY \_ DEVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) sein.

Verwenden Sie für Bluetooth [und WSALookupServiceBegin für die Dienstermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)die folgenden Einstellungen:

-   Das **cbsize-Element** muss auf die Größe der im **pBlobData-Element** verwendeten [**BTH \_ QUERY \_ SERVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) in Bytes festgelegt werden.
-   Der **pBlobData-Member** muss ein Zeiger auf eine [**BTH \_ QUERY \_ SERVICE-Struktur**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) sein.

Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der [**Referenzseite zur BTH \_ SET \_ SERVICE-Struktur.**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und WSALookupServiceBegin für die Geräteanfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin für die Dienstermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_BTH-ABFRAGEGERÄT \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_BTH-ABFRAGEDIENST \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 