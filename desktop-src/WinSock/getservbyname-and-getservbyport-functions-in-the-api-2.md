---
description: Die Funktionen "getservbyname" und "getservbyport" verwenden die Funktion "wsalookupservicebegin", um svcid \_ inet \_ servicebyname als Dienst Klassen-GUID abzufragen.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Funktionen "getservbyname" und "getservbyport" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353067"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>Funktionen "getservbyname" und "getservbyport" in der API

Die Funktionen " [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) " und " [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) " verwenden die Funktion " [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ", um svcid \_ inet \_ servicebyname als Dienst Klassen-GUID abzufragen. Der *lpszserviceinstancename* -Member in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur, der an die **wsalookupservicebegin** -Funktion übergeben wird, verweist auf eine Zeichenfolge, um den Dienstnamen oder den Dienstport und (optional) das Dienst Protokoll anzugeben. Die Formatierung der Zeichenfolge wird als FTP, TCP oder 21/TCP oder nur FTP veranschaulicht. Bei der Zeichenfolge wird Groß-/Kleinschreibung nicht beachtet Der Schrägstrich trennt, falls vorhanden, den Protokoll Bezeichner vom vorangehenden Teil der Zeichenfolge. Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der Namespace Anbieter fügt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur in das BLOB ein (verwendet Offsets anstelle von Zeigern, wie oben beschrieben). Namespace Anbieter sollten diese anderen Lup- \_ \_ \* rückgabeflags ebenfalls berücksichtigen.

| Flag              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt das **s- \_ Namen** Element aus der [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur in *lpszserviceinstancename* zurück.                                                                                                                                                                                                                                                                                                                                                                                                               |
| - \_ \_ Rückgabetyp | Gibt die kanonische GUID in *lpserviceclassid* zurück. es wird verstanden, dass sich ein als FTP oder 21 identifizierter Dienst gemäß den lokal festgelegten Konventionen an einem anderen Port befinden kann. Der **s- \_ Port** Parameter der [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur sollte angeben, wo der Dienst in der lokalen Umgebung kontaktiert werden kann. Die kanonische GUID, die zurückgegeben wird, wenn der Lup- \_ \_ Rückgabetyp festgelegt ist, muss eine der vordefinierten GUIDs aus SVCs. h sein, die der in der **servent** -Struktur aufgeführten Portnummer entspricht. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



