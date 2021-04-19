---
description: Decodereinstellungen für Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Decodereinstellungen für Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106363889"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="1a67b-103">Decodereinstellungen für Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="1a67b-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="1a67b-104">Windows XP Media Center Edition 2005 und höher verwendet die [**icodecapi**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) -Schnittstelle, um den audiodecoderfilter für die Fernseh-und DVD-Wiedergabe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1a67b-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="1a67b-105">Die folgenden Eigenschaften werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1a67b-105">The following properties are supported.</span></span>



| <span data-ttu-id="1a67b-106">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="1a67b-106">Property GUID</span></span>                   | <span data-ttu-id="1a67b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a67b-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="1a67b-108">codecapi \_ - \_ audioausgabeformat \_</span><span class="sxs-lookup"><span data-stu-id="1a67b-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="1a67b-109">Konfiguriert das audioausgabeformat.</span><span class="sxs-lookup"><span data-stu-id="1a67b-109">Configures the audio output format.</span></span> <span data-ttu-id="1a67b-110">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1a67b-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1a67b-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a67b-111">Remarks</span></span>

<span data-ttu-id="1a67b-112">Der Wert der Eigenschaft codecapi \_ - \_ audioausgabeformat \_ ist eine Zeichen folgen Darstellung einer GUID, die als **BSTR** -Wert gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="1a67b-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="1a67b-113">Die folgenden GUIDs sind definiert.</span><span class="sxs-lookup"><span data-stu-id="1a67b-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="1a67b-114">GUID</span><span class="sxs-lookup"><span data-stu-id="1a67b-114">GUID</span></span>                                                        | <span data-ttu-id="1a67b-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a67b-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a67b-116">codecapi \_ - \_ audioausgabeformat \_ \_ PCM \_ Stereo \_ matrixencoded</span><span class="sxs-lookup"><span data-stu-id="1a67b-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="1a67b-117">Der Software Audiofilter sollte das Decodieren von Software und das Ausgeben eines Stereo-Audiostreams durchführen, wobei die Multichannel-Audiomatrix auf die beiden Kanäle codiert ist.</span><span class="sxs-lookup"><span data-stu-id="1a67b-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="1a67b-118">codecapi \_ - \_ audioausgabeformat \_ \_ PCM \_ Stereo</span><span class="sxs-lookup"><span data-stu-id="1a67b-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="1a67b-119">Der Software-Audiofilter sollte Software Decodierung durchführen und einen Stereo-Audiostream ausgeben.</span><span class="sxs-lookup"><span data-stu-id="1a67b-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="1a67b-120">codecapi \_ - \_ audioausgabeformat \_ \_ SPDIF \_ PCM</span><span class="sxs-lookup"><span data-stu-id="1a67b-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="1a67b-121">Der Software Audiofilter sollte Software-Audiodecodierung durchführen, auch wenn die physische Ausgabe des PCs eine digitale Schnittstelle sein kann, z. b. S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="1a67b-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="1a67b-122">codecapi \_ - \_ audioausgabeformat \_ \_ SPDIF \_ Bitstream</span><span class="sxs-lookup"><span data-stu-id="1a67b-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="1a67b-123">Der softwareupdateifilter sollte keine Software-Audiodecodierung durchführen, sondern den unformatierten, digitalen audiopstream für die externe Verarbeitung durch ein Gerät übergeben, das mit einem digitalen audiolink verbunden ist, z. b. S/PDIF</span><span class="sxs-lookup"><span data-stu-id="1a67b-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="1a67b-124">codecapi \_ - \_ audioausgabeformat \_ \_ PCM- \_ Kopfhörer</span><span class="sxs-lookup"><span data-stu-id="1a67b-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="1a67b-125">Der Software Audiofilter sollte Software-Audiodecodierung durchführen und die proprietäre Verarbeitung anwenden, um für Kopfhörer zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="1a67b-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="1a67b-126">Die Unterstützung für diese Einstellung ist optional.</span><span class="sxs-lookup"><span data-stu-id="1a67b-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="1a67b-127">Die **icodecapi** -Schnittstelle speichert Codec-Eigenschaften als Schlüssel-Wert-Paare, wobei der Schlüssel eine GUID und der Wert ein **Variant** -Typ ist.</span><span class="sxs-lookup"><span data-stu-id="1a67b-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1a67b-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1a67b-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a67b-129">Encoder-und decoderentwicklung</span><span class="sxs-lookup"><span data-stu-id="1a67b-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



