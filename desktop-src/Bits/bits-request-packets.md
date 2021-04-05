---
title: Bits-Anforderungs Pakete
description: Bits-Anforderungs Pakete
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947465"
---
# <a name="bits-request-packets"></a><span data-ttu-id="56cf9-103">Bits-Anforderungs Pakete</span><span class="sxs-lookup"><span data-stu-id="56cf9-103">BITS Request Packets</span></span>

<span data-ttu-id="56cf9-104">Anforderungs Pakete beschreiben Client Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="56cf9-104">Request packets describe client requests.</span></span> <span data-ttu-id="56cf9-105">Es kann immer nur eine ausstehende Anforderung vorhanden sein. Sie müssen eine Bestätigung [für die](bits-response-packets.md) aktuelle Anforderung vom Server erhalten, bevor Sie eine weitere Anforderung senden.</span><span class="sxs-lookup"><span data-stu-id="56cf9-105">There can be only one outstanding request at any given time; you must receive an [Ack](bits-response-packets.md) for the current request from the server before sending another request.</span></span>

<span data-ttu-id="56cf9-106">In der folgenden Tabelle werden die Anforderungs Pakete aufgelistet, die für Upload-und Upload-Reply-Aufträge an den BITS-Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="56cf9-106">The following table lists the request packets sent to the BITS server for upload and upload-reply jobs.</span></span> <span data-ttu-id="56cf9-107">In der Tabelle werden die Pakete in der typischen Reihenfolge aufgelistet, an die Sie an den Server gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="56cf9-107">The table lists the packets in the typical sequence they are sent to the server.</span></span>



| <span data-ttu-id="56cf9-108">Anforderungspaket</span><span class="sxs-lookup"><span data-stu-id="56cf9-108">Request packet</span></span>                       | <span data-ttu-id="56cf9-109">Zweck</span><span class="sxs-lookup"><span data-stu-id="56cf9-109">Purpose</span></span>                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56cf9-110">Ping</span><span class="sxs-lookup"><span data-stu-id="56cf9-110">Ping</span></span>](ping.md)                     | <span data-ttu-id="56cf9-111">Stellt eine Verbindung her und aushandiert die Sicherheit mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="56cf9-111">Establishes a connection and negotiates security with the server.</span></span>                                                                                              |
| [<span data-ttu-id="56cf9-112">Create-Session</span><span class="sxs-lookup"><span data-stu-id="56cf9-112">Create-Session</span></span>](create-session.md) | <span data-ttu-id="56cf9-113">Fordert eine Uploadsitzung mit dem BITS-Server an.</span><span class="sxs-lookup"><span data-stu-id="56cf9-113">Requests an upload session with the BITS server.</span></span>                                                                                                               |
| [<span data-ttu-id="56cf9-114">Fragment</span><span class="sxs-lookup"><span data-stu-id="56cf9-114">Fragment</span></span>](fragment.md)             | <span data-ttu-id="56cf9-115">Sendet ein Fragment der Datei an den BITS-Server.</span><span class="sxs-lookup"><span data-stu-id="56cf9-115">Sends a fragment of the file to the BITS server.</span></span> <span data-ttu-id="56cf9-116">Die Anzahl der gesendeten fragmentanforderungen hängt von der ausgewählten Fragmentgröße und der Größe der Uploaddatei ab.</span><span class="sxs-lookup"><span data-stu-id="56cf9-116">The number of fragment requests sent depends on the fragment size you choose and the size of the upload file.</span></span> |
| [<span data-ttu-id="56cf9-117">Sitzung schließen</span><span class="sxs-lookup"><span data-stu-id="56cf9-117">Close-Session</span></span>](close-session.md)   | <span data-ttu-id="56cf9-118">Beendet die dateiuploadsitzung mit dem BITS-Server.</span><span class="sxs-lookup"><span data-stu-id="56cf9-118">Ends the file upload session with the BITS server.</span></span>                                                                                                             |
| [<span data-ttu-id="56cf9-119">Abbrechen-Sitzung</span><span class="sxs-lookup"><span data-stu-id="56cf9-119">Cancel-Session</span></span>](cancel-session.md) | <span data-ttu-id="56cf9-120">Beendet die dateiuploadsitzung mit dem BITS-Server.</span><span class="sxs-lookup"><span data-stu-id="56cf9-120">Ends the file upload session with the BITS server.</span></span> <span data-ttu-id="56cf9-121">Normalerweise senden Sie das Cancel-Session Paket, wenn der Benutzer den Auftrag abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="56cf9-121">Typically, you send the Cancel-Session packet if the user canceled the job.</span></span>                                 |



 

<span data-ttu-id="56cf9-122">Das Ping-Paket ist optional.</span><span class="sxs-lookup"><span data-stu-id="56cf9-122">The Ping packet is optional.</span></span> <span data-ttu-id="56cf9-123">Anstatt ein Ping-Paket zu senden, können Sie das Create-Session Paket verwenden, um eine Verbindung herzustellen und Sicherheit auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="56cf9-123">Instead of sending a Ping packet, you can use the Create-Session packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="56cf9-124">Es ist jedoch effizienter, das Ping-Paket zu diesem Zweck zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="56cf9-124">However, it is more efficient to use the Ping packet for this purpose.</span></span>

 

 




