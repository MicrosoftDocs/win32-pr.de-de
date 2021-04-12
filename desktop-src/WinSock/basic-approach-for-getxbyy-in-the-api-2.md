---
description: Die meisten getxbyy-Funktionen werden vom Ws2- \_32.dll in eine wsalookupservicebegin-, WSALookupServiceNext-und WSALookupServiceEnd-Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Grundlegender Ansatz für getxbyy in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526207"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Grundlegender Ansatz für getxbyy in der API

Die meisten **getxbyy** -Funktionen werden vom Ws2- \_32.dll in eine [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)-, [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)-und [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) -Sequenz übersetzt, die eine Reihe spezieller GUIDs als Dienstklasse verwendet. Diese GUIDs bestimmen den Typ des **getxbyy** -Vorgangs, der emuliert wird. Die Abfrage wird auf solche namens Dienstanbieter beschränkt, die AF inet unterstützen \_ . Wenn eine **getxbyy** -Funktion eine [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -oder eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur zurückgibt, gibt die Ws2- \_32.dll das Lup- \_ \_ blobflag "BLOB" in **wsalookupservicebegin** an, sodass die gewünschten Informationen vom namens Dienstanbieter zurückgegeben werden. Diese Strukturen müssen geringfügig geändert werden, da die in enthaltenen Zeiger durch Offsets ersetzt werden müssen, die relativ zum Anfang der Daten des BLOBs sind. Alle Werte, auf die von diesen Zeiger Parametern verwiesen wird, müssen natürlich vollständig im BLOB enthalten sein, und alle Zeichen folgen sind ASCII.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Protokoll unabhängige Namensauflösung](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Registrierung und Namensauflösung](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



