---
description: Verwenden High-Definition Audiodaten
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Verwenden High-Definition Audiodaten (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755240"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="932c3-103">Verwenden High-Definition Audiodaten (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="932c3-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="932c3-104">Bei der Verwendung von High-Definition-Audiodaten im Kontext der Windows Media Audio Codecs handelt es sich um einen beliebigen Audiotyp mit mehr als zwei Kanälen oder mehr als 16 Bits pro Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="932c3-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="932c3-105">High-Definition-Audiodaten werden von den Kategorien "Professional" und "Lossless" des [Windows Media Audio Encoders](windowsmediaaudioencoder.md)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="932c3-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="932c3-106">Unkomprimierte High-Definition-Audiotypen werden mithilfe der [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="932c3-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="932c3-107">**WAVEFORMATEXTENSIBLE** ist eine strukturierte Erweiterung der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="932c3-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="932c3-108">Wenn Sie DMOS verwenden, muss der **Format Type** -Member der [**DMO \_ - \_ Medientyp**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Struktur, der einen hoch definierbaren Audiotyp beschreibt, auf das wmcformat \_ WaveFormatEx festgelegt werden, so wie es für das normale Audioformat der Fall ist. es gibt keinen speziellen Format Bezeichner für **WAVEFORMATEXTENSIBLE**.</span><span class="sxs-lookup"><span data-stu-id="932c3-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="932c3-109">Wenn ein Format **WAVEFORMATEXTENSIBLE** verwendet, müssen Sie das **CBSIZE** -Element der **WaveFormatEx** -Struktur auf 22 festlegen.</span><span class="sxs-lookup"><span data-stu-id="932c3-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="932c3-110">Wenn Sie Media Foundation verwenden, können Sie den richtigen Medientyp aus einer [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur erstellen, indem Sie die [**mfinitmediatypeer fromwaveformatex**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex)-Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="932c3-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="932c3-111">Die vom Windows Media Audio 10 Professional-Codec unterstützten multikanalausgabetypen verwenden [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))nicht, melden jedoch die richtige Anzahl von Kanälen und Bits pro Stichprobe in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="932c3-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="932c3-112">Wie bei allen Audiotypen, die komprimierte Windows Media Audio Inhalt beschreiben, werden zusätzliche Informationen an die **WaveFormatEx** -Struktur angehängt, die vom Decoder für die Dekomprimierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="932c3-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="932c3-113">Decodieren High-Definition Audiodaten</span><span class="sxs-lookup"><span data-stu-id="932c3-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="932c3-114">Zum Decodieren von High-Definition-Audiodaten müssen Sie die Eigenschaft [mfpkey \_ wmadec \_ hiresoutput](mfpkey-wmadec-hiresoutputproperty.md) auf Variant \_ true festlegen.</span><span class="sxs-lookup"><span data-stu-id="932c3-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="932c3-115">Wenn diese Eigenschaft nicht festgelegt ist, stellt der Decoder unabhängig vom komprimierten Format Stereo Inhalte mit maximal 16 Bits pro Beispiel bereit.</span><span class="sxs-lookup"><span data-stu-id="932c3-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="932c3-116">High-Definition-Audiodaten werden nur für Windows XP, Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="932c3-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="932c3-117">In früheren Versionen von Windows wird Windows Media Audio mit hoher Definition codierte Inhalt als zwei-Kanal-Audiodaten mit maximal 16 Bits pro Stichprobe gerendert.</span><span class="sxs-lookup"><span data-stu-id="932c3-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="932c3-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="932c3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="932c3-119">Arbeiten mit Audiodaten</span><span class="sxs-lookup"><span data-stu-id="932c3-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
