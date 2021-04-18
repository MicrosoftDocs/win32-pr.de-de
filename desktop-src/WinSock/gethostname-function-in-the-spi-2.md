---
description: Die wsalookupservicebegin-Abfrage verwendet den svcid- \_ Hostnamen als Dienst Klassen-GUID.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: GetHostName-Funktion in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343297"
---
# <a name="gethostname-function-in-the-spi"></a>GetHostName-Funktion in der SPI

Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet den svcid- \_ Hostnamen als Dienst Klassen-GUID. , Wenn *lpszserviceingestancename* NULL ist oder auf eine NULL-Zeichenfolge verweist (d. h.. ""), muss der lokale Host aufgelöst werden. Andernfalls sollte eine Suche nach einem angegebenen Hostnamen erfolgen. Im Rahmen der emueration von [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) gibt Ws2 \_32.dll einen NULL-Zeiger für *lpszserviceinstancename* an und \_ gibt den \_ luprückgabenamen an, sodass der Hostname im *lpszserviceinstancename* -Parameter zurückgegeben wird. Wenn eine Anwendung diese Abfrage verwendet und eine "Lup \_ Return addr" angibt, \_ wird die Host Adresse in einer **csaddr- \_ Informations** Struktur bereitgestellt. Die PPS- \_ Rückgabe- \_ BLOB-Aktion ist für diese Abfrage nicht definiert. Die Port Informationen werden standardmäßig auf 0 (null) festgelegt, es sei denn, die *lpszquerystring* verweist auf einen Dienst wie FTP. in diesem Fall wird die gesamte Transport Adresse des angegebenen Dienstanbieter bereitgestellt.

 

 



