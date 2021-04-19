---
description: Die GetHostName-Funktion verwendet die wsalookupservicebegin-Funktion, um den svcid- \_ Hostnamen als Dienst Klassen-GUID abzufragen.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Funktion "GetHostName" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348776"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="fc9e6-103">Funktion "GetHostName" in der API</span><span class="sxs-lookup"><span data-stu-id="fc9e6-103">gethostname Function in the API</span></span>

<span data-ttu-id="fc9e6-104">Die [**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) -Funktion verwendet die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Funktion, um den svcid- \_ Hostnamen als Dienst Klassen-GUID abzufragen.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="fc9e6-105">Wenn der **lpszserviceinstancename** -Member der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur, die an die **wsalookupservicebegin** -Funktion übergeben wurde, **null** ist oder auf eine **null** -Zeichenfolge verweist (d. h..</span><span class="sxs-lookup"><span data-stu-id="fc9e6-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="fc9e6-106">""), muss der lokale Host aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="fc9e6-107">Andernfalls tritt eine Suche nach einem angegebenen Hostnamen auf.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="fc9e6-108">Zum emuinieren von **GetHostName** gibt das Ws2 \_ -32.dll einen **null** -Zeiger für das **lpszserviceinstancename** -Element an und gibt den Namen der Lup- \_ Rückgabe an, \_ sodass der Hostname im **lpszserviceinstancename** -Member zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="fc9e6-109">Wenn eine Anwendung diese Abfrage verwendet und eine "Lup \_ Return addr" angibt, \_ wird die Host Adresse in einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="fc9e6-110">Die PPS- \_ Rückgabe- \_ BLOB-Aktion ist für diese Abfrage nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="fc9e6-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="fc9e6-111">Die Port Informationen werden standardmäßig auf NULL festgelegt, es sei denn, der **lpszquerystring** -Member der **wsaqueryset** -Struktur, die an die **wsalookupservicebegin** -Funktion übergeben wurde, verweist auf einen Dienst wie FTP. in diesem Fall wird die gesamte Transport Adresse des angegebenen Dienstanbieter bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="fc9e6-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc9e6-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fc9e6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc9e6-113">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="fc9e6-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="fc9e6-114">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="fc9e6-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="fc9e6-115">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="fc9e6-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
