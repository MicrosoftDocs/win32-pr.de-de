---
description: PNRP verwendet die wsaqueryset-Struktur in Verbindung mit verschiedenen Funktionen, um das Auflösen von Namen und das Auflisten von Namen und Clouds zu vereinfachen.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP und wsaqueryset (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347687"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP und wsaqueryset

PNRP verwendet die [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur in Verbindung mit verschiedenen Funktionen, um das Auflösen von Namen und das Auflisten von Namen und Clouds zu vereinfachen.

Umfassende Definitionen von [**wsaqueryset**](winsock-nsp-reference-links.md) -oder Windows Sockets-Funktionen finden Sie in den entsprechenden Definitionen in der API-Dokumentation zu Windows Sockets 2 im Platform SDK.

## <a name="wsaqueryset-and-wsasetservice"></a>Wsaqueryset und wsasetservice

Die [**wsasetservice**](winsock-nsp-reference-links.md) -Funktion verwendet die **wsaqueryset** -Struktur, um Peer Namen zu registrieren oder zu entfernen. Auf der Seite [PNRP und wsasetservice](pnrp-and-wsasetservice.md) wird beschrieben, wie Sie die **wsaqueryset** -Struktur mit dieser Funktion verwenden.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>Wsaqueryset und wsalookupservicebegin

Die [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur wird in großem Umfang mit den Funktionen **wsalookupservicebegin**, **WSALookupServiceNext** und **WSALookupServiceEnd** verwendet. Details dazu, wie diese Funktionen die **wsaqueryset** -Struktur verwenden, werden auf den folgenden Referenzseiten ausführlich erläutert:

-   [PNRP und wsalookupservicebegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP und WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                             |
| Version<br/>                  | Windows XP mit SP1 mit dem erweiterten Netzwerk Paket für Windows XP<br/>  |
| Header<br/>                   | <dl> <dt>P2P. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und wsasetservice](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




