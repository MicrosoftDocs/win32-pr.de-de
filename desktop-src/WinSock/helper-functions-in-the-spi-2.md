---
description: Nspgetserviceclassinfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Hilfsfunktionen in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345062"
---
# <a name="helper-functions-in-the-spi"></a>Hilfsfunktionen in der SPI

-   [**Nspgetserviceclassinfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

Die [**nspgetserviceclassinfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) -Funktion ruft Schema Informationen der Dienstklasse ab, die von einem Namespace Anbieter beibehalten wurden. Sie wird auch von der Windows Sockets 2-dll in der Implementierung von [**wsagetserviceclassnamebyclassid**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)verwendet.

Die folgenden Makros, die in der Header Datei " *svcguid. h* " definiert sind, können bei der Zuordnung von bekannten Dienst Klassen und diesen Namespaces helfen.

| Makroname                                                                              | BESCHREIBUNG                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Svcid \_ TCP (Port)**<br/> **Svcid \_ UDP (Port)**<br/>                         | Bei einem TCP-oder UDP-Port für das Internet Protokoll wird die GUID zurückgegeben.                                                                               |
| **ist \_ svcid \_ TCP (GUID)**<br/> **ist \_ svcid \_ UDP (GUID)**<br/>                 | Gibt **true** zurück, wenn die GUID für TCP oder UDP innerhalb des zulässigen Bereichs liegt.                                                                         |
| **Port \_ von \_ svcid \_ TCP (GUID)**<br/> **Port \_ von \_ svcid \_ UDP (GUID)**<br/> | Gibt den TCP-oder UDP-Port zurück, der der GUID zugeordnet ist.                                                                                              |
| **svcid \_ NetWare (SAPID)**<br/>                                                    | Gibt die GUID zurück, wenn der Dienst Ankündigungs Protokoll (SAP)-Bezeichner angegeben ist. Dieses Makro wird mit dem SAP-Namespace in einer NetWare-Umgebung verwendet. |
| **SAPID \_ von \_ svcid \_ NetWare (GUID)**<br/>                                        | Gibt den NetWare-SAP-Bezeichner zurück, der der GUID zugeordnet ist. Dieses Makro wird mit dem SAP-Namespace in einer NetWare-Umgebung verwendet.               |
| **ist \_ svcid \_ NetWare (GUID)**<br/>                                                 | Gibt **true** zurück, wenn die GUID für NetWare innerhalb des zulässigen Bereichs liegt. Dieses Makro wird mit dem SAP-Namespace in einer NetWare-Umgebung verwendet.    |



 

> [!Note]  
> Die Header Datei " *svcguid. h* " ist nicht automatisch in der Header Datei " *Winsock2. h* " enthalten.

 

 

 




