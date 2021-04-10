---
description: Die wsalookupservicebegin-Abfrage verwendet svcid \_ inet \_ servicebyname als Dienst Klassen-GUID.
ms.assetid: 72ee4a10-2864-48e3-a72c-ae069eb5aef3
title: Funktionen "getservbyname" und "getservbyport" in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd910dc7ab478c262bd5ca6c480dc3ec58e1b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129188"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-spi"></a>Funktionen "getservbyname" und "getservbyport" in der SPI

Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet svcid \_ inet \_ servicebyname als Dienst Klassen-GUID. Der *lpszserviceinstancename* -Parameter verweist auf eine Zeichenfolge, die den Dienstnamen oder Dienstport angibt, und (optional) das Dienst Protokoll. Die Formatierung der Zeichenfolge wird als FTP/TCP oder 21/TCP oder nur FTP veranschaulicht. Bei der Zeichenfolge wird Groß-/Kleinschreibung nicht beachtet Der Schrägstrich trennt, falls vorhanden, den Protokoll Bezeichner vom vorangehenden Teil der Zeichenfolge. Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der NSP fügt eine [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur in das BLOB ein (verwendet Offsets anstelle von Zeigern, wie oben beschrieben). NSPs sollten auch diese anderen Lup- \_ rückgabeflags berücksichtigen \_ \* .



| Flag              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Name der Lup- \_ Rückgabe \_ | Gibt das **s- \_ Namen** Element aus der [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur in *lpszserviceinstancename* zurück.                                                                                                                                                                                                                                                                                                                                                                                                            |
| - \_ \_ Rückgabetyp | Gibt die kanonische GUID in *lpserviceclassid* zurück. es wird verstanden, dass sich ein als FTP oder 21 identifizierter Dienst gemäß den lokal festgelegten Konventionen an einem anderen Port befinden kann. Der **s- \_ portmember** der [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) -Struktur sollte angeben, wo der Dienst in der lokalen Umgebung kontaktiert werden kann. Die kanonische GUID, die zurückgegeben wird, wenn der Lup- \_ \_ Rückgabetyp festgelegt ist, muss eine der vordefinierten GUIDs aus SVCs. h sein, die der in der **servent** -Struktur aufgeführten Portnummer entspricht. |



 

 

 



