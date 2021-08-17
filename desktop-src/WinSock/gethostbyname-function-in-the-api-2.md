---
description: Gethostbyname-Funktion in der Winsock-API.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: gethostbyname-Funktion in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a63bf7884cd170721de9b7d5009ed53c7bcb60bb36869986862f5e81e03215b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132303"
---
# <a name="gethostbyname-function-in-the-api"></a>gethostbyname-Funktion in der API

Die [**gethostbyname-Funktion**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) verwendet die [**WSALookupServiceBegin-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) um SVCID \_ INET \_ HOSTADDRBYNAME als Dienstklassen-GUID abzufragen. Der Hostname wird im **lpszServiceInstanceName-Member** in der [**WSAQUERYSET-Struktur**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) angegeben, die an die **WSALookupServiceBegin-Funktion** übergeben wird. Der \_ Ws2-32.dll gibt LUP RETURN BLOB an, \_ und der \_ Name-Dienstanbieter platziert eine [**HOSTENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-hostent) im Blob (mit Offsets anstelle von Zeigern, wie oben beschrieben). Name-Dienstanbieter sollten diese anderen LUP \_ \_ \* RETURN-Flags ebenfalls berücksichtigen.

| Flag              | Beschreibung                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-RÜCKGABENAME \_ | Gibt den **\_ h-Namenmember** aus der [**HOSTENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName* zurück.                                                                                                                                           |
| LUP \_ RETURN \_ ADDR | Gibt Adressierungsinformationen von [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR \_ INFO-Strukturen**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) zurück. Portinformationen werden standardmäßig auf 0 (null) festgelegt. Beachten Sie, dass diese Routine keine Hostnamen auflöst, die aus einer gepunkteten IPv4-Adresse bestehen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierungs- und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
