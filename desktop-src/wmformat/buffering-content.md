---
title: Pufferung von Inhalten
description: Pufferung von Inhalten
ms.assetid: e14e0130-aefd-4e46-b288-4302d2333de2
keywords:
- Windows Media-Format-SDK, Pufferung von Inhalten
- Pufferung von Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b378431653f21be742c12b4e4a5ae2a994318
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341421"
---
# <a name="buffering-content"></a><span data-ttu-id="26470-105">Pufferung von Inhalten</span><span class="sxs-lookup"><span data-stu-id="26470-105">Buffering Content</span></span>

<span data-ttu-id="26470-106">Wenn das Reader-Objekt eine Streamingdatei öffnet, bestimmt es die Größe des Puffers basierend auf den Einstellungen im Header der Datei.</span><span class="sxs-lookup"><span data-stu-id="26470-106">When the reader object opens a streaming file, it determines the size of the buffer based upon settings in the header of the file.</span></span> <span data-ttu-id="26470-107">Sie können sich den Puffer als Bucket mit einem Loch im unteren Bereich vorstellen, das bei konstanter Geschwindigkeit eine Dichte gibt.</span><span class="sxs-lookup"><span data-stu-id="26470-107">You can think of the buffer as a bucket with a hole in the bottom that leaks at a constant rate.</span></span> <span data-ttu-id="26470-108">Solange die Rate, mit der der Bucket aufgefüllt wird, nicht im Durchschnitt größer ist als die Rate, mit der er nicht mehr erreicht wird, führt der Bucket nie zu einem Überlauf.</span><span class="sxs-lookup"><span data-stu-id="26470-108">As long as the rate at which the bucket is filled is not, on average, greater than the rate at which it is leaking, the bucket will never overflow.</span></span>

<span data-ttu-id="26470-109">Die Rate, mit der die imaginären Bucket-Lecks die Bitrate des Streams ist.</span><span class="sxs-lookup"><span data-stu-id="26470-109">The rate at which the imaginary bucket leaks is the bit rate of the stream.</span></span> <span data-ttu-id="26470-110">Die Rate, mit der der Bucket ausgefüllt wird, ist die tatsächliche streamingbitrate.</span><span class="sxs-lookup"><span data-stu-id="26470-110">The rate at which the bucket fills is the actual streaming bit rate.</span></span> <span data-ttu-id="26470-111">Die Daten in einem komprimierten Datenstrom variieren abhängig von der erreichten Komprimierung von Sample zu Sample.</span><span class="sxs-lookup"><span data-stu-id="26470-111">The data in a compressed stream varies in size from sample to sample depending on the amount of compression that was achieved.</span></span> <span data-ttu-id="26470-112">Obwohl die Bitrate des Streams im Profil festgelegt ist, stellt Sie somit die durchschnittliche Bitrate dar, nicht eine Konstante.</span><span class="sxs-lookup"><span data-stu-id="26470-112">Thus, even though the bit rate of the stream is set in the profile, it represents the average bit rate, not a constant.</span></span>

<span data-ttu-id="26470-113">Die andere streamingeinstellung, die für den Puffer Prozess wichtig ist, ist das Puffer Fenster.</span><span class="sxs-lookup"><span data-stu-id="26470-113">The other stream setting important to the buffering process is the buffer window.</span></span> <span data-ttu-id="26470-114">Das Puffer Fenster wird zeitlich gemessen und gibt an, wie viel Inhalt gepuffert werden kann.</span><span class="sxs-lookup"><span data-stu-id="26470-114">The buffer window is measured in time and specifies how much content can be buffered.</span></span> <span data-ttu-id="26470-115">Die Kapazität des imaginären Bucket kann mithilfe des Puffer Fensters gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="26470-115">The capacity of the imaginary bucket can be found using the buffer window.</span></span> <span data-ttu-id="26470-116">Wenn Sie z. b. einen Datenstrom mit einer Bitrate von 32 Kbit/s und einem Puffer Fenster von 3 Sekunden haben, wird der Puffer so skaliert, dass er 3 Sekunden mit 32 Kbit/s-Inhalt und 12.000 Bytes (32.000 Bits pro Sekunde x 3 Sekunden/8 Bits pro Byte) enthält.</span><span class="sxs-lookup"><span data-stu-id="26470-116">For example, if you have a stream with a bit rate of 32 Kbps and a buffer window of 3 seconds, the buffer is sized to hold 3 seconds of 32 Kbps content, or 12,000 bytes (32,000 bits per second x 3 seconds / 8 bits per byte).</span></span> <span data-ttu-id="26470-117">Der Codec schränkt die Variation zwischen der tatsächlichen streamingbitrate codierter Stichproben ein, sodass die durchschnittliche Bitrate über einen Zeitraum, der gleich dem Puffer Fenster ist, nicht größer als die Bitrate des Streams ist.</span><span class="sxs-lookup"><span data-stu-id="26470-117">The codec limits the variation between the actual streaming bit rate of encoded samples so that over a period of time equal to the buffer window, the average bit rate is no greater than the bit rate of the stream.</span></span>

<span data-ttu-id="26470-118">Normalerweise legen Sie die Bitrate und das Puffer Fenster für einen Stream in einem Profil fest, und der Writer übernimmt den Rest.</span><span class="sxs-lookup"><span data-stu-id="26470-118">Normally, you set the bit rate and buffer window for a stream in a profile, and the writer handles the rest.</span></span> <span data-ttu-id="26470-119">Wenn Sie komprimierte Beispiele an den Reader übergeben, müssen Sie jedoch sicherstellen, dass die richtigen Werte in die neue Datei übertragen werden, indem Sie die Bitrate und das Puffer Fenster für den Stream im Ziel Profil auf die Werte aus dem komprimierten Stream festlegen.</span><span class="sxs-lookup"><span data-stu-id="26470-119">When passing compressed samples to the reader, however, you must ensure that the correct values are transferred to the new file by setting the bit rate and buffer window for the stream in the destination profile to the values from the compressed stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26470-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26470-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26470-121">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="26470-121">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="26470-122">**Medien Beispiele**</span><span class="sxs-lookup"><span data-stu-id="26470-122">**Media Samples**</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="26470-123">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="26470-123">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> </dl>

 

 




