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
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="e08f4-103">GetHostName-Funktion in der SPI</span><span class="sxs-lookup"><span data-stu-id="e08f4-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="e08f4-104">Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet den svcid- \_ Hostnamen als Dienst Klassen-GUID.</span><span class="sxs-lookup"><span data-stu-id="e08f4-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="e08f4-105">, Wenn *lpszserviceingestancename* NULL ist oder auf eine NULL-Zeichenfolge verweist (d. h..</span><span class="sxs-lookup"><span data-stu-id="e08f4-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="e08f4-106">""), muss der lokale Host aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="e08f4-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="e08f4-107">Andernfalls sollte eine Suche nach einem angegebenen Hostnamen erfolgen.</span><span class="sxs-lookup"><span data-stu-id="e08f4-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="e08f4-108">Im Rahmen der emueration von [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) gibt Ws2 \_32.dll einen NULL-Zeiger für *lpszserviceinstancename* an und \_ gibt den \_ luprückgabenamen an, sodass der Hostname im *lpszserviceinstancename* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e08f4-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="e08f4-109">Wenn eine Anwendung diese Abfrage verwendet und eine "Lup \_ Return addr" angibt, \_ wird die Host Adresse in einer **csaddr- \_ Informations** Struktur bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e08f4-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="e08f4-110">Die PPS- \_ Rückgabe- \_ BLOB-Aktion ist für diese Abfrage nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="e08f4-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="e08f4-111">Die Port Informationen werden standardmäßig auf 0 (null) festgelegt, es sei denn, die *lpszquerystring* verweist auf einen Dienst wie FTP. in diesem Fall wird die gesamte Transport Adresse des angegebenen Dienstanbieter bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e08f4-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



