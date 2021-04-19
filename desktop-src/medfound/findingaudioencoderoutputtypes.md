---
description: Suchen von Audioencoder-Ausgabetypen
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Suchen von audioencoderausgabetypen (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346464"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="78852-103">Suchen von audioencoderausgabetypen (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="78852-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="78852-104">Da Sie ein audiocodierungsausgabeformat verwenden müssen, das vom Audioencoder aufgelistet wird, müssen Sie über eine Möglichkeit verfügen, das Format zu finden, das für Ihre Anforderungen am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="78852-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="78852-105">Die Anzahl der Kanäle, Bits pro Stichprobe und die Samplingrate der Ausgabe, die Sie auswählen, müssen mit den Werten für den von Ihnen komprimierte Inhalt identisch sein.</span><span class="sxs-lookup"><span data-stu-id="78852-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="78852-106">Der Encoder unterstützt jedoch möglicherweise mehrere Typen innerhalb dieser Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="78852-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="78852-107">Der entscheidende Faktor für die Auswahl eines Typs ist die Bitrate des codierten Streams. Sie möchten einen Medientyp suchen, der mit Ihrer Eingabe übereinstimmt und eine Bitrate hat, die so nah wie möglich an einem Zielwert ist.</span><span class="sxs-lookup"><span data-stu-id="78852-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="78852-108">Wenn Sie die VBR-Ausgabetypen mit einem Durchlauf auflisten, ist dies der Qualitäts Wert, der den Typ bestimmt, den Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="78852-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="78852-109">Weitere Informationen zu Qualitätswerten in Enumerationstypen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="78852-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="78852-110">Der Audioencoder listet einige Typen auf, bei denen es sich um Duplikate anderer Typen handelt.</span><span class="sxs-lookup"><span data-stu-id="78852-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="78852-111">Diese Duplikate sind für Formate vorhanden, in denen die Anzahl der Pakete pro Sekunde nicht den Anforderungen für die Speicherung in ASF-Dateien entspricht, wenn Sie mit Video synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="78852-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="78852-112">Audiodaten, die mit einem Video in einer ASF-Datei synchronisiert werden, müssen mindestens 3 Pakete pro Sekunde für Bitraten unter 32000 und mindestens 5 Pakete pro Sekunde für Bitraten größer oder gleich 32000 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="78852-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="78852-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78852-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78852-114">Konfigurieren der Audiocodierung</span><span class="sxs-lookup"><span data-stu-id="78852-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="78852-115">Auflisten von Audiotypen für bestimmte Codierungs Modi</span><span class="sxs-lookup"><span data-stu-id="78852-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



