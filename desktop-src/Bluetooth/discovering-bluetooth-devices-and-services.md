---
title: Ermitteln von Bluetooth-Geräten und -Diensten
description: Um die Ermittlung von Bluetooth Geräten und Diensten zu erleichtern, ordnet Windows das Bluetooth Service Discovery Protocol (SDP) den Namespaceschnittstellen Windows Sockets zu.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, Aufgaben, Ermitteln von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae18f8f7ff8e7c2fcf2623ef9554bc77ec84d4b1d4ea56eced289cc86c12f0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004040"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Ermitteln von Bluetooth-Geräten und -Diensten

Um die Ermittlung von Bluetooth Geräten und Diensten zu erleichtern, ordnet Windows das Bluetooth Service Discovery Protocol (SDP) den Namespaceschnittstellen Windows Sockets zu. Die primären Funktionen, die für diese Zuordnung verwendet werden, sind die Funktionen [**WSASetService,**](bluetooth-and-wsasetservice.md) [**WSALookupServiceBegin,**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)und [**WSALookupServiceEnd.**](bluetooth-and-wsalookupserviceend.md) Die [**WSAQUERYSET-Struktur**](bluetooth-and-wsaqueryset-for-set-service.md) wird auch in Verbindung mit diesen Funktionen verwendet.

Da bestimmte Konzepte und Parameter aus dem Bluetooth SDP nicht notwendigerweise direkt der [**WSAQUERYSET-Struktur**](bluetooth-and-wsaqueryset-for-set-service.md) zugeordnet werden, muss darauf geachtet werden, wie die Member erstellt und verwendet werden. Für viele komplexe Bluetooth Vorgänge, z. B. die Erstellung von SDP-Datensätzen, wird der **lpBlob-Member** von **WSAQUERYSET** verwendet. Wenn eine solche besondere Berücksichtigung erforderlich ist, wird dies speziell beschrieben, z. B. in Referenzseiten wie [**Bluetooth und WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)und anderen.

Es ist wichtig zu verstehen, dass die SDP-Registrierung vom Socketsteuerelement getrennt ist. Wenn eine Serveranwendung darauf vorbereitet ist, eine Clientverbindung zu akzeptieren, sollte sie die [**WSASetService-Funktion**](bluetooth-and-wsasetservice.md) aufrufen, um einen Bluetooth SDP-Datensatz zu registrieren, der diesem Dienst entspricht. Diese Bluetooth Anwendung muss die **WSASetService-Funktion** vor dem Schließen erneut aufrufen, um die Registrierung des Bluetooth SDP-Datensatzes zu aufheben.

Bei Verwendung der auf dieser Seite beschriebenen Zuordnungsfunktionen wird der \_ NS-BTH-Namespace zugewiesen.

Weitere Informationen zum Ermitteln von Geräten und Diensten finden Sie auf den folgenden Referenzseiten:

-   [**Bluetooth und WSASetService**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth und WSALookupServiceBegin für Geräteabfragen**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth und WSALookupServiceBegin für die Dienstermittlung**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth und WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth und WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth und BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth und WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md)

Sie können auch das [Bluetooth Verbindungsbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) herunterladen, um ein vollständiges Beispiel zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth Programmieren mit Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Beispiel für Bluetooth Verbindung](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




