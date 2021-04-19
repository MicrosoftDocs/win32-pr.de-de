---
description: Die gethostbyname-Funktion in der Winsock-SPI.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: gethostbyname-Funktion in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348179"
---
# <a name="gethostbyname-function-in-the-spi"></a>gethostbyname-Funktion in der SPI

Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet svcid \_ inet \_ anstaddrbyname als Dienst Klassen-GUID. Der Hostname wird in " *lpszserviceinstancename*" bereitgestellt. Der *Ws2 \_32.dll* gibt das \_ luprückgabeblob \_ an, und der NSP platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben). NSPs sollten auch diese anderen Lup- \_ rückgabeflags berücksichtigen \_ \* .



| Flag              | Beschreibung                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt den **h- \_ Namen** Member aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.                                                                                                                                                            |
| Lup \_ Return \_ addr | Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt. Beachten Sie, dass diese Routine keine Hostnamen auflöst, die aus einer gepunkteten IPv4-Adress Zeichenfolge bestehen. |



 

 

 
