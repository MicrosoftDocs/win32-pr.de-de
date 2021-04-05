---
title: Funktions Aufrufattribute
description: Programme können diese Attribute für einzelne Funktionen innerhalb der Schnittstelle verwenden und nur diese Funktion betreffen.
ms.assetid: c54dbcd9-46c9-4755-b4a8-0f78068920b7
keywords:
- IDL-Mittell, Attribute, Funktionsaufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d53407abf464d7b201c49d9cb2b1d3f3625b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714082"
---
# <a name="function-call-attributes"></a><span data-ttu-id="69e5b-104">Funktions Aufrufattribute</span><span class="sxs-lookup"><span data-stu-id="69e5b-104">Function Call Attributes</span></span>

<span data-ttu-id="69e5b-105">Programme können diese Attribute für einzelne Funktionen innerhalb der Schnittstelle verwenden und nur diese Funktion betreffen.</span><span class="sxs-lookup"><span data-stu-id="69e5b-105">Programs can use these attributes on individual functions within the interface, and affect only that function.</span></span>



| <span data-ttu-id="69e5b-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="69e5b-106">Attribute</span></span>                        | <span data-ttu-id="69e5b-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="69e5b-107">Usage</span></span>                                                                                                                                                                                                                                                      |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69e5b-108">**Nachricht**</span><span class="sxs-lookup"><span data-stu-id="69e5b-108">**message**</span></span>](message.md)       | <span data-ttu-id="69e5b-109">Der Remote Prozedur Aufrufe muss als asynchrone Meldung vom Client an den Server behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="69e5b-109">The remote procedure call is to be treated as an asynchronous message from the client to the server.</span></span> <span data-ttu-id="69e5b-110">Der Client führt den-Rückruf aus und gibt sofort zurück, während der tatsächliche-Rückruf vom Message Queueing-Transport ([**ncadg \_ MQ**](ncadg-mq.md)) verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="69e5b-110">The client makes the call and returns immediately, while the actual call is handled by the message-queuing transport ([**ncadg\_mq**](ncadg-mq.md)).</span></span> |
| [<span data-ttu-id="69e5b-111">**auch**</span><span class="sxs-lookup"><span data-stu-id="69e5b-111">**maybe**</span></span>](maybe.md)           | <span data-ttu-id="69e5b-112">Der Client, der diesen Remote Prozedur Vorgang durchführt, erwartet keine Antwort, die die Übermittlung oder den Abschluss des Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="69e5b-112">The client making this remote procedure call does not expect any response indicating delivery or completion of the call.</span></span> <span data-ttu-id="69e5b-113">Dies steht im Gegensatz zu [**Nachrichten**](message.md) Vorgängen, bei denen keine Antwort erwartet wird, aber die Übermittlung gewährleistet ist.</span><span class="sxs-lookup"><span data-stu-id="69e5b-113">This is in contrast to [**message**](message.md) operations where no response is expected but the delivery is guaranteed.</span></span>        |
| [<span data-ttu-id="69e5b-114">**aus**</span><span class="sxs-lookup"><span data-stu-id="69e5b-114">**broadcast**</span></span>](broadcast.md)   | <span data-ttu-id="69e5b-115">Der Remote Prozedur Aufrufe muss an alle Server im Netzwerk gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="69e5b-115">The remote procedure call is to be sent to all of the servers on the network.</span></span> <span data-ttu-id="69e5b-116">Der Client akzeptiert die erste Rückgabe, nachfolgende Antworten von anderen Servern werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="69e5b-116">The client accepts the first return, subsequent replies from other servers are discarded.</span></span>                                                                                    |
| [<span data-ttu-id="69e5b-117">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="69e5b-117">**idempotent**</span></span>](idempotent.md) | <span data-ttu-id="69e5b-118">Der Aufruf ändert den Status nicht und gibt die gleichen Informationen zurück, wenn er mit denselben Eingabe Parametern aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="69e5b-118">The call does not change state and returns the same information each time it is called with the same input parameters.</span></span>                                                                                                                                     |
| [<span data-ttu-id="69e5b-119">**Rückruf**</span><span class="sxs-lookup"><span data-stu-id="69e5b-119">**callback**</span></span>](callback.md)     | <span data-ttu-id="69e5b-120">Gibt eine Funktion an, die sich in der Client Anwendung befindet, die der Server zum Abrufen von Informationen vom Client abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="69e5b-120">Designates a function that resides in the client application, which the server can call to obtain information from the client.</span></span>                                                                                                                             |
| [<span data-ttu-id="69e5b-121">**aufzurufen \_ als**</span><span class="sxs-lookup"><span data-stu-id="69e5b-121">**call\_as**</span></span>](call-as.md)      | <span data-ttu-id="69e5b-122">Ordnet einem Remote Prozedur aufzurufen eine nicht Remote fähige Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="69e5b-122">Maps a nonremotable function to a remote procedure call.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="69e5b-123">**nah**</span><span class="sxs-lookup"><span data-stu-id="69e5b-123">**local**</span></span>](local.md)           | <span data-ttu-id="69e5b-124">Gibt eine lokale Prozedur an, für die die-Klasse keinen Stub-Code generiert.</span><span class="sxs-lookup"><span data-stu-id="69e5b-124">Designates a local procedure for which MIDL does not generate stub code.</span></span>                                                                                                                                                                                   |



 

<span data-ttu-id="69e5b-125">Bei nicht-[**Objekt**](object.md) Schnittstellen können Sie auch das [**Kontext \_ handle**](context-handle.md) -Attribut auf eine Funktion anwenden, um die Eigenschaften des Rückgabewerts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="69e5b-125">On non-[**object**](object.md) interfaces, you can also apply the [**context\_handle**](context-handle.md) attribute to a function to specify characteristics of the return value.</span></span>

 

 




