---
title: Bluetooth und getaddrinfo
description: Die getaddrinfo-Funktion ermöglicht die Übersetzung von Hostnamen in Adressen für IP-basierte Transporte. Da die getaddrinfo-Funktion spezifisch für IP-basierte Transporte ist, schlägt Sie an Bluetooth-Sockets fehl.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth und getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729849"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth und getaddrinfo

Die [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion ermöglicht die Übersetzung von Hostnamen in Adressen für IP-basierte Transporte. Da die **getaddrinfo** -Funktion spezifisch für IP-basierte Transporte ist, schlägt Sie an Bluetooth-Sockets fehl.

Um die Übersetzung vom Hostnamen zur Adresse für Bluetooth-Sockets auszuführen, verwenden Sie die [**wsalookupservicebegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) -Funktion mit **\_ lupcontainern** , um Remote Geräte abzufragen, und suchen Sie dann nach einem bestimmten Remote Namen und der entsprechenden Adresse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 