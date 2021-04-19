---
description: Die GetHostName-Funktion verwendet die wsalookupservicebegin-Funktion, um den svcid- \_ Hostnamen als Dienst Klassen-GUID abzufragen.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Funktion "GetHostName" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348776"
---
# <a name="gethostname-function-in-the-api"></a>Funktion "GetHostName" in der API

Die [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) -Funktion verwendet die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktion, um den svcid- \_ Hostnamen als Dienst Klassen-GUID abzufragen. Wenn der **lpszserviceinstancename** -Member der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur, die an die **wsalookupservicebegin** -Funktion übergeben wurde, **null** ist oder auf eine **null** -Zeichenfolge verweist (d. h.. ""), muss der lokale Host aufgelöst werden. Andernfalls tritt eine Suche nach einem angegebenen Hostnamen auf. Zum emuinieren von **GetHostName** gibt das Ws2 \_ -32.dll einen **null** -Zeiger für das **lpszserviceinstancename** -Element an und gibt den Namen der Lup- \_ Rückgabe an, \_ sodass der Hostname im **lpszserviceinstancename** -Member zurückgegeben wird. Wenn eine Anwendung diese Abfrage verwendet und eine "Lup \_ Return addr" angibt, \_ wird die Host Adresse in einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur bereitgestellt. Die PPS- \_ Rückgabe- \_ BLOB-Aktion ist für diese Abfrage nicht definiert. Die Port Informationen werden standardmäßig auf NULL festgelegt, es sei denn, der **lpszquerystring** -Member der **wsaqueryset** -Struktur, die an die **wsalookupservicebegin** -Funktion übergeben wurde, verweist auf einen Dienst wie FTP. in diesem Fall wird die gesamte Transport Adresse des angegebenen Dienstanbieter bereitgestellt

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
