---
description: Die wsalookupservicebegin-Abfrage verwendet svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Funktion "gethostbyaddr" in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526171"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Funktion "gethostbyaddr" in SPI

Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID. Die Host Adresse wird in *lpszserviceinstancename* als gepunktete Dezimalstellen-IPv4-Adress Zeichenfolge (z. b. 192.9.200.120) bereitgestellt. Der *Ws2 \_32.dll* gibt das \_ luprückgabeblob \_ an, und der NSP platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben). NSPs sollten auch diese anderen Lup- \_ rückgabeflags berücksichtigen \_ \* .



| Flag              | Beschreibung                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt den **h- \_ Namen** Member aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.                                                     |
| Lup \_ Return \_ addr | Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt. |



 

 

 
