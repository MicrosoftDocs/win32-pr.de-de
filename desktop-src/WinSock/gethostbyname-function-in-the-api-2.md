---
description: Die Funktion "gethostbyname" in der Winsock-API.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Funktion "gethostbyname" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129192"
---
# <a name="gethostbyname-function-in-the-api"></a>Funktion "gethostbyname" in der API

Die Funktion " [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " verwendet die Funktion " [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ", um svcid \_ inet \_ hostaddrbyname als Dienst Klassen-GUID abzufragen. Der Hostname wird im **lpszserviceinstancename** -Member in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur angegeben, die an die **wsalookupservicebegin** -Funktion übergeben wird. Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der Name Service Provider platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben). Namens Dienstanbieter sollten diese anderen Lup \_ - \_ \* rückgabeflags ebenfalls berücksichtigen.

| Flag              | Beschreibung                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt das **h- \_ Name** -Element aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.                                                                                                                                           |
| Lup \_ Return \_ addr | Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt. Beachten Sie, dass mit dieser Routine keine Hostnamen aufgelöst werden, die aus einer gepunkteten IPv4-Adresse bestehen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
