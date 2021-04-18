---
title: Bluetooth und BLOB
description: Bluetooth verwendet die BLOB-Struktur, um bei Aufrufen der wsasetservice-oder WSALookupService \-Funktionen Transport spezifische Daten an die wsaqueryset-Struktur zu übergeben oder zu empfangen.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth und BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340522"
---
# <a name="bluetooth-and-blob"></a>Bluetooth und BLOB

Bluetooth verwendet die [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Struktur, um bei Aufrufen der [**wsasetservice**](bluetooth-and-wsasetservice.md) -oder **WSALookupService** -Funktionen Transport spezifische Daten an die [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur zu übergeben oder zu empfangen \* .

Zur Verwendung mit Bluetooth und der [**wsasetservice**](bluetooth-and-wsasetservice.md) -Funktion benötigen die [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) -Strukturmember die folgenden Einstellungen:

-   Das **CBSIZE** -Element muss auf die Größe der im **pblobdata** -Member verwendeten Struktur des [**BTH- \_ Set- \_ dienstansatzes**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) (in Bytes) festgelegt werden.
-   Der **pblobdata** -Member muss ein Zeiger auf eine [**BTH \_ Set \_ Service**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) -Struktur sein.

Verwenden Sie für die Verwendung mit Bluetooth und [wsalookupservicebegin für die Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)die folgenden Einstellungen:

-   Das **CBSIZE** -Element muss auf die Größe der [**BTH- \_ Abfrage \_ Geräte**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) Struktur, die im **pblobdata** -Element verwendet wird, in Bytes festgelegt werden.
-   Der **pblobdata** -Member muss ein Zeiger auf eine [**BTH- \_ Abfrage \_ Geräte**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) Struktur sein.

Verwenden Sie für die Verwendung mit Bluetooth und [wsalookupservicebegin für die Dienst](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)Ermittlung die folgenden Einstellungen:

-   Das **CBSIZE** -Element muss auf die Größe der [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) Struktur festgelegt werden, die im **pblobdata** -Member verwendet wird (in Bytes).
-   Der **pblobdata** -Member muss ein Zeiger auf eine [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) Struktur sein.

Weitere Informationen finden Sie im Abschnitt "Hinweise" auf der Referenzseite zum [**BTH- \_ Satz der \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) Struktur.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und wsalookupservicebegin für Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin für die Dienst Ermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und wsasetservice](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH- \_ Abfrage \_ Gerät**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH- \_ Set- \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**Wsasetservice**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 