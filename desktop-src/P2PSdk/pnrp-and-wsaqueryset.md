---
description: PNRP verwendet die WSAQUERYSET-Struktur in Verbindung mit verschiedenen Funktionen, um das Auflösen von Namen und das Auflisten von Namen und Clouds zu vereinfachen.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP und WSAQUERYSET (P2P.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbc635b0c1ca19cfaeeeb7f8b013aefad1e49e2141dd9715a36c0238e7be6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061357"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP und WSAQUERYSET

PNRP verwendet die [**WSAQUERYSET-Struktur**](winsock-nsp-reference-links.md) in Verbindung mit verschiedenen Funktionen, um das Auflösen von Namen und das Auflisten von Namen und Clouds zu vereinfachen.

Vollständige Definitionen von [**WSAQUERYSET-**](winsock-nsp-reference-links.md) oder Windows Sockets-Funktionen finden Sie in den entsprechenden Definitionen in der Windows Sockets 2-API-Dokumentation im Plattform-SDK.

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET und WSASetService

Die [**WSASetService-Funktion**](winsock-nsp-reference-links.md) verwendet die **WSAQUERYSET-Struktur,** um Peernamen zu registrieren oder zu entfernen. Auf der Seite [PNRP und WSASetService](pnrp-and-wsasetservice.md) wird die Verwendung der **WSAQUERYSET-Struktur** mit dieser Funktion beschrieben.

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET und WSALookupServiceBegin

Die [**WSAQUERYSET-Struktur**](winsock-nsp-reference-links.md) wird umfassend mit den Funktionen **WSALookupServiceBegin,** **WSALookupServiceNext** und **WSALookupServiceEnd** verwendet. Details zur Verwendung der **WSAQUERYSET-Struktur** durch diese Funktionen finden Sie auf den folgenden Referenzseiten:

-   [PNRP und WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP und WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP und WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                             |
| Version<br/>                  | Windows XP mit SP1 mit dem Advanced Networking Pack für Windows XP<br/>  |
| Header<br/>                   | <dl> <dt>P2P.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[PNRP und BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP und WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




