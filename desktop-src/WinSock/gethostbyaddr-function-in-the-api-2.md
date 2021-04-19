---
description: Die Funktion "gethostbyaddr" verwendet die Funktion "wsalookupservicebegin", um svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID abzufragen.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Funktion "gethostbyaddr" in der API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350431"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="43c1f-103">Funktion "gethostbyaddr" in der API</span><span class="sxs-lookup"><span data-stu-id="43c1f-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="43c1f-104">Die Funktion " [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) " verwendet die Funktion " [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) ", um svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID abzufragen.</span><span class="sxs-lookup"><span data-stu-id="43c1f-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="43c1f-105">Die Host Adresse wird als gepunktete dezimische IPv4-Zeichenfolge (z. b. "192.9.200.120") im *lpszserviceinstancename* -Member der [**wsaqueryset**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur angegeben, die an die **wsalookupservicebegin** -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="43c1f-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="43c1f-106">Der Ws2 \_ -32.dll gibt das \_ luprückgabeblob \_ an, und der Name Service Provider platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="43c1f-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="43c1f-107">Namens Dienstanbieter sollten diese anderen Lup \_ - \_ \* rückgabeflags ebenfalls berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="43c1f-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="43c1f-108">Flag</span><span class="sxs-lookup"><span data-stu-id="43c1f-108">Flag</span></span>              | <span data-ttu-id="43c1f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43c1f-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c1f-110">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="43c1f-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="43c1f-111">Gibt den **h- \_ Namen** Member aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.</span><span class="sxs-lookup"><span data-stu-id="43c1f-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="43c1f-112">Lup \_ Return \_ addr</span><span class="sxs-lookup"><span data-stu-id="43c1f-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="43c1f-113">Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="43c1f-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43c1f-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43c1f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43c1f-115">Kompatible Namensauflösung für TCP/IP in der Windows Sockets 1,1-API</span><span class="sxs-lookup"><span data-stu-id="43c1f-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="43c1f-116">Protokoll unabhängige Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="43c1f-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="43c1f-117">Registrierung und Namensauflösung</span><span class="sxs-lookup"><span data-stu-id="43c1f-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
