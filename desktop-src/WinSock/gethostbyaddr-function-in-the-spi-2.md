---
description: Die wsalookupservicebegin-Abfrage verwendet svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Funktion "gethostbyaddr" in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526171"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="475f8-103">Funktion "gethostbyaddr" in SPI</span><span class="sxs-lookup"><span data-stu-id="475f8-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="475f8-104">Die [**wsalookupservicebegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) -Abfrage verwendet svcid \_ inet \_ hostnamebyaddr als Dienst Klassen-GUID.</span><span class="sxs-lookup"><span data-stu-id="475f8-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="475f8-105">Die Host Adresse wird in *lpszserviceinstancename* als gepunktete Dezimalstellen-IPv4-Adress Zeichenfolge (z. b. 192.9.200.120) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="475f8-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="475f8-106">Der *Ws2 \_32.dll* gibt das \_ luprückgabeblob \_ an, und der NSP platziert eine [**hostende**](/windows/desktop/api/winsock/ns-winsock-hostent) Struktur im BLOB (verwendet Offsets anstelle von Zeigern, wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="475f8-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="475f8-107">NSPs sollten auch diese anderen Lup- \_ rückgabeflags berücksichtigen \_ \* .</span><span class="sxs-lookup"><span data-stu-id="475f8-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="475f8-108">Flag</span><span class="sxs-lookup"><span data-stu-id="475f8-108">Flag</span></span>              | <span data-ttu-id="475f8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="475f8-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="475f8-110">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="475f8-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="475f8-111">Gibt den **h- \_ Namen** Member aus der [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) -Struktur in *lpszserviceinstancename* zurück.</span><span class="sxs-lookup"><span data-stu-id="475f8-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="475f8-112">Lup \_ Return \_ addr</span><span class="sxs-lookup"><span data-stu-id="475f8-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="475f8-113">Gibt Adressierungs Informationen vom [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstrukturen zurück, Port Informationen werden standardmäßig auf 0 (null) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="475f8-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
