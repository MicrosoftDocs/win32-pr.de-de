---
description: PNRP verwendet die WSALookupServiceEnd-Funktion, um Folgendes durchzuführen.
ms.assetid: 0732929e-ca03-438f-80d9-48a3da0095f7
title: PNRP und WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db499c9a736e26d630b623a29baa4c18dcfceeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347688"
---
# <a name="pnrp-and-wsalookupserviceend"></a><span data-ttu-id="5b98c-103">PNRP und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="5b98c-103">PNRP and WSALookupServiceEnd</span></span>

<span data-ttu-id="5b98c-104">PNRP verwendet die [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) -Funktion, um Folgendes durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="5b98c-104">PNRP uses the [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) function to do the following:</span></span>

-   <span data-ttu-id="5b98c-105">Beenden einer Abfrage, die in einem vorherigen [ **wsalookupservicebegin** -aufrufen initiiert wurde](winsock-nsp-reference-links.md)</span><span class="sxs-lookup"><span data-stu-id="5b98c-105">Terminate a query initiated in a previous call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md)</span></span>
-   <span data-ttu-id="5b98c-106">Aufheben der Blockierung eines [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Aufrufes zum Abbrechen der Suche</span><span class="sxs-lookup"><span data-stu-id="5b98c-106">Unblock a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to stop the search</span></span>

<span data-ttu-id="5b98c-107">Ein [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) -Aufrufe beendet eine Abfrage und bereinigt den Kontext.</span><span class="sxs-lookup"><span data-stu-id="5b98c-107">A call to [**WSALookupServiceEnd**](winsock-nsp-reference-links.md) terminates a query and cleans up the context.</span></span> <span data-ttu-id="5b98c-108">Das von einem **wsalookupservicebegin** -Befehl erhaltene Handle muss als Parameter an **WSALookupServiceEnd** übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b98c-108">The handle obtained from a call to **WSALookupServiceBegin** must be passed as a parameter to **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="5b98c-109">Weitere Informationen zu PNRP und der [**wsalookupservicebegin**](winsock-nsp-reference-links.md) -Funktion finden Sie unter [PNRP und wsalookupservicebegin](pnrp-and-wsalookupservicebegin.md).</span><span class="sxs-lookup"><span data-stu-id="5b98c-109">For more information about PNRP and the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function, see [PNRP and WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b98c-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b98c-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b98c-111">PNRP und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="5b98c-111">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="5b98c-112">PNRP-NSP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="5b98c-112">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="5b98c-113">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="5b98c-113">**WSALookupServiceNext**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



