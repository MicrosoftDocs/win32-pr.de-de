---
title: Bits-Antwort Pakete
description: Bits-Antwort Pakete
ms.assetid: 30755476-daa9-42ea-8fb3-5b505fc9dd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755e28b749d201a2c90640ea9e456f012f790453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855484"
---
# <a name="bits-response-packets"></a><span data-ttu-id="af1cc-103">Bits-Antwort Pakete</span><span class="sxs-lookup"><span data-stu-id="af1cc-103">BITS Response Packets</span></span>

<span data-ttu-id="af1cc-104">In der folgenden Tabelle sind die Antwort Pakete aufgelistet, die für Upload-und Upload-Reply-Aufträge an den Bits-Client gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="af1cc-104">The following table lists the response packets sent to the BITS client for upload and upload-reply jobs.</span></span> <span data-ttu-id="af1cc-105">In der Tabelle werden die Pakete in der typischen Reihenfolge aufgelistet, an die Sie an den Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="af1cc-105">The table lists the packets in the typical sequence they are sent to the client.</span></span>



| <span data-ttu-id="af1cc-106">Antwortpaket</span><span class="sxs-lookup"><span data-stu-id="af1cc-106">Response packet</span></span>                                      | <span data-ttu-id="af1cc-107">Zweck</span><span class="sxs-lookup"><span data-stu-id="af1cc-107">Purpose</span></span>                                                                                                                                                                                     |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="af1cc-108">Bestätigung für Ping</span><span class="sxs-lookup"><span data-stu-id="af1cc-108">Ack for Ping</span></span>](ack-for-ping.md)                     | <span data-ttu-id="af1cc-109">Bestätigt die [Ping](ping.md) -Anforderung.</span><span class="sxs-lookup"><span data-stu-id="af1cc-109">Acknowledges the [Ping](ping.md) request.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="af1cc-110">Bestätigung für Create-Session</span><span class="sxs-lookup"><span data-stu-id="af1cc-110">Ack for Create-Session</span></span>](ack-for-create-session.md) | <span data-ttu-id="af1cc-111">Bestätigt die [Create-Session-](create-session.md) Anforderung und gibt einen Sitzungs Bezeichner zurück, den der BITS-Client für alle nachfolgenden Anforderungen verwendet, um diese Datei Übertragungs Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="af1cc-111">Acknowledges the [Create-Session](create-session.md) request and returns a session identifier that the BITS client uses on all subsequent requests to identify this file transfer session.</span></span> |
| [<span data-ttu-id="af1cc-112">Bestätigung für Fragment</span><span class="sxs-lookup"><span data-stu-id="af1cc-112">Ack for Fragment</span></span>](ack-for-fragment.md)             | <span data-ttu-id="af1cc-113">Bestätigt die [fragmentanforderung](fragment.md) und schreibt das Fragment in die Uploaddatei auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="af1cc-113">Acknowledges the [Fragment](fragment.md) request and writes the fragment to the upload file on the server.</span></span>                                                                                 |
| [<span data-ttu-id="af1cc-114">Bestätigung für Close-Session</span><span class="sxs-lookup"><span data-stu-id="af1cc-114">Ack for Close-Session</span></span>](ack-for-close-session.md)   | <span data-ttu-id="af1cc-115">Bestätigt die Anforderung zum [Schließen der Sitzung](close-session.md) und gibt alle der Sitzung zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="af1cc-115">Acknowledges the [Close-Session](close-session.md) request and releases all resources associated with the session.</span></span>                                                                         |
| [<span data-ttu-id="af1cc-116">Bestätigung für Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="af1cc-116">Ack for Cancel-Session</span></span>](ack-for-cancel-session.md) | <span data-ttu-id="af1cc-117">Bestätigt die [Abbruch Sitzungs](cancel-session.md) Anforderung und gibt alle der Sitzung zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="af1cc-117">Acknowledges the [Cancel-Session](cancel-session.md) request and releases all resources associated with the session.</span></span>                                                                       |



 

 

 




