---
description: Wenn ich VBR mit hoher Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codec-Objekt abgerufen wird, größer als die Spitzen Bitrate.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Wenn ich VBR mit hoher Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codec-Objekt abgerufen wird, größer als die Spitzen Bitrate. Wie ist das möglich?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344839"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a><span data-ttu-id="90cd6-104">Wenn ich VBR mit hoher Auslastung verwende, ist die durchschnittliche Bitrate, die vom Codec-Objekt abgerufen wird, größer als die Spitzen Bitrate.</span><span class="sxs-lookup"><span data-stu-id="90cd6-104">When I use peak-constrained VBR, the average bit rate retrieved from the codec object is larger than the peak bit rate.</span></span> <span data-ttu-id="90cd6-105">Wie ist das möglich?</span><span class="sxs-lookup"><span data-stu-id="90cd6-105">How is that possible?</span></span>

<span data-ttu-id="90cd6-106">Die Beziehung zwischen der durchschnittlichen Bitrate und der Spitzen Bitrate wird häufig falsch verstanden.</span><span class="sxs-lookup"><span data-stu-id="90cd6-106">The relationship between the average bit rate and the peak bit rate is often misunderstood.</span></span> <span data-ttu-id="90cd6-107">Die Spitzen Bitrate beschreibt eine Puffer Einschränkung über einen Zeitraum, der durch das Hauptpuffer Fenster angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="90cd6-107">The peak bit rate describes a buffer constraint over a period of time specified by the peak buffer window.</span></span> <span data-ttu-id="90cd6-108">Die durchschnittliche Bitrate für die zweistufige VBR (uneingeschränkt oder mit hoher Einschränkung) ist die durchschnittliche Bits pro Sekunde während der Dauer der Datei.</span><span class="sxs-lookup"><span data-stu-id="90cd6-108">The average bit rate for two-pass VBR (unconstrained or peak-constrained) is the average bits per second over the duration of the file.</span></span>

<span data-ttu-id="90cd6-109">Die tatsächliche Bitrate, die für eine Zeitspanne gleich dem Puffer Fenster verwendet [wird, kann die doppelte](the-leaky-bucket-buffer-model.md)Bitrate erreichen.</span><span class="sxs-lookup"><span data-stu-id="90cd6-109">As described in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), the actual bit rate used over a period of time equal to the buffer window can approach twice the bit rate.</span></span> <span data-ttu-id="90cd6-110">Dies liegt daran, dass der Puffer, der als Anzahl von Bits definiert ist, die gleich der Bitrate für das Puffer Fenster (in Sekunden) ist, mit konstanter Geschwindigkeit geleert wird.</span><span class="sxs-lookup"><span data-stu-id="90cd6-110">This is because the buffer, defined as a number of bits equal to the bit rate times the buffer window (in seconds), is being emptied at a constant rate.</span></span>

<span data-ttu-id="90cd6-111">Beispielsweise erstellt der Encoder in einer Sekunde eines 56-Kbit/s-Streams Stichproben mit einer Gesamtgröße von 59 KB.</span><span class="sxs-lookup"><span data-stu-id="90cd6-111">For example, in one second of a 56 Kbps stream, the encoder creates samples totaling 59 Kb.</span></span> <span data-ttu-id="90cd6-112">Somit werden 56 KB Daten aus dem Puffer in dieser Sekunde entfernt, wobei 3 KB im Puffer belassen werden.</span><span class="sxs-lookup"><span data-stu-id="90cd6-112">So, 56 Kb of data is removed from the buffer in that second, leaving 3 Kb in the buffer.</span></span> <span data-ttu-id="90cd6-113">Wenn der Stream über ein Puffer Fenster von drei Sekunden und somit eine Gesamt Puffergröße von 168 KB verfügt, dauert das Ausfüllen des Puffers fast 40 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="90cd6-113">If the stream has a buffer window of three seconds, and thus a total buffer size of 168 Kb, it would take almost 40 seconds to fill the buffer.</span></span> <span data-ttu-id="90cd6-114">Die durchschnittliche Bitrate für den Datenstrom (wenn seine Dauer kleiner ist als die Zeitspanne, die zum Ausfüllen des Puffers benötigt wird) beträgt 59 Kbit/s, auch wenn die Bitrate auf 56 Kbit/s festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="90cd6-114">The average bit rate for the stream (if its duration is less than the time it takes to fill the buffer) is 59 Kbps, even though the bit rate is set to 56 Kbps.</span></span>

<span data-ttu-id="90cd6-115">Dasselbe Phänomen gilt für Einschränkungen der Spitzen Bitrate.</span><span class="sxs-lookup"><span data-stu-id="90cd6-115">The same phenomenon applies to peak bit rate constraints.</span></span> <span data-ttu-id="90cd6-116">Bei kurzen Inhalten kann die durchschnittliche Bitrate, die nach Abschluss der Codierung vom Codec-Objekt berechnet wird, größer als die Spitzen Bitrate sein.</span><span class="sxs-lookup"><span data-stu-id="90cd6-116">For short content, the average bit rate computed by the codec object after encoding is completed can be greater than the peak bit rate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90cd6-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90cd6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90cd6-118">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="90cd6-118">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



