---
title: Auswählen einer Codierungsmethode
description: Auswählen einer Codierungsmethode
ms.assetid: 095245a6-39eb-4228-86ac-ade94dde3695
keywords:
- Profile, auswählen von Codierungs Methoden
- Profile, Codierungs Methoden
- Codecs, auswählen von Codierungs Methoden
- Codecs, Codierungs Methoden
- Profile, auswählen von Codierungs Methoden
- Codecs, auswählen von Codierungs Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54c5bd099e5aaf8b3a735594c8b87a335fc2594
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337982"
---
# <a name="choosing-an-encoding-method"></a><span data-ttu-id="52df4-109">Auswählen einer Codierungsmethode</span><span class="sxs-lookup"><span data-stu-id="52df4-109">Choosing an Encoding Method</span></span>

<span data-ttu-id="52df4-110">Einige Codecs, wie der Windows Media Video 9-Codec, unterstützen mehrere Codierungs Methoden.</span><span class="sxs-lookup"><span data-stu-id="52df4-110">Some codecs, like the Windows Media Video 9 codec, support multiple encoding methods.</span></span> <span data-ttu-id="52df4-111">Die Codierungsmethode, die Sie für einen Stream auswählen, hängt davon ab, wie der Stream übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52df4-111">The encoding method that you choose for a stream will depend upon how the stream is to be delivered.</span></span> <span data-ttu-id="52df4-112">In der folgenden Tabelle wird beschrieben, wann die verschiedenen Codierungs Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="52df4-112">The following table describes when to use the various encoding methods.</span></span>



| <span data-ttu-id="52df4-113">Codiermethode</span><span class="sxs-lookup"><span data-stu-id="52df4-113">Encoding method</span></span>                | <span data-ttu-id="52df4-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="52df4-114">Description</span></span>                                                                                                                                                                                       |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52df4-115">1-Pass-Konstante Bitrate (CBR)</span><span class="sxs-lookup"><span data-stu-id="52df4-115">1-pass Constant Bit Rate (CBR)</span></span> | <span data-ttu-id="52df4-116">Die einzige Option für Live Streaming.</span><span class="sxs-lookup"><span data-stu-id="52df4-116">The only option for live streaming.</span></span> <span data-ttu-id="52df4-117">Codiert in eine vorhersagbare Bitrate und bietet die niedrigste Qualität aller Codierungs Methoden.</span><span class="sxs-lookup"><span data-stu-id="52df4-117">Encodes to a predictable bit rate and delivers the lowest quality of all encoding methods.</span></span>                                                                    |
| <span data-ttu-id="52df4-118">2-Pass-CBR</span><span class="sxs-lookup"><span data-stu-id="52df4-118">2-pass CBR</span></span>                     | <span data-ttu-id="52df4-119">Verwenden Sie für Dateien, die über ein Netzwerk an einen Client Leser gestreamt werden, aber nicht von einer Live Quelle übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="52df4-119">Use for files that will be streamed over a network to a client reader, but that are not broadcast from a live source.</span></span> <span data-ttu-id="52df4-120">Codiert in eine vorhersagbare Bitrate, aber mit besserer Qualität als 1-Pass-CBR.</span><span class="sxs-lookup"><span data-stu-id="52df4-120">Encodes to a predictable bit rate, but with better quality than 1-pass CBR.</span></span> |
| <span data-ttu-id="52df4-121">1-Pass-Variable Bitrate (VBR)</span><span class="sxs-lookup"><span data-stu-id="52df4-121">1-pass Variable Bit Rate (VBR)</span></span> | <span data-ttu-id="52df4-122">Verwenden Sie, wenn Sie die Qualität der codierten Ausgabe angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="52df4-122">Use when you need to specify the quality of the encoded output.</span></span> <span data-ttu-id="52df4-123">Bietet die konsistente Qualität aller Codierungs Methoden.</span><span class="sxs-lookup"><span data-stu-id="52df4-123">Delivers the most consistent quality of all encoding methods.</span></span> <span data-ttu-id="52df4-124">Wird nur für lokale Dateien oder zum Herunterladen verwendet.</span><span class="sxs-lookup"><span data-stu-id="52df4-124">Use only for local files or for downloading.</span></span>                        |
| <span data-ttu-id="52df4-125">2-Pass-VBR – nicht eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="52df4-125">2-pass VBR – unconstrained</span></span>     | <span data-ttu-id="52df4-126">Verwenden Sie, wenn Sie eine Bandbreite angeben müssen, aber Schwankungen in Bezug auf die angegebene Bandbreite sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="52df4-126">Use when you need to specify a bandwidth, but fluctuations around the specified bandwidth are acceptable.</span></span> <span data-ttu-id="52df4-127">Für lokale Dateien oder nur herunterladen.</span><span class="sxs-lookup"><span data-stu-id="52df4-127">For local files or downloading only.</span></span>                                                    |
| <span data-ttu-id="52df4-128">2-Pass-VBR – eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="52df4-128">2-pass VBR – constrained</span></span>       | <span data-ttu-id="52df4-129">Verwenden Sie unter denselben Bedingungen wie nicht eingeschränkt, aber wenn Sie eine maximale momentane Bitrate angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="52df4-129">Use under the same circumstances as unconstrained, but when you need to specify a maximum momentary bit rate.</span></span> <span data-ttu-id="52df4-130">Für lokale Dateien oder nur herunterladen.</span><span class="sxs-lookup"><span data-stu-id="52df4-130">For local files or downloading only.</span></span>                                                |



 

<span data-ttu-id="52df4-131">In der folgenden Tabelle werden die Codierungs Methoden aufgelistet, die von den Codecs unterstützt werden, die mit dem Windows Media-Format SDK ausgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="52df4-131">The following table lists the encoding methods that are supported by the codecs that ship with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="52df4-132">Codec</span><span class="sxs-lookup"><span data-stu-id="52df4-132">Codec</span></span>                                  | <span data-ttu-id="52df4-133">CBR</span><span class="sxs-lookup"><span data-stu-id="52df4-133">CBR</span></span> | <span data-ttu-id="52df4-134">2-Pass-CBR</span><span class="sxs-lookup"><span data-stu-id="52df4-134">2-pass CBR</span></span> | <span data-ttu-id="52df4-135">VBR</span><span class="sxs-lookup"><span data-stu-id="52df4-135">VBR</span></span> | <span data-ttu-id="52df4-136">2-Pass-VBR</span><span class="sxs-lookup"><span data-stu-id="52df4-136">2-pass VBR</span></span> |
|----------------------------------------|-----|------------|-----|------------|
| <span data-ttu-id="52df4-137">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="52df4-137">Windows Media Video 9</span></span>                  | <span data-ttu-id="52df4-138">X</span><span class="sxs-lookup"><span data-stu-id="52df4-138">X</span></span>   | <span data-ttu-id="52df4-139">X</span><span class="sxs-lookup"><span data-stu-id="52df4-139">X</span></span>          | <span data-ttu-id="52df4-140">X</span><span class="sxs-lookup"><span data-stu-id="52df4-140">X</span></span>   | <span data-ttu-id="52df4-141">X</span><span class="sxs-lookup"><span data-stu-id="52df4-141">X</span></span>          |
| <span data-ttu-id="52df4-142">Windows Media Audio 9 und höher</span><span class="sxs-lookup"><span data-stu-id="52df4-142">Windows Media Audio 9 and later</span></span>        | <span data-ttu-id="52df4-143">X</span><span class="sxs-lookup"><span data-stu-id="52df4-143">X</span></span>   | <span data-ttu-id="52df4-144">X</span><span class="sxs-lookup"><span data-stu-id="52df4-144">X</span></span>          | <span data-ttu-id="52df4-145">X</span><span class="sxs-lookup"><span data-stu-id="52df4-145">X</span></span>   | <span data-ttu-id="52df4-146">X</span><span class="sxs-lookup"><span data-stu-id="52df4-146">X</span></span>          |
| <span data-ttu-id="52df4-147">Windows Media Video 9-Bildschirm</span><span class="sxs-lookup"><span data-stu-id="52df4-147">Windows Media Video 9 Screen</span></span>           | <span data-ttu-id="52df4-148">X</span><span class="sxs-lookup"><span data-stu-id="52df4-148">X</span></span>   |            | <span data-ttu-id="52df4-149">X</span><span class="sxs-lookup"><span data-stu-id="52df4-149">X</span></span>   |            |
| <span data-ttu-id="52df4-150">Windows Media Audio 9-Stimme</span><span class="sxs-lookup"><span data-stu-id="52df4-150">Windows Media Audio 9 Voice</span></span>            | <span data-ttu-id="52df4-151">X</span><span class="sxs-lookup"><span data-stu-id="52df4-151">X</span></span>   |            |     |            |
| <span data-ttu-id="52df4-152">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="52df4-152">Windows Media Audio Professional</span></span>       | <span data-ttu-id="52df4-153">X</span><span class="sxs-lookup"><span data-stu-id="52df4-153">X</span></span>   | <span data-ttu-id="52df4-154">X</span><span class="sxs-lookup"><span data-stu-id="52df4-154">X</span></span>          | <span data-ttu-id="52df4-155">X</span><span class="sxs-lookup"><span data-stu-id="52df4-155">X</span></span>   | <span data-ttu-id="52df4-156">X</span><span class="sxs-lookup"><span data-stu-id="52df4-156">X</span></span>          |
| <span data-ttu-id="52df4-157">Verlust von Windows Media Audio Verlust</span><span class="sxs-lookup"><span data-stu-id="52df4-157">Windows Media Audio Lossless</span></span>           |     |            | <span data-ttu-id="52df4-158">X</span><span class="sxs-lookup"><span data-stu-id="52df4-158">X</span></span>   |            |
| <span data-ttu-id="52df4-159">Windows Media Video 9-Image und höher</span><span class="sxs-lookup"><span data-stu-id="52df4-159">Windows Media Video 9 Image and later</span></span>  | <span data-ttu-id="52df4-160">X</span><span class="sxs-lookup"><span data-stu-id="52df4-160">X</span></span>   |            | <span data-ttu-id="52df4-161">X</span><span class="sxs-lookup"><span data-stu-id="52df4-161">X</span></span>   |            |
| <span data-ttu-id="52df4-162">Erweiterte profile Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="52df4-162">Windows Media Video 9 Advanced Profile</span></span> | <span data-ttu-id="52df4-163">X</span><span class="sxs-lookup"><span data-stu-id="52df4-163">X</span></span>   | <span data-ttu-id="52df4-164">X</span><span class="sxs-lookup"><span data-stu-id="52df4-164">X</span></span>          | <span data-ttu-id="52df4-165">X</span><span class="sxs-lookup"><span data-stu-id="52df4-165">X</span></span>   | <span data-ttu-id="52df4-166">X</span><span class="sxs-lookup"><span data-stu-id="52df4-166">X</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="52df4-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52df4-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52df4-168">**Entwerfen von Profilen**</span><span class="sxs-lookup"><span data-stu-id="52df4-168">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="52df4-169">**Codierung mit konstanter Bitrate (CBR)**</span><span class="sxs-lookup"><span data-stu-id="52df4-169">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="52df4-170">**Zwei-Pass-Codierung**</span><span class="sxs-lookup"><span data-stu-id="52df4-170">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="52df4-171">**Codierung der Variablen Bitrate (VBR)**</span><span class="sxs-lookup"><span data-stu-id="52df4-171">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




