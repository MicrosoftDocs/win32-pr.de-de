---
description: Die gethostbyaddr-Funktion verwendet die WSALookupServiceBegin-Funktion, um SVCID \_ INET \_ HOSTNAMEBYADDR als Dienstklassen-GUID abfragt.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: gethostbyaddr-Funktion in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac84d30ba919a4fc61456d5ca4772c12df786d89241e8249b57068b9aac3f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132323"
---
# <a name="gethostbyaddr-function-in-the-api"></a>gethostbyaddr-Funktion in der API

Die [**gethostbyaddr-Funktion**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) verwendet die [**WSALookupServiceBegin-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) um SVCID \_ INET \_ HOSTNAMEBYADDR als Dienstklassen-GUID abfragt. Die Hostadresse wird als gepunktete, dezimale IPv4-Zeichenfolge (z.B. "192.9.200.120") im *lpszServiceInstanceName-Member* der [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) bereitgestellt, die an die **WSALookupServiceBegin-Funktion** übergeben wird. Der Ws2-32.dll gibt LUP RETURN BLOB an, und der Name-Dienstanbieter platziert eine \_ \_ \_ [**HOSTENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-hostent) im Blob (mit Offsets anstelle von Zeigern, wie oben beschrieben). Namendienstanbieter sollten auch diese anderen LUP \_ \_ \* RETURN-Flags verwenden. 

| Flag              | Beschreibung                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-RÜCKGABENAME \_ | Gibt den **Member h \_ name** aus [**der HOSTENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName zurück.*                                                     |
| \_ \_ LUP-RÜCKGABE-ADDR | Gibt Adressierungsinformationen [**von HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR \_ INFO-Strukturen**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) zurück. Portinformationen werden standardmäßig auf 0 (null) festgelegt. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
