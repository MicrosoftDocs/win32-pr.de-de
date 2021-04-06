---
title: MIDI-Streams
description: MIDI-Streams
ms.assetid: 622472d9-2888-407f-bdaa-4943896c0bac
keywords:
- Digital Instrumentation Digital Interface (MIDI), Streams
- MIDI (Digital Instrumentation Digital Interface), Streams
- Streampuffer, MIDI-Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4237e1590f3af2e15a3b0b9fedea2fea4c9c40fc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101595"
---
# <a name="midi-streams"></a><span data-ttu-id="ab490-106">MIDI-Streams</span><span class="sxs-lookup"><span data-stu-id="ab490-106">MIDI Streams</span></span>

<span data-ttu-id="ab490-107">MIDI-Ereignisse treten im Zusammenhang mit einem Stream von MIDI-Daten auf.</span><span class="sxs-lookup"><span data-stu-id="ab490-107">MIDI events occur in the context of a stream of MIDI data.</span></span> <span data-ttu-id="ab490-108">Obwohl eine Anwendung mehrere Streams zum Definieren von musikalischen Daten verwenden kann, erkennt der MIDI-Mapper nicht mehrere Datenströme.</span><span class="sxs-lookup"><span data-stu-id="ab490-108">Although an application can use several streams to define musical data, the MIDI mapper does not recognize multiple streams.</span></span> <span data-ttu-id="ab490-109">Die meisten Anwendungen, die Streams verwenden, verwenden einen einzelnen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="ab490-109">Most applications that use streams use a single MIDI stream.</span></span>

<span data-ttu-id="ab490-110">Die folgenden Funktionen können mit Streams verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab490-110">The following functions work with streams.</span></span>



| <span data-ttu-id="ab490-111">Wert</span><span class="sxs-lookup"><span data-stu-id="ab490-111">Value</span></span>                                            | <span data-ttu-id="ab490-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ab490-112">Meaning</span></span>                                                                 |
|--------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="ab490-113">**midistreamclose**</span><span class="sxs-lookup"><span data-stu-id="ab490-113">**midiStreamClose**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)       | <span data-ttu-id="ab490-114">Schließt einen MIDI-Stream.</span><span class="sxs-lookup"><span data-stu-id="ab490-114">Closes a MIDI stream.</span></span>                                                   |
| [<span data-ttu-id="ab490-115">**midistreamopen**</span><span class="sxs-lookup"><span data-stu-id="ab490-115">**midiStreamOpen**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)         | <span data-ttu-id="ab490-116">Öffnet einen MIDI-Stream und ruft ein Handle ab.</span><span class="sxs-lookup"><span data-stu-id="ab490-116">Opens a MIDI stream and retrieves a handle.</span></span>                             |
| [<span data-ttu-id="ab490-117">**midistreamout**</span><span class="sxs-lookup"><span data-stu-id="ab490-117">**midiStreamOut**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)           | <span data-ttu-id="ab490-118">Gibt einen Datenstrom (Puffer) von "MIDI"-Daten in einem MIDI-Ausgabegerät an</span><span class="sxs-lookup"><span data-stu-id="ab490-118">Plays or queues a stream (buffer) of MIDI data to a MIDI output device.</span></span> |
| [<span data-ttu-id="ab490-119">**midistreampause**</span><span class="sxs-lookup"><span data-stu-id="ab490-119">**midiStreamPause**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)       | <span data-ttu-id="ab490-120">Hält die Wiedergabe eines angegebenen MIDI-Streams an.</span><span class="sxs-lookup"><span data-stu-id="ab490-120">Pauses playback of a specified MIDI stream.</span></span>                             |
| [<span data-ttu-id="ab490-121">**midistreamposition**</span><span class="sxs-lookup"><span data-stu-id="ab490-121">**midiStreamPosition**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) | <span data-ttu-id="ab490-122">Ruft die aktuelle Position in einem MIDI-Stream ab.</span><span class="sxs-lookup"><span data-stu-id="ab490-122">Retrieves the current position in a MIDI stream.</span></span>                        |
| [<span data-ttu-id="ab490-123">**midistreamproperty**</span><span class="sxs-lookup"><span data-stu-id="ab490-123">**midiStreamProperty**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty) | <span data-ttu-id="ab490-124">Legt die streameigenschaften fest und ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="ab490-124">Sets and retrieves stream properties.</span></span>                                   |
| [<span data-ttu-id="ab490-125">**midistreamrestart**</span><span class="sxs-lookup"><span data-stu-id="ab490-125">**midiStreamRestart**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)   | <span data-ttu-id="ab490-126">Startet die Wiedergabe eines angehaltenen MIDI-Datenstroms neu.</span><span class="sxs-lookup"><span data-stu-id="ab490-126">Restarts playback of a paused MIDI stream.</span></span>                              |
| [<span data-ttu-id="ab490-127">**midistreamstoppt**</span><span class="sxs-lookup"><span data-stu-id="ab490-127">**midiStreamStop**</span></span>](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)         | <span data-ttu-id="ab490-128">Deaktiviert alle Notizen für alle MIDI-Kanäle für den angegebenen MIDI-Stream.</span><span class="sxs-lookup"><span data-stu-id="ab490-128">Turns off all notes on all MIDI channels for the specified MIDI stream.</span></span> |



 

 

 