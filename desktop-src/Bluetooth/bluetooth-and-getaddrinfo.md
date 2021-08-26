---
title: Bluetooth und getaddrinfo
description: Die getaddrinfo-Funktion ermöglicht die Übersetzung von Hostname zu Adresse für IP-basierte Transporte. Da die getaddrinfo-Funktion für IP-basierte Transporte spezifisch ist, schlägt sie auf Bluetooth fehl.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth und getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9faea4cebf9eee183942da04f39dfae123feea4900483d27ae2d70d8cb5b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004530"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth und getaddrinfo

Die [**getaddrinfo-Funktion**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) ermöglicht die Übersetzung von Hostname zu Adresse für IP-basierte Transporte. Da die **getaddrinfo-Funktion** für IP-basierte Transporte spezifisch ist, schlägt sie auf Bluetooth fehl.

Um die Übersetzung von Hostname zu Adresse für Bluetooth-Sockets durchzuführen, verwenden Sie die [**WSALookupServiceBegin-Funktion**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) mit **\_ LUP-CONTAINERn,** um Remotegeräte abfragt und dann nach einem bestimmten übereinstimmenden Remotenamen und einer entsprechenden Adresse zu suchen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 