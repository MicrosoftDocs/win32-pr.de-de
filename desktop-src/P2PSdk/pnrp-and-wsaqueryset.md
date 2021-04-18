---
description: PNRP verwendet die wsaqueryset-Struktur in Verbindung mit verschiedenen Funktionen, um das Auflösen von Namen und das Auflisten von Namen und Clouds zu vereinfachen.
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: PNRP und wsaqueryset (P2P. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347687"
---
# <a name="pnrp-and-wsaqueryset"></a><span data-ttu-id="f4e94-103">PNRP und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="f4e94-103">PNRP and WSAQUERYSET</span></span>

<span data-ttu-id="f4e94-104">PNRP verwendet die [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur in Verbindung mit verschiedenen Funktionen, um das Auflösen von Namen und das Auflisten von Namen und Clouds zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="f4e94-104">PNRP uses the [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure in conjunction with various functions to facilitate resolving names and enumerating names and clouds.</span></span>

<span data-ttu-id="f4e94-105">Umfassende Definitionen von [**wsaqueryset**](winsock-nsp-reference-links.md) -oder Windows Sockets-Funktionen finden Sie in den entsprechenden Definitionen in der API-Dokumentation zu Windows Sockets 2 im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f4e94-105">For complete definitions of [**WSAQUERYSET**](winsock-nsp-reference-links.md) or Windows Sockets functions, see their respective definitions in the Windows Sockets 2 API documentation in the Platform SDK.</span></span>

## <a name="wsaqueryset-and-wsasetservice"></a><span data-ttu-id="f4e94-106">Wsaqueryset und wsasetservice</span><span class="sxs-lookup"><span data-stu-id="f4e94-106">WSAQUERYSET and WSASetService</span></span>

<span data-ttu-id="f4e94-107">Die [**wsasetservice**](winsock-nsp-reference-links.md) -Funktion verwendet die **wsaqueryset** -Struktur, um Peer Namen zu registrieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f4e94-107">The [**WSASetService**](winsock-nsp-reference-links.md) function uses the **WSAQUERYSET** structure to register or remove peer names.</span></span> <span data-ttu-id="f4e94-108">Auf der Seite [PNRP und wsasetservice](pnrp-and-wsasetservice.md) wird beschrieben, wie Sie die **wsaqueryset** -Struktur mit dieser Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4e94-108">The [PNRP and WSASetService](pnrp-and-wsasetservice.md) page outlines how to use the **WSAQUERYSET** structure with this function.</span></span>

## <a name="wsaqueryset-and-wsalookupservicebegin"></a><span data-ttu-id="f4e94-109">Wsaqueryset und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="f4e94-109">WSAQUERYSET and WSALookupServiceBegin</span></span>

<span data-ttu-id="f4e94-110">Die [**wsaqueryset**](winsock-nsp-reference-links.md) -Struktur wird in großem Umfang mit den Funktionen **wsalookupservicebegin**, **WSALookupServiceNext** und **WSALookupServiceEnd** verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4e94-110">The [**WSAQUERYSET**](winsock-nsp-reference-links.md) structure is used extensively with the **WSALookupServiceBegin**, **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span> <span data-ttu-id="f4e94-111">Details dazu, wie diese Funktionen die **wsaqueryset** -Struktur verwenden, werden auf den folgenden Referenzseiten ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="f4e94-111">Details about how these functions use the **WSAQUERYSET** structure are detailed in the following reference pages:</span></span>

-   [<span data-ttu-id="f4e94-112">PNRP und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="f4e94-112">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
-   [<span data-ttu-id="f4e94-113">PNRP und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="f4e94-113">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
-   [<span data-ttu-id="f4e94-114">PNRP und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="f4e94-114">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a><span data-ttu-id="f4e94-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4e94-115">Requirements</span></span>



| <span data-ttu-id="f4e94-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4e94-116">Requirement</span></span> | <span data-ttu-id="f4e94-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f4e94-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4e94-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4e94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f4e94-119">Nur Windows XP mit SP2 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4e94-119">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4e94-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4e94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f4e94-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4e94-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4e94-122">Version</span><span class="sxs-lookup"><span data-stu-id="f4e94-122">Version</span></span><br/>                  | <span data-ttu-id="f4e94-123">Windows XP mit SP1 mit dem erweiterten Netzwerk Paket für Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4e94-123">Windows XP with SP1 with the Advanced Networking Pack for Windows XP</span></span><br/>  |
| <span data-ttu-id="f4e94-124">Header</span><span class="sxs-lookup"><span data-stu-id="f4e94-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4e94-125"><dt>P2P. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4e94-125"><dt>P2P.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e94-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4e94-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e94-127">PNRP und BLOB</span><span class="sxs-lookup"><span data-stu-id="f4e94-127">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="f4e94-128">PNRP und wsasetservice</span><span class="sxs-lookup"><span data-stu-id="f4e94-128">PNRP and WSASetService</span></span>](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




