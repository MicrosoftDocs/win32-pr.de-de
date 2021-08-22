---
description: Die WSALookupServiceBegin-Abfrage verwendet SVCID \_ HOSTNAME als Dienstklassen-GUID.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: gethostname-Funktion in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b610016222ab8a06ed874377be9ae447ad1d194ab9605a6e07b3cf829f520093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132263"
---
# <a name="gethostname-function-in-the-spi"></a>gethostname-Funktion in der SPI

Die [**WSALookupServiceBegin-Abfrage**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) verwendet SVCID \_ HOSTNAME als Dienstklassen-GUID. Wenn *lpszServiceInstanceName* NULL ist oder auf eine NULL-Zeichenfolge verweist (d. h. . ""), der lokale Host aufgelöst werden soll. Andernfalls muss eine Suche nach einem angegebenen Hostnamen erfolgen. Zum Emulieren von [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) gibt der Ws2-32.dll \_ einen NULL-Zeiger für *lpszServiceInstanceName* und LUP \_ RETURN NAME \_ an, sodass der Hostname im *lpszServiceInstanceName-Parameter* zurückgegeben wird. Wenn eine Anwendung diese Abfrage verwendet und LUP \_ RETURN \_ ADDR angibt, wird die Hostadresse in einer **CSADDR \_ INFO-Struktur** bereitgestellt. Die LUP \_ RETURN \_ BLOB-Aktion ist für diese Abfrage nicht definiert. Portinformationen werden standardmäßig auf 0 festgelegt, es sei denn, *lpszQueryString* verweist auf einen Dienst wie ftp. In diesem Fall wird die vollständige Transportadresse des angegebenen Diensts angegeben.

 

 



