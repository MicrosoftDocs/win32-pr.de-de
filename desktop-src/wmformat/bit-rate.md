---
title: Bitrate
description: Bitrate
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- SDK für Windows Media-Format, Bitraten
- Advanced Systems Format (ASF), Bitraten
- ASF (Advanced Systems Format), Bitraten
- Bitraten, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713710"
---
# <a name="bit-rate"></a><span data-ttu-id="a6f14-107">Bitrate</span><span class="sxs-lookup"><span data-stu-id="a6f14-107">Bit Rate</span></span>

<span data-ttu-id="a6f14-108">Die Bitrate bezieht sich auf die Menge der Daten, die pro Sekunde von einer ASF-Datei übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a6f14-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="a6f14-109">Bitraten Messungen liegen in Bits pro Sekunde (Bit/s) oder kbit pro Sekunde (Kbit/s) vor.</span><span class="sxs-lookup"><span data-stu-id="a6f14-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="a6f14-110">Die Bitrate wird häufig mit der Bandbreite verwechselt, bei der es sich um eine Messung der Datenübertragungs Kapazität eines Netzwerks handelt.</span><span class="sxs-lookup"><span data-stu-id="a6f14-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="a6f14-111">Bandbreite wird auch in Bit/s und Kbit/s gemessen.</span><span class="sxs-lookup"><span data-stu-id="a6f14-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="a6f14-112">Das Windows Media-Format-SDK kann zum Erstellen von Anwendungen verwendet werden, die das Streaming von Windows Media-basierten Inhalten aus Internet-oder Intranetstandorten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a6f14-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="a6f14-113">Wenn Sie Daten über ein Netzwerk oder das Internet streamen, ist die Bitrate von entscheidender Bedeutung für den Endbenutzer.</span><span class="sxs-lookup"><span data-stu-id="a6f14-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="a6f14-114">Wenn die für das Netzwerk verfügbare Bandbreite kleiner ist als die Bitrate der ASF-Datei, wird die Wiedergabe der Datei auf irgendeine Weise unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="a6f14-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="a6f14-115">In der Regel werden bei unzureichender Bandbreite entweder Stichproben übersprungen oder eine Pause in der Wiedergabe angezeigt, während mehr Daten gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="a6f14-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="a6f14-116">Jeder ASF-Datei wird zum Zeitpunkt der Erstellung ein Bitrate-Wert zugewiesen, basierend auf dem Typ und der Anzahl der Streams, die im verwendeten Profil enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a6f14-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="a6f14-117">Einzelne Streams verfügen über eigene Bitraten.</span><span class="sxs-lookup"><span data-stu-id="a6f14-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="a6f14-118">Die Bitraten können konstant sein (die ursprünglichen Daten werden auf eine Weise komprimiert, um einen konstanten Datenfluss mit ungefähr derselben Geschwindigkeit aufrechtzuerhalten) oder eine Variable (die ursprünglichen Daten werden so komprimiert, dass Sie die gleiche Qualität erhalten, obwohl dies einen ungleichen Datenfluss bedeuten kann).</span><span class="sxs-lookup"><span data-stu-id="a6f14-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="a6f14-119">Verschiedene Bitrate-Typen können auf verschiedene Datenströme innerhalb derselben Datei angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="a6f14-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="a6f14-120">Sie können denselben Inhalt in mehrere unterschiedliche Streams codieren, von denen jeder eine andere Bitrate hat.</span><span class="sxs-lookup"><span data-stu-id="a6f14-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="a6f14-121">Anschließend können Sie die Datenströme so konfigurieren, dass Sie sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="a6f14-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="a6f14-122">Dies ermöglicht es Ihnen, eine einzelne Datei zu erstellen, die an Benutzer mit unterschiedlichen Bandbreiten gestreamt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6f14-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="a6f14-123">Diese Funktion wird als mehrfache Bitrate oder MBR bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a6f14-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6f14-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a6f14-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6f14-125">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="a6f14-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="a6f14-126">**Codierung mit konstanter Bitrate (CBR)**</span><span class="sxs-lookup"><span data-stu-id="a6f14-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="a6f14-127">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="a6f14-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="a6f14-128">**Profiles**</span><span class="sxs-lookup"><span data-stu-id="a6f14-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="a6f14-129">**Codierung der Variablen Bitrate (VBR)**</span><span class="sxs-lookup"><span data-stu-id="a6f14-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




