---
description: Die WSALookupServiceBegin-Abfrage verwendet SVCID \_ INET \_ HOSTNAMEBYADDR als GUID der Dienstklasse.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: gethostbyaddr-Funktion in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e343bcd66b7b1482f14a07239ae73710fd789486633219952696406dd8f1bd3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132313"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>gethostbyaddr-Funktion in der SPI

Die [**WSALookupServiceBegin-Abfrage**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) verwendet SVCID \_ INET \_ HOSTNAMEBYADDR als GUID der Dienstklasse. Die Hostadresse wird in *lpszServiceInstanceName* als IPv4-Adresszeichenfolge mit gepunkteten Dezimalstellen angegeben (z.B. 192.9.200.120). Der *Ws232.dll\_* gibt LUP RETURN BLOB an, und der NSP platziert eine \_ \_ [**HOSTENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-hostent) im Blob (mit Offsets anstelle von Zeigern, wie oben beschrieben). NSPs sollten auch diese anderen \_ LUP-RETURN-Flags \_ \* honoriert werden.



| Flag              | Beschreibung                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-RÜCKGABENAME \_ | Gibt den **Member h \_ name** aus [**der HOSTENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-hostent) in *lpszServiceInstanceName zurück.*                                                     |
| \_ \_ LUP-RÜCKGABE-ADDR | Gibt Adressierungsinformationen [**von HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR \_ INFO-Strukturen**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) zurück. Portinformationen werden standardmäßig auf 0 (null) festgelegt. |



 

 

 
