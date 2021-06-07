---
title: So verwenden Sie einen Skriptstream
description: So verwenden Sie einen Skriptstream
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, Skriptstreams
- Advanced Systems Format (ASF), Skriptstreams
- ASF (Advanced Systems Format), Skriptstreams
- Skriptstreams, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444731"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="44676-107">So verwenden Sie einen Skriptstream</span><span class="sxs-lookup"><span data-stu-id="44676-107">To Use a Script Stream</span></span>

<span data-ttu-id="44676-108">In diesem Abschnitt wird beschrieben, wie Skriptdaten zur Aufnahme in eine Datei an den Writer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="44676-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="44676-109">Informationen zum Verwenden von Skriptstreams in Profile finden Sie unter Configuring Arbitrary Stream Types (Konfigurieren [beliebiger Streamtypen).](configuring-arbitrary-stream-types.md)</span><span class="sxs-lookup"><span data-stu-id="44676-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="44676-110">Jedes Skript besteht aus zwei Zeichenfolgen, einer *Typzeichenfolge* und einer *Argumentzeichenfolge.*</span><span class="sxs-lookup"><span data-stu-id="44676-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="44676-111">Die Skriptdaten müssen formatiert werden, bevor sie an den Writer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="44676-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="44676-112">Die Zeichenfolgen sollten verkettet, durch ein **NULL-Zeichen** getrennt und mit einem **NULL-Zeichen beendet** werden.</span><span class="sxs-lookup"><span data-stu-id="44676-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="44676-113">Das folgende Beispiel zeigt ein legitimes Skript:</span><span class="sxs-lookup"><span data-stu-id="44676-113">The following example shows a legitimate script:</span></span>



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="44676-114">U</span><span class="sxs-lookup"><span data-stu-id="44676-114">U</span></span>   | <span data-ttu-id="44676-115">R</span><span class="sxs-lookup"><span data-stu-id="44676-115">R</span></span>   | <span data-ttu-id="44676-116">L</span><span class="sxs-lookup"><span data-stu-id="44676-116">L</span></span>   | &nbsp; | <span data-ttu-id="44676-117">h</span><span class="sxs-lookup"><span data-stu-id="44676-117">h</span></span>   | <span data-ttu-id="44676-118">t</span><span class="sxs-lookup"><span data-stu-id="44676-118">t</span></span>   | <span data-ttu-id="44676-119">t</span><span class="sxs-lookup"><span data-stu-id="44676-119">t</span></span>   | <span data-ttu-id="44676-120">p</span><span class="sxs-lookup"><span data-stu-id="44676-120">p</span></span>   | <span data-ttu-id="44676-121">:</span><span class="sxs-lookup"><span data-stu-id="44676-121">:</span></span>   | /   | /   | <span data-ttu-id="44676-122">w</span><span class="sxs-lookup"><span data-stu-id="44676-122">w</span></span>   | <span data-ttu-id="44676-123">w</span><span class="sxs-lookup"><span data-stu-id="44676-123">w</span></span>   | <span data-ttu-id="44676-124">w</span><span class="sxs-lookup"><span data-stu-id="44676-124">w</span></span>   | <span data-ttu-id="44676-125">.</span><span class="sxs-lookup"><span data-stu-id="44676-125">.</span></span>   | <span data-ttu-id="44676-126">a</span><span class="sxs-lookup"><span data-stu-id="44676-126">a</span></span>   | <span data-ttu-id="44676-127">d</span><span class="sxs-lookup"><span data-stu-id="44676-127">d</span></span>   | <span data-ttu-id="44676-128">a</span><span class="sxs-lookup"><span data-stu-id="44676-128">a</span></span>   | <span data-ttu-id="44676-129">t</span><span class="sxs-lookup"><span data-stu-id="44676-129">t</span></span>   | <span data-ttu-id="44676-130">u</span><span class="sxs-lookup"><span data-stu-id="44676-130">u</span></span>   | <span data-ttu-id="44676-131">m</span><span class="sxs-lookup"><span data-stu-id="44676-131">m</span></span>   | <span data-ttu-id="44676-132">.</span><span class="sxs-lookup"><span data-stu-id="44676-132">.</span></span>   | <span data-ttu-id="44676-133">c</span><span class="sxs-lookup"><span data-stu-id="44676-133">c</span></span>   | <span data-ttu-id="44676-134">o</span><span class="sxs-lookup"><span data-stu-id="44676-134">o</span></span>   | <span data-ttu-id="44676-135">m</span><span class="sxs-lookup"><span data-stu-id="44676-135">m</span></span>   | &nbsp; |



 

<span data-ttu-id="44676-136">Jedes Skriptbefehlspaar sollte als Beispiel in den Writer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="44676-136">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="44676-137">Weitere Informationen zum Schreiben von Beispielen finden Sie unter [To Write Samples](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="44676-137">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="44676-138">Wenn die ASF-Datei abgespielt wird, werden die Skriptbefehle vom Reader (oder synchronen Reader) in der Reihenfolge der Präsentationszeit übermittelt.</span><span class="sxs-lookup"><span data-stu-id="44676-138">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="44676-139">Die Anwendung ist dafür verantwortlich, die beiden Zeichenfolgen zu analysieren und auf den Skriptbefehl zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="44676-139">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="44676-140">Bei Verwendung von DRM zum Verschlüsseln einer Datei kann kein Skriptbefehl eine Präsentationszeit von 0 haben.</span><span class="sxs-lookup"><span data-stu-id="44676-140">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="44676-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44676-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44676-142">**Verwenden von Skriptbefehlen**</span><span class="sxs-lookup"><span data-stu-id="44676-142">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




