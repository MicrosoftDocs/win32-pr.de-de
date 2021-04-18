---
description: Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-ATM-Strukturen. Wenn Sie weitere Informationen zu einer Struktur haben, klicken Sie auf den Struktur Namen.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Winsock ATM-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf28266de89e5346727a9ad42fdb90d9167bc9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345806"
---
# <a name="winsock-atm-structures"></a>Winsock ATM-Strukturen

Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-ATM-Strukturen. Wenn Sie weitere Informationen zu einer Struktur haben, klicken Sie auf den Struktur Namen.



| ATM-Struktur                           | BESCHREIBUNG                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**ATM- \_ Adresse**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Speichert ATM-Adressdaten für ATM-basierte Sockets.             |
| [**ATM- \_ bhli**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifiziert B-HLI-Informationen für einen zugeordneten ATM-Socket. |
| [**ATM \_ blli**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifiziert B-lli-Informationen für einen zugeordneten ATM-Socket. |
| [**sockaddr \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Speichert socketadressinformationen für ATM-Sockets.         |



 

Verwenden Sie für systemeigene ATM \_ -Dienste den AF-ATM für die Adressfamilie und die [**sockaddr \_ ATM**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) -socketadressstruktur. Um einen systemeigenen ATM-Socket zu öffnen, übergeben Sie AF \_ ATM, sock \_ RAW und atmproto \_ AAL5 bzw. atmproto \_ aaluser an die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) .

 

 



