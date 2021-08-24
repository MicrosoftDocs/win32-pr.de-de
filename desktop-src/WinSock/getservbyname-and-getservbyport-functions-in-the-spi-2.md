---
description: Die WSALookupServiceBegin-Abfrage verwendet SVCID \_ INET \_ SERVICEBYNAME als GUID der Dienstklasse.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: getservbyname- und getservbyport-Funktionen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466966db2fc605b4043355746a1e606626e3d5d518452d1fab661dcfb68b3238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132163"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>getservbyname- und getservbyport-Funktionen in der SPI

Die [**WSALookupServiceBegin-Abfrage**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) verwendet SVCID \_ INET \_ SERVICEBYNAME als GUID der Dienstklasse. Der *lpszServiceInstanceName-Parameter* verweist auf eine Zeichenfolge, die den Dienstnamen oder Den Dienstport und (optional) das Dienstprotokoll angibt. Die Formatierung der Zeichenfolge wird als ftp/tcp oder 21/tcp oder einfach als ftp dargestellt. Bei der Zeichenfolge wird die Schreibung nicht beachtet. Falls vorhanden, trennt der Schrägstrich den Protokollbezeichner vom vorherigen Teil der Zeichenfolge. Die Ws2-32.dll gibt LUP RETURN BLOB an, und der NSP legt eine \_ \_ \_ [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) im Blob ab (mit Offsets anstelle von Zeigern, wie oben beschrieben). NSPs sollten auch diese anderen \_ LUP-RETURN-Flags \_ \* honoriert werden.



| Flag              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-RÜCKGABENAME \_ | Gibt den **Namens \_ member aus** der [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName zurück.*                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_LUP-RÜCKGABETYP \_ | Gibt kanonische GUID in *lpServiceClassId* zurück. Es ist bekannt, dass sich ein als ftp oder 21 identifizierter Dienst gemäß den lokal festgelegten Konventionen an einem anderen Port befindet. Der **\_ Port-Member** der [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) sollte angeben, wo der Dienst in der lokalen Umgebung kontaktiert werden kann. Die kanonische GUID, die zurückgegeben wird, wenn LUP RETURN TYPE festgelegt ist, sollte eine der vordefinierten GUIDs von svcs.h sein, die der in der \_ \_ **SERVENT-Struktur** angegebenen Portnummer entspricht. |



 

 

 



