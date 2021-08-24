---
description: Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock ATM-Strukturen. Klicken Sie auf den Strukturnamen, um weitere Informationen zu einer Struktur zu erhalten.
ms.assetid: ce80ef1f-9a76-4a6f-a7ce-f166bc46ca08
title: Winsock ATM-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f45cafef8bcf628f9172f2ad7ce3323d0d5b0c3e2c3912d195615ea2471501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612800"
---
# <a name="winsock-atm-structures"></a>Winsock ATM-Strukturen

Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock ATM-Strukturen. Klicken Sie auf den Strukturnamen, um weitere Informationen zu einer Struktur zu erhalten.



| ATM-Struktur                           | Beschreibung                                                |
|-----------------------------------------|------------------------------------------------------------|
| [**ADRESSE DES \_ GELDAUTOMATEN**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_address)   | Speichert ATM-Adressdaten für ATM-basierte Sockets.             |
| [**\_ATM-BESENSLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_bhli)         | Identifiziert B-HLI-Informationen für einen zugeordneten ATM-Socket. |
| [**ATM \_ BLLI**](/windows/desktop/api/Ws2atm/ns-ws2atm-atm_blli)         | Identifiziert B-LLI-Informationen für einen zugeordneten ATM-Socket. |
| [**sockaddr \_ atm**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) | Speichert Socketadresseninformationen für ATM-Sockets.         |



 

Verwenden Sie für native ATM-Dienste AF ATM für die Adressfamilie und die \_ [**Sockaddr-Atm-Socketaddr-Adressstruktur. \_**](/windows/desktop/api/Ws2atm/ns-ws2atm-sockaddr_atm) Um einen nativen ATM-Socket zu öffnen, übergeben Sie AF \_ ATM, SOCK \_ RAW und ATMPROTO \_ AAL5 bzw. ATMPROTO \_ ATOLSER an die [**Socketfunktion.**](/windows/desktop/api/Winsock2/nf-winsock2-socket)

 

 



