---
description: Die Funktionen getservbyname und getservbyport verwenden die WSALookupServiceBegin-Funktion, um SVCID \_ INET \_ SERVICEBYNAME als Dienstklassen-GUID abzufragen.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: getservbyname- und getservbyport-Funktionen in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e5d7cc9b1811eef98cc6d337abc3230ea46bd537a19969a4b412473e671b39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132213"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a>getservbyname- und getservbyport-Funktionen in der API

Die Funktionen [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) und [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) verwenden die [**WSALookupServiceBegin-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) um SVCID \_ INET \_ SERVICEBYNAME als Dienstklassen-GUID abzufragen. Der *lpszServiceInstanceName-Member* in der [**WSAQUERYSET-Struktur,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) der an die **WSALookupServiceBegin-Funktion** übergeben wird, verweist auf eine Zeichenfolge, um den Dienstnamen oder Dienstport anzugeben, und (optional) auf das Dienstprotokoll. Die Formatierung der Zeichenfolge wird als FTP oder TCP oder 21/TCP oder nur FTP dargestellt. Bei der Zeichenfolge wird die Groß-/Kleinschreibung nicht beachtet. Falls vorhanden, trennt der Schrägstrich den Protokollbezeichner vom vorherigen Teil der Zeichenfolge. Der \_ Ws2-32.dll gibt LUP \_ RETURN BLOB \_ an, und der Namespaceanbieter legt eine [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) im Blob fest (mit Offsets anstelle von Zeigern, wie oben beschrieben). Namespaceanbieter sollten diese anderen LUP \_ \_ \* RETURN-Flags ebenfalls berücksichtigen.

| Flag              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-RÜCKGABENAME \_ | Gibt den **\_ Namensmember** aus der [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) in *lpszServiceInstanceName* zurück.                                                                                                                                                                                                                                                                                                                                                                                                               |
| \_LUP-RÜCKGABETYP \_ | Gibt kanonische GUID in *lpServiceClassId* zurück. Es wird davon ausgegangen, dass sich ein als FTP oder 21 identifizierter Dienst gemäß den lokal festgelegten Konventionen auf einem anderen Port befindet. Der **\_ Portparameter** der [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) sollte angeben, wo der Dienst in der lokalen Umgebung kontaktiert werden kann. Die kanonische GUID, die zurückgegeben wird, wenn LUP \_ RETURN \_ TYPE festgelegt wird, sollte eine der vordefinierten GUIDs von Svcs.h sein, die der in der **SERVENT-Struktur** angegebenen Portnummer entsprechen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierungs- und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



