---
title: Ermitteln von Bluetooth-Geräten und -Diensten
description: Um die Ermittlung von Bluetooth-Geräten und-Diensten zu vereinfachen, ordnet Windows das Bluetooth Service Discovery-Protokoll (SDP) den Windows Sockets-Namespace Schnittstellen zu.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, Tasks, ermitteln von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "106339049"
---
# <a name="discovering-bluetooth-devices-and-services"></a>Ermitteln von Bluetooth-Geräten und -Diensten

Um die Ermittlung von Bluetooth-Geräten und-Diensten zu vereinfachen, ordnet Windows das Bluetooth Service Discovery-Protokoll (SDP) den Windows Sockets-Namespace Schnittstellen zu. Die primären Funktionen, die für diese Zuordnung verwendet werden, sind die Funktionen [**wsasetservice**](bluetooth-and-wsasetservice.md), [**wsalookupservicebegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)und [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) . Die [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur wird auch in Verbindung mit diesen Funktionen verwendet.

Da bestimmte Konzepte und Parameter aus dem Bluetooth-SDP nicht notwendigerweise direkt in der [**wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md) -Struktur zugeordnet werden, muss die Aufmerksamkeit für die Erstellung und Verwendung ihrer Mitglieder bezahlt werden. Für viele komplexe Bluetooth-Vorgänge, wie z. b. die Erstellung von SDP-Datensätzen, wird das **lpblob** -Element von **wsaqueryset** verwendet. Wenn eine solche besondere Überlegung erforderlich ist, wird Sie speziell beschrieben, wie z. b. auf Verweis Seiten wie [**Bluetooth und WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), und anderen.

Es ist wichtig zu verstehen, dass die SDP-Registrierung vom socketsteuerelement getrennt ist. Wenn eine Serveranwendung für die Annahme der Client Verbindung vorbereitet ist, sollte Sie die [**wsasetservice**](bluetooth-and-wsasetservice.md) -Funktion zum Registrieren eines Bluetooth-SDP-Datensatzes, der diesem Dienst entspricht, registrieren. Diese Bluetooth-Anwendung muss die **wsasetservice** -Funktion vor dem Schließen erneut abrufen, um die Registrierung des Bluetooth-SDP-Datensatzes aufzuheben.

Wenn die auf dieser Seite beschriebenen Zuweisungs Funktionen verwendet werden, wird der NS- \_ BTH-Namespace zugewiesen.

Weitere Informationen zum Ermitteln von Geräten und Diensten finden Sie auf den folgenden Referenzseiten:

-   [**Bluetooth und wsasetservice**](bluetooth-and-wsasetservice.md)
-   [**Bluetooth und wsalookupservicebegin für Geräte Anfrage**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [**Bluetooth und wsalookupservicebegin für die Dienst Ermittlung**](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [**Bluetooth und WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md)
-   [**Bluetooth und WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md)
-   [**Bluetooth und BLOB**](bluetooth-and-blob.md)
-   [**Bluetooth und wsaqueryset**](bluetooth-and-wsaqueryset-for-set-service.md)

Sie können auch das [Bluetooth-Verbindungs](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) Beispiel herunterladen, um ein umfassendes Beispiel zu erhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth-Programmierung mit Windows Sockets](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[Beispiel für Bluetooth-Verbindung](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




