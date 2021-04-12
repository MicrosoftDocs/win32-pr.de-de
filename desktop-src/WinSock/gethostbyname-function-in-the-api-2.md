---
description: Die Funktion "gethostbyname" in der Winsock-API.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Funktion "gethostbyname" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129192"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="3cf2b-103">Funktion "gethostbyname" in der API</span><span class="sxs-lookup"><span data-stu-id="3cf2b-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="3cf2b-104">Die Funktion " [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " verwendet die Funktion " [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ", um svcid \_ inet \_ hostaddrbyname als Dienst Klassen-GUID abzufragen.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="3cf2b-105">Der Hostname wird im **lpszserviceinstancename** -Member in der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur angegeben, die an die **wsalookupservicebegin** -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="3cf2b-106">Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der Name Service Provider platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="3cf2b-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="3cf2b-107">Namens Dienstanbieter sollten diese anderen Lup \_ - \_ \* rückgabeflags ebenfalls berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="3cf2b-108">Flag</span><span class="sxs-lookup"><span data-stu-id="3cf2b-108">Flag</span></span>              | <span data-ttu-id="3cf2b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cf2b-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf2b-110">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="3cf2b-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="3cf2b-111">Gibt das **h- \_ Name** -Element aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="3cf2b-112">Lup \_ Return \_ addr</span><span class="sxs-lookup"><span data-stu-id="3cf2b-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="3cf2b-113">Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="3cf2b-114">Beachten Sie, dass mit dieser Routine keine Hostnamen aufgelöst werden, die aus einer gepunkteten IPv4-Adresse bestehen.</span><span class="sxs-lookup"><span data-stu-id="3cf2b-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3cf2b-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3cf2b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cf2b-116">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="3cf2b-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="3cf2b-117">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="3cf2b-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="3cf2b-118">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="3cf2b-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
