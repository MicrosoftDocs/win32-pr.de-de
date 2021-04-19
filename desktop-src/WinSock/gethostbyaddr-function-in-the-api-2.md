---
description: Die Funktion "gethostbyaddr" verwendet die Funktion "wsalookupservicebegin", um svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID abzufragen.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Funktion "gethostbyaddr" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350431"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Funktion "gethostbyaddr" in der API

Die Funktion " [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) " verwendet die Funktion " [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ", um svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID abzufragen. Die Host Adresse wird als gepunktete dezimische IPv4-Zeichenfolge (z. b. "192.9.200.120") im *lpszserviceinstancename* -Member der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur angegeben, die an die **wsalookupservicebegin** -Funktion übergeben wird. Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der Name Service Provider platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben). Namens Dienstanbieter sollten diese anderen Lup \_ - \_ \* rückgabeflags ebenfalls berücksichtigen. 

| Flag              | Beschreibung                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt den **h- \_ Namen** Member aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.                                                     |
| Lup \_ Return \_ addr | Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
