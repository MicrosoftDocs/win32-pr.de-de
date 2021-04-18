---
title: So verwenden Sie einen Skript Datenstrom
description: So verwenden Sie einen Skript Datenstrom
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media-Format-SDK, Skript Datenströme
- Advanced Systems Format (ASF), Skript Datenströme
- ASF (Advanced Systems Format), Skript Datenströme
- Skript Datenströme, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dee2c4a9789406c21b18c58a5f281a768fc713
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311447"
---
# <a name="to-use-a-script-stream"></a><span data-ttu-id="e6474-107">So verwenden Sie einen Skript Datenstrom</span><span class="sxs-lookup"><span data-stu-id="e6474-107">To Use a Script Stream</span></span>

<span data-ttu-id="e6474-108">In diesem Abschnitt wird beschrieben, wie Skript Daten für die Einbindung in eine Datei an den Writer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6474-108">This section describes how to send script data to the writer for inclusion in a file.</span></span> <span data-ttu-id="e6474-109">Informationen zum Einschließen von Skript Datenströmen in Profile finden Sie unter [Konfigurieren beliebiger Streamtypen](configuring-arbitrary-stream-types.md).</span><span class="sxs-lookup"><span data-stu-id="e6474-109">For information about including script streams in profiles, see [Configuring Arbitrary Stream Types](configuring-arbitrary-stream-types.md).</span></span>

<span data-ttu-id="e6474-110">Jedes Skript besteht aus zwei Zeichen folgen, einer *Typzeichenfolge* und einer *Argument* Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e6474-110">Each script consists of two strings, a *type* string and an *argument* string.</span></span>

<span data-ttu-id="e6474-111">Die Skript Daten müssen formatiert werden, bevor Sie an den Writer gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6474-111">The script data must be formatted before it is sent to the writer.</span></span> <span data-ttu-id="e6474-112">Die Zeichen folgen müssen verkettet werden, durch ein **null** -Zeichen getrennt und mit einem **null** -Zeichen beendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6474-112">The strings should be concatenated, separated by a **NULL** character, and terminated with a **NULL** character.</span></span> <span data-ttu-id="e6474-113">Das folgende Beispiel zeigt ein legitimer Skript:</span><span class="sxs-lookup"><span data-stu-id="e6474-113">The following example shows a legitimate script:</span></span>



|     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="e6474-114">U</span><span class="sxs-lookup"><span data-stu-id="e6474-114">U</span></span>   | <span data-ttu-id="e6474-115">R</span><span class="sxs-lookup"><span data-stu-id="e6474-115">R</span></span>   | <span data-ttu-id="e6474-116">L</span><span class="sxs-lookup"><span data-stu-id="e6474-116">L</span></span>   | <span data-ttu-id="e6474-117">\\0</span><span class="sxs-lookup"><span data-stu-id="e6474-117">\\0</span></span> | <span data-ttu-id="e6474-118">h.</span><span class="sxs-lookup"><span data-stu-id="e6474-118">h</span></span>   | <span data-ttu-id="e6474-119">t</span><span class="sxs-lookup"><span data-stu-id="e6474-119">t</span></span>   | <span data-ttu-id="e6474-120">t</span><span class="sxs-lookup"><span data-stu-id="e6474-120">t</span></span>   | <span data-ttu-id="e6474-121">p</span><span class="sxs-lookup"><span data-stu-id="e6474-121">p</span></span>   | <span data-ttu-id="e6474-122">:</span><span class="sxs-lookup"><span data-stu-id="e6474-122">:</span></span>   | /   | /   | <span data-ttu-id="e6474-123">w</span><span class="sxs-lookup"><span data-stu-id="e6474-123">w</span></span>   | <span data-ttu-id="e6474-124">w</span><span class="sxs-lookup"><span data-stu-id="e6474-124">w</span></span>   | <span data-ttu-id="e6474-125">w</span><span class="sxs-lookup"><span data-stu-id="e6474-125">w</span></span>   | <span data-ttu-id="e6474-126">.</span><span class="sxs-lookup"><span data-stu-id="e6474-126">.</span></span>   | <span data-ttu-id="e6474-127">a</span><span class="sxs-lookup"><span data-stu-id="e6474-127">a</span></span>   | <span data-ttu-id="e6474-128">d</span><span class="sxs-lookup"><span data-stu-id="e6474-128">d</span></span>   | <span data-ttu-id="e6474-129">a</span><span class="sxs-lookup"><span data-stu-id="e6474-129">a</span></span>   | <span data-ttu-id="e6474-130">t</span><span class="sxs-lookup"><span data-stu-id="e6474-130">t</span></span>   | <span data-ttu-id="e6474-131">u</span><span class="sxs-lookup"><span data-stu-id="e6474-131">u</span></span>   | <span data-ttu-id="e6474-132">m</span><span class="sxs-lookup"><span data-stu-id="e6474-132">m</span></span>   | <span data-ttu-id="e6474-133">.</span><span class="sxs-lookup"><span data-stu-id="e6474-133">.</span></span>   | <span data-ttu-id="e6474-134">c</span><span class="sxs-lookup"><span data-stu-id="e6474-134">c</span></span>   | <span data-ttu-id="e6474-135">o</span><span class="sxs-lookup"><span data-stu-id="e6474-135">o</span></span>   | <span data-ttu-id="e6474-136">m</span><span class="sxs-lookup"><span data-stu-id="e6474-136">m</span></span>   | <span data-ttu-id="e6474-137">\\0</span><span class="sxs-lookup"><span data-stu-id="e6474-137">\\0</span></span> |



 

<span data-ttu-id="e6474-138">Jedes Paar von Skript Befehlen sollte als Beispiel für den Writer geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e6474-138">Each pair of script commands should be written as a sample to the writer.</span></span> <span data-ttu-id="e6474-139">Weitere Informationen zum Schreiben von Beispielen finden [Sie unter so schreiben Sie Beispiele](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="e6474-139">For more information about writing samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="e6474-140">Beim Wiedergeben der ASF-Datei werden die Skript Befehle vom Reader (oder synchronen Reader) in der Präsentationszeit Reihenfolge übermittelt.</span><span class="sxs-lookup"><span data-stu-id="e6474-140">When the ASF file is played, the script commands will be delivered by the reader (or synchronous reader) in presentation time order.</span></span> <span data-ttu-id="e6474-141">Es liegt in der Verantwortung der Anwendung, die beiden Zeichen folgen zu analysieren und auf den Skript Befehl zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="e6474-141">It is the responsibility of the application to parse the two strings and respond to the script command.</span></span>

> [!Note]  
> <span data-ttu-id="e6474-142">Wenn Sie DRM zum Verschlüsseln einer Datei verwenden, kann kein Skript Befehl eine Präsentationszeit von 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e6474-142">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e6474-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6474-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6474-144">**Verwenden von Skript Befehlen**</span><span class="sxs-lookup"><span data-stu-id="e6474-144">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




