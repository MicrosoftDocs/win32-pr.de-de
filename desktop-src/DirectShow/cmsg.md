---
description: Die cmsgthread-Klasse bietet Unterstützung für einen Arbeits Thread, an den Anforderungen asynchron gesendet werden können, anstatt direkt gesendet zu werden.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMSG-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345593"
---
# <a name="cmsg-class"></a><span data-ttu-id="b23ce-103">CMSG-Klasse</span><span class="sxs-lookup"><span data-stu-id="b23ce-103">CMsg class</span></span>

<span data-ttu-id="b23ce-104">Die [**cmsgthread**](cmsgthread.md) -Klasse bietet Unterstützung für einen Arbeits Thread, an den Anforderungen asynchron gesendet werden können, anstatt direkt gesendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="b23ce-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="b23ce-105">Die [**camthread**](camthread.md) -Klasse stellt einen Arbeits Thread bereit, an den einzelne Anforderungen gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b23ce-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="b23ce-106">Nur ein Client kann eine Anforderung gleichzeitig ausführen, und der Client wird blockiert, bis der Arbeits Thread die Anforderung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="b23ce-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="b23ce-107">Im Gegensatz dazu stellt die **cmsgthread** -Klasse einen Arbeits Thread bereit, an den eine beliebige Anzahl von Anforderungen gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b23ce-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="b23ce-108">Die Anforderungen (in Form eines- `CMsg` Objekts) werden in der Reihenfolge asynchron in die Warteschlange eingereiht und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b23ce-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="b23ce-109">Es wird keine Antwort oder kein Rückgabewert empfangen.</span><span class="sxs-lookup"><span data-stu-id="b23ce-109">No reply or return value is received.</span></span>



| <span data-ttu-id="b23ce-110">Datenelemente</span><span class="sxs-lookup"><span data-stu-id="b23ce-110">Data Members</span></span>              | <span data-ttu-id="b23ce-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b23ce-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b23ce-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="b23ce-112">dwFlags</span></span>                   | <span data-ttu-id="b23ce-113">Markieren Sie den Parameter für den Anforderungs Code.</span><span class="sxs-lookup"><span data-stu-id="b23ce-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="b23ce-114">lpparam</span><span class="sxs-lookup"><span data-stu-id="b23ce-114">lpParam</span></span>                   | <span data-ttu-id="b23ce-115">Daten, die vom Arbeits Thread als Parameter oder Rückgabewerte benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="b23ce-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="b23ce-116">Diese Daten sollten nicht Stapel basiert sein, da nach Abschluss des Warteschlangen Vorgangs einige Zeit darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b23ce-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="b23ce-117">Peer Event</span><span class="sxs-lookup"><span data-stu-id="b23ce-117">pEvent</span></span>                    | <span data-ttu-id="b23ce-118">Ereignis Objekt, das ein Arbeits Thread signalisieren kann, um den Abschluss des Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="b23ce-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="b23ce-119">Umschlag</span><span class="sxs-lookup"><span data-stu-id="b23ce-119">uMsg</span></span>                      | <span data-ttu-id="b23ce-120">Anforderungs Code, der vom Client der Thread Klasse definiert und von der überschriebenen Arbeits Thread Funktion verstanden wird.</span><span class="sxs-lookup"><span data-stu-id="b23ce-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="b23ce-121">Elementfunktionen</span><span class="sxs-lookup"><span data-stu-id="b23ce-121">Member Functions</span></span>          | <span data-ttu-id="b23ce-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b23ce-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="b23ce-123">**CMSG**</span><span class="sxs-lookup"><span data-stu-id="b23ce-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="b23ce-124">Erstellt ein [**CMSG**](cmsg-cmsg.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b23ce-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



