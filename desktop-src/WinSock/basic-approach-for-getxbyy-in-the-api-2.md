---
description: Die meisten getXbyY-Funktionen werden vom \_ Ws2-32.dll in eine WSALookupServiceBegin-, WSALookupServiceNext- und WSALookupServiceEnd-Sequenz übersetzt, die eine spezielle GUIDs als Dienstklasse verwendet.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Grundlegende Vorgehensweise für GetXbyY in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e6dd0e5569bd11de813e28eaec1ee04f6b5f206277f695cdb9aaab05ec4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322624"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Grundlegende Vorgehensweise für GetXbyY in der API

Die meisten **getXbyY-Funktionen** werden vom Ws2-32.dll \_ in eine [**WSALookupServiceBegin-,**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) [**WSALookupServiceNext-**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)und [**WSALookupServiceEnd-Sequenz**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) übersetzt, die eine spezielle GUIDs als Dienstklasse verwendet. Diese GUIDs identifizieren den Typ des **getXbyY-Vorgangs,** der emuliert wird. Die Abfrage ist auf die Namendienstanbieter beschränkt, die AF \_ INET unterstützen. Wenn eine **getXbyY-Funktion** eine [**HOSTENT-**](/windows/desktop/api/winsock/ns-winsock-hostent) oder [**SERVENT-Struktur**](/windows/desktop/api/winsock/ns-winsock-servent) zurückgibt, gibt die Ws2-32.dll \_ das LUP \_ RETURN \_ BLOB-Flag in **WSALookupServiceBegin** an, sodass die gewünschten Informationen vom Namensdienstanbieter zurückgegeben werden. Diese Strukturen müssen geringfügig geändert werden, da die in enthaltenen Zeiger durch Offsets ersetzt werden müssen, die relativ zum Anfang der Blobdaten sind. Alle Werte, auf die von diesen Zeigerparametern verwiesen wird, müssen natürlich vollständig im Blob enthalten sein, und alle Zeichenfolgen sind ASCII.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1.1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokollunabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierungs- und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



