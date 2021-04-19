---
description: Die gethostbyname-Funktion in der Winsock-SPI.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: gethostbyname-Funktion in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348179"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="fe848-103">gethostbyname-Funktion in der SPI</span><span class="sxs-lookup"><span data-stu-id="fe848-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="fe848-104">Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet svcid \_ inet \_ anstaddrbyname als Dienst Klassen-GUID.</span><span class="sxs-lookup"><span data-stu-id="fe848-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="fe848-105">Der Hostname wird in " *lpszserviceinstancename*" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fe848-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="fe848-106">Der *Ws2 \_32.dll* gibt das \_ luprückgabeblob \_ an, und der NSP platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="fe848-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="fe848-107">NSPs sollten auch diese anderen Lup- \_ rückgabeflags berücksichtigen \_ \* .</span><span class="sxs-lookup"><span data-stu-id="fe848-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="fe848-108">Flag</span><span class="sxs-lookup"><span data-stu-id="fe848-108">Flag</span></span>              | <span data-ttu-id="fe848-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fe848-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe848-110">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="fe848-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="fe848-111">Gibt den **h- \_ Namen** Member aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.</span><span class="sxs-lookup"><span data-stu-id="fe848-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="fe848-112">Lup \_ Return \_ addr</span><span class="sxs-lookup"><span data-stu-id="fe848-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="fe848-113">Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="fe848-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="fe848-114">Beachten Sie, dass diese Routine keine Hostnamen auflöst, die aus einer gepunkteten IPv4-Adress Zeichenfolge bestehen.</span><span class="sxs-lookup"><span data-stu-id="fe848-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
