---
title: Codierung der Variablen Bitrate (VBR)
description: Codierung der Variablen Bitrate (VBR)
ms.assetid: d3fe0cc6-64d7-44ce-8bb4-dd2eed021345
keywords:
- Windows Media-Format-SDK, VBR-Codierung
- Windows Media-Format-SDK, Variable Bitrate (VBR)
- Windows Media-Format-SDK, Qualitäts basierte VBR-Codierung
- Windows Media-Format-SDK, uneingeschränkte VBR-Codierung
- Windows Media-Format-SDK, eingeschränkte VBR-Codierung
- Codecs, VBR-Codierung
- Codecs, Variable Bitrate (VBR)
- Codecs, Qualitäts basierte VBR-Codierung
- Codecs, nicht eingeschränkte VBR-Codierung
- Codecs, eingeschränkte VBR-Codierung
- Variable Bitrate (VBR), Informationen zu
- VBR (Variable Bitrate), Informationen zu
- Qualitäts basierte VBR-Codierung, Informationen zu
- nicht eingeschränkte VBR-Codierung, Informationen zu
- eingeschränkte VBR-Codierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18b24a32b693cc4801f95695cc2d6e5f9ffa400c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341680"
---
# <a name="variable-bit-rate-vbr-encoding"></a><span data-ttu-id="defc5-118">Codierung der Variablen Bitrate (VBR)</span><span class="sxs-lookup"><span data-stu-id="defc5-118">Variable Bit Rate (VBR) Encoding</span></span>

<span data-ttu-id="defc5-119">Die VBR-Codierung (Variable Bitrate) ist eine Alternative zur konstanten Bitrate-Codierung (CBR) und wird von einigen Codecs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="defc5-119">Variable bit rate (VBR) encoding is an alternative to constant bit rate encoding (CBR) and is supported by some codecs.</span></span> <span data-ttu-id="defc5-120">Wenn die CBR-Codierung die Bitrate der codierten Medien beibehalten soll, strebt VBR die bestmögliche Qualität der codierten Medien an.</span><span class="sxs-lookup"><span data-stu-id="defc5-120">Where CBR encoding strives to maintain the bit rate of the encoded media, VBR strives to achieve the best possible quality of the encoded media.</span></span>

<span data-ttu-id="defc5-121">Die Qualität der codierten Inhalte hängt von der Menge der Daten ab, die bei der Komprimierung/Dekomprimierung der Inhalte verloren geht.</span><span class="sxs-lookup"><span data-stu-id="defc5-121">The quality of encoded content is determined by the amount of data that is lost when the content is compressed and decompressed.</span></span> <span data-ttu-id="defc5-122">Der Datenverlust bei der Komprimierung hängt von vielen Faktoren ab. Im Allgemeinen gehen jedoch umso mehr Details beim Komprimierungsprozess verloren, je komplexer die Ausgangsdaten und je höher die Komprimierungsrate ist.</span><span class="sxs-lookup"><span data-stu-id="defc5-122">Many factors affect the loss of data in the compression process, but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="defc5-123">Es gibt drei Arten von VBR-Codierung: Qualitäts basiert, nicht eingeschränkt und eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="defc5-123">There are three types of VBR encoding: quality-based, unconstrained, and constrained.</span></span>

## <a name="quality-based-vbr-encoding"></a><span data-ttu-id="defc5-124">Qualitäts basierte VBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="defc5-124">Quality-based VBR Encoding</span></span>

<span data-ttu-id="defc5-125">Der erste Typ der VBR-Codierung ist Qualitäts basiert und verwendet einen Codierungs Durchlauf.</span><span class="sxs-lookup"><span data-stu-id="defc5-125">The first type of VBR encoding is quality-based, which uses one encoding pass.</span></span> <span data-ttu-id="defc5-126">Bei der Qualitäts basierten VBR-Codierung können Sie eine Qualitätsstufe für einen digitalen Mediendaten Strom anstelle einer Bitrate angeben.</span><span class="sxs-lookup"><span data-stu-id="defc5-126">Quality-based VBR encoding enables you to specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="defc5-127">Der Codec codiert dann den Inhalt, sodass alle Beispiele eine vergleichbare Qualität haben.</span><span class="sxs-lookup"><span data-stu-id="defc5-127">The codec will then encode the content so that all samples are of comparable quality.</span></span>

<span data-ttu-id="defc5-128">Der Hauptvorteil der Qualitäts basierten VBR-Codierung besteht darin, dass die Qualität innerhalb einer Datei und von einer Datei zur nächsten konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="defc5-128">The main advantage of quality-based VBR encoding is that quality is consistent within a file and from one file to the next.</span></span> <span data-ttu-id="defc5-129">Beispielsweise können Sie ein Programm zum Kopieren von Liedern von CD in ASF-Dateien auf einem Computer schreiben.</span><span class="sxs-lookup"><span data-stu-id="defc5-129">For example, you can write a program to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="defc5-130">In diesem Fall ist die konsistente Qualität wahrscheinlich wichtiger für die Endbenutzer Leistung als die konsistente Dateigröße.</span><span class="sxs-lookup"><span data-stu-id="defc5-130">In this case, consistent quality is probably more important to the end-user experience than consistent file size.</span></span> <span data-ttu-id="defc5-131">Durch die Verwendung der Qualitäts basierten VBR-Codierung wird sichergestellt, dass alle kopierten Lieder dieselbe Qualität aufweisen.</span><span class="sxs-lookup"><span data-stu-id="defc5-131">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span>

<span data-ttu-id="defc5-132">Der Nachteil der Qualitäts basierten VBR-Codierung besteht darin, dass es keine Möglichkeit gibt, die Größen-oder Bandbreitenanforderungen der codierten Medien vor der Codierung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="defc5-132">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before encoding.</span></span> <span data-ttu-id="defc5-133">Dadurch können Qualitäts basierte VBR-codierte Dateien für Situationen ungeeignet werden, in denen der Arbeitsspeicher oder die Bandbreite eingeschränkt ist, z. b. Portable Media Player oder Internet Verbindungen mit geringer Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="defc5-133">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as portable media players, or low-bandwidth Internet connections.</span></span>

<span data-ttu-id="defc5-134">Im Allgemeinen eignet sich die Qualitäts basierte VBR-Codierung gut für die lokale Wiedergabe oder Netzwerkverbindungen mit hoher Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="defc5-134">In general, quality-based VBR encoding is well suited for local playback or high bandwidth network connections.</span></span> <span data-ttu-id="defc5-135">In diesen Fällen bietet die konsistente Qualität eine bessere Benutzer Leistung.</span><span class="sxs-lookup"><span data-stu-id="defc5-135">In those cases, the consistent quality will provide a better user experience.</span></span>

## <a name="unconstrained-vbr-encoding"></a><span data-ttu-id="defc5-136">Nicht eingeschränkte VBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="defc5-136">Unconstrained VBR Encoding</span></span>

<span data-ttu-id="defc5-137">Bei der uneingeschränkten VBR-Codierung werden zwei Codierungs Durchgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="defc5-137">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="defc5-138">Wenn Sie die nicht eingeschränkte VBR-Codierung verwenden, geben Sie wie bei der CBR-Codierung eine Bitrate für den Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="defc5-138">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with CBR encoding.</span></span> <span data-ttu-id="defc5-139">Der Codec verwendet diesen Wert jedoch nur als durchschnittliche Bitrate für den Stream und codiert, sodass die Qualität so hoch wie möglich ist, während der Durchschnitt beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="defc5-139">However, the codec uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="defc5-140">Die tatsächliche Bitrate an einem beliebigen Punkt im codierten Stream kann stark vom Durchschnittswert abweichen.</span><span class="sxs-lookup"><span data-stu-id="defc5-140">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span>

<span data-ttu-id="defc5-141">Sie legen kein Puffer Fenster für die unbeschränkte VBR-Codierung fest, wie es bei einem CBR-codierten Stream der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="defc5-141">You do not set a buffer window for unconstrained VBR encoding as you would for a CBR-encoded stream.</span></span> <span data-ttu-id="defc5-142">Stattdessen berechnet der Codec die Größe des erforderlichen Puffer Fensters basierend auf den Anforderungen der codierten Stichproben.</span><span class="sxs-lookup"><span data-stu-id="defc5-142">Instead, the codec computes the size of the required buffer window based on the requirements of the encoded samples.</span></span>

<span data-ttu-id="defc5-143">Der Vorteil der uneingeschränkten VBR-Codierung besteht darin, dass der komprimierte Datenstrom die höchste mögliche Qualität aufweist und gleichzeitig in einer vorhersagbaren durchschnittlichen Bandbreite bleibt.</span><span class="sxs-lookup"><span data-stu-id="defc5-143">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span>

## <a name="constrained-vbr-encoding"></a><span data-ttu-id="defc5-144">Eingeschränkte VBR-Codierung</span><span class="sxs-lookup"><span data-stu-id="defc5-144">Constrained VBR Encoding</span></span>

<span data-ttu-id="defc5-145">Die eingeschränkte VBR-Codierung ist mit der nicht eingeschränkten VBR-Codierung identisch, mit der Ausnahme, dass Sie eine maximale Bitrate und ein maximales Puffer Fenster im Profil angeben.</span><span class="sxs-lookup"><span data-stu-id="defc5-145">Constrained VBR encoding is identical to unconstrained VBR encoding, except that you specify a maximum bit rate and a maximum buffer window in the profile.</span></span> <span data-ttu-id="defc5-146">Der Codec verwendet dann die maximalen Werte, um zu bestimmen, wie die Daten komprimiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="defc5-146">The codec then uses the maximum values to determine how to compress the data.</span></span> <span data-ttu-id="defc5-147">Wenn Sie die maximalen Werte hoch genug festlegen, erzeugt die eingeschränkte VBR-Codierung denselben codierten Stream wie die uneingeschränkte VBR-Codierung.</span><span class="sxs-lookup"><span data-stu-id="defc5-147">If you set the maximum values high enough, constrained VBR encoding will produce the same encoded stream as unconstrained VBR encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="defc5-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="defc5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="defc5-149">**Auswählen einer Codierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="defc5-149">**Choosing an Encoding Method**</span></span>](choosing-an-encoding-method.md)
</dt> <dt>

[<span data-ttu-id="defc5-150">**Codec-Features**</span><span class="sxs-lookup"><span data-stu-id="defc5-150">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="defc5-151">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="defc5-151">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="defc5-152">**Konfigurieren von VBR-Streams**</span><span class="sxs-lookup"><span data-stu-id="defc5-152">**Configuring VBR Streams**</span></span>](configuring-vbr-streams.md)
</dt> <dt>

[<span data-ttu-id="defc5-153">**Codierung mit konstanter Bitrate (CBR)**</span><span class="sxs-lookup"><span data-stu-id="defc5-153">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="defc5-154">**Zwei-Pass-Codierung**</span><span class="sxs-lookup"><span data-stu-id="defc5-154">**Two-Pass Encoding**</span></span>](two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="defc5-155">**Verwenden von Two-Pass Codierung**</span><span class="sxs-lookup"><span data-stu-id="defc5-155">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> </dl>

 

 




