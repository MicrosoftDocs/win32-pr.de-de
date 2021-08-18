---
description: Die gethostname-Funktion verwendet die WSALookupServiceBegin-Funktion, um SVCID \_ HOSTNAME als Dienstklassen-GUID abzufragen.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: gethostname-Funktion in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec72c7eab46ccb9988dc166d8121304850ea49e2488901496e5c0377a395a48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132273"
---
# <a name="gethostname-function-in-the-api"></a>gethostname-Funktion in der API

Die [**gethostname-Funktion**](/windows/desktop/api/winsock/nf-winsock-gethostname) verwendet die [**WSALookupServiceBegin-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) um SVCID \_ HOSTNAME als Dienstklassen-GUID abzufragen. Wenn der **lpszServiceInstanceName-Member** der [**WSAQUERYSET-Struktur,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) der an die **WSALookupServiceBegin-Funktion** übergeben wird, **NULL** ist oder auf eine **NULL-Zeichenfolge** verweist (d. h. . ""), der lokale Host aufgelöst werden soll. Andernfalls erfolgt eine Suche nach einem angegebenen Hostnamen. Zum Emulieren von **gethostname** gibt der Ws2-32.dll \_ einen **NULL-Zeiger** für den **lpszServiceInstanceName-Member** und LUP \_ RETURN NAME \_ an, sodass der Hostname im **lpszServiceInstanceName-Member** zurückgegeben wird. Wenn eine Anwendung diese Abfrage verwendet und LUP \_ RETURN \_ ADDR angibt, wird die Hostadresse in einer [**CSADDR \_ INFO-Struktur**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) bereitgestellt. Die LUP \_ RETURN \_ BLOB-Aktion ist für diese Abfrage nicht definiert. Portinformationen werden standardmäßig auf 0 (null) festgelegt, es sei denn, der **lpszQueryString-Member** der **WSAQUERYSET-Struktur,** der an die **WSALookupServiceBegin-Funktion** übergeben wird, verweist auf einen Dienst wie FTP. In diesem Fall wird die vollständige Transportadresse des angegebenen Diensts angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierungs- und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
