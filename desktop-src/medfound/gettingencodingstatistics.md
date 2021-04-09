---
description: Beschreibt Statistiken, die Sie aus einem Windows Media-Codec abrufen können.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Erhalten von Codierungs Statistiken (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749217"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="44ab3-103">Erhalten von Codierungs Statistiken (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="44ab3-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="44ab3-104">Informationen dazu, was in einer Codierungs Sitzung geschieht, sind in der Regel sofort in Form von Fehlercodes verfügbar, die beim Verarbeiten von Beispielen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="44ab3-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="44ab3-105">Es gibt jedoch einige Statistiken, die Sie aus dem Codec über verschiedene Codierungs Aspekte abrufen können.</span><span class="sxs-lookup"><span data-stu-id="44ab3-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="44ab3-106">Video Frame Informationen</span><span class="sxs-lookup"><span data-stu-id="44ab3-106">Video Frame Information</span></span>

<span data-ttu-id="44ab3-107">Einige Video Statistiken, die Sie abrufen können, sind mit der Anzahl der vom Encoder verarbeiteten Frames zu beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="44ab3-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="44ab3-108">Es gibt drei Eigenschaften von Frame Nummern, die Sie aus dem Video Encoder lesen können:</span><span class="sxs-lookup"><span data-stu-id="44ab3-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="44ab3-109">[Mfpkey \_ Total Frames](mfpkey-totalframesproperty.md) ist die Anzahl der Frames, die über den Eingabestream des DMO verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="44ab3-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="44ab3-110">[Mfpkey \_ Codedframes](mfpkey-codedframesproperty.md) ist die Anzahl der codierten Frames.</span><span class="sxs-lookup"><span data-stu-id="44ab3-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="44ab3-111">Wenn Sie diesen Wert von der Gesamtzahl der übergebenen Frames subtrahieren, können Sie bestimmen, wie viele Frames gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="44ab3-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="44ab3-112">[Mfpkey \_ Zerobyteframes](mfpkey-zerobyteframesproperty.md) ist die Anzahl der Frames, die nicht codiert werden, da Sie bereits enthaltene Inhalte duplizieren.</span><span class="sxs-lookup"><span data-stu-id="44ab3-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="44ab3-113">Dieser Wert wird nicht von der Anzahl der vom DMO gemeldeten codierten Frames subtrahiert.</span><span class="sxs-lookup"><span data-stu-id="44ab3-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="44ab3-114">Sie können während der Codierung jederzeit Video Frame Eigenschaften lesen.</span><span class="sxs-lookup"><span data-stu-id="44ab3-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="44ab3-115">Dies kann hilfreich sein, um zu bestimmen, ob die Codierungs Einstellungen für Ihre Inhalte geeignet sind. Wenn ein großer Unterschied zwischen den Gesamtrahmen und den codierten Frames besteht, entsprechen die komprimierten Inhalte möglicherweise nicht Ihren Qualitätsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="44ab3-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="44ab3-116">Sie können die endgültigen Werte lesen, nachdem Sie die Codierung abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="44ab3-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="44ab3-117">VBR-Puffer Statistik</span><span class="sxs-lookup"><span data-stu-id="44ab3-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="44ab3-118">Abhängig vom verwendeten Codierungs Modus können einige oder alle Puffer Einstellungen während der Codierung bestimmt werden (z. b. ist die Bitrate von Quality-basiertem VBR erst bekannt, wenn der Inhalt codiert ist).</span><span class="sxs-lookup"><span data-stu-id="44ab3-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="44ab3-119">Es gibt vier VBR-Puffer Eigenschaften, die Sie mithilfe der **IPropertyBag:: Read** -Methode erhalten können:</span><span class="sxs-lookup"><span data-stu-id="44ab3-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="44ab3-120">[Mfpkey \_ Ravg](mfpkey-ravgproperty.md) ist die durchschnittliche Bitrate des VBR-Inhalts.</span><span class="sxs-lookup"><span data-stu-id="44ab3-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="44ab3-121">[Mfpkey \_ Bavg](mfpkey-bavgproperty.md) ist das Puffer Fenster für die durchschnittliche Bitrate.</span><span class="sxs-lookup"><span data-stu-id="44ab3-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="44ab3-122">[Mfpkey \_ Rmax](mfpkey-rmaxproperty.md) ist die Spitzen Bitrate der VBR-Inhalte.</span><span class="sxs-lookup"><span data-stu-id="44ab3-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="44ab3-123">[Mfpkey \_ Bmax](mfpkey-bmaxproperty.md) ist das Hauptpuffer Fenster.</span><span class="sxs-lookup"><span data-stu-id="44ab3-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="44ab3-124">Nachdem Sie mit der Verarbeitung von Beispielen begonnen haben, sollten Sie die VBR-Eigenschaften erst lesen, wenn Sie mit dem Codieren des Streams fertig sind.</span><span class="sxs-lookup"><span data-stu-id="44ab3-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="44ab3-125">Wenn Sie dies tun, interpretiert der Encoder Ihre Anforderung als Signal, dass die Codierung fertiggestellt ist.</span><span class="sxs-lookup"><span data-stu-id="44ab3-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="44ab3-126">Das nächste Beispiel, das Sie verarbeiten, wird als neue Codierungs Sitzung behandelt.</span><span class="sxs-lookup"><span data-stu-id="44ab3-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44ab3-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44ab3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44ab3-128">Windows Media-Codecs</span><span class="sxs-lookup"><span data-stu-id="44ab3-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



