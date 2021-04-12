---
description: Gibt die WaveFormatEx-Struktur an, die den audioinhaltstyp beschreibt.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215421"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a><span data-ttu-id="e8b3d-103">Mfpkey \_ wmaenc \_ origwaveformat (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e8b3d-103">MFPKEY\_WMAENC\_ORIGWAVEFORMAT Property</span></span>

<span data-ttu-id="e8b3d-104">Gibt die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur an, die den audioinhaltstyp beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-104">Specifies the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure describing the input audio content.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e8b3d-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e8b3d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e8b3d-106">g \_ wszwmacoriginalwaveformat</span><span class="sxs-lookup"><span data-stu-id="e8b3d-106">g\_wszWMACOriginalWaveFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="e8b3d-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e8b3d-107">Data Type</span></span>

<span data-ttu-id="e8b3d-108">VT \_ array \| VT \_ UI1 ([**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) als Bytearray)</span><span class="sxs-lookup"><span data-stu-id="e8b3d-108">VT\_ARRAY \| VT\_UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) as an array of bytes)</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b3d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8b3d-109">Remarks</span></span>

<span data-ttu-id="e8b3d-110">Wenn Sie Windows Media Audio basierten Inhalt in eine niedrigere Bitrate transcodieren, können Sie die [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur des Inhalts an den Codec übergeben, damit der Codec seine Algorithmen optimieren kann.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-110">When transcoding Windows Media Audio-based content to a lower bit rate, you can pass the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure of the content to the codec to enable the codec to optimize its algorithms.</span></span> <span data-ttu-id="e8b3d-111">Diese Funktion, die als Smart Recompression bezeichnet wird, bietet bessere Ergebnisse als das Dekomprimieren des Inhalts und das anschließende Füttern der rekonstruierten PCM-Beispiele über den Codec.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-111">This feature, called smart recompression, provides better results than decompressing the content and then feeding the reconstructed PCM samples back through the codec.</span></span>

<span data-ttu-id="e8b3d-112">Schließen Sie beim Übergeben der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur alle zusätzlichen Bytes am Ende der Struktur ein, die von **WaveFormatEx. cbSize** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-112">When passing the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure, include any extra bytes at the end of the structure specified by **WAVEFORMATEX.cbSize**.</span></span>

<span data-ttu-id="e8b3d-113">Der Audioencoder akzeptiert nur Eingaben und Ausgaben, bei denen die Anzahl der Kanäle, Bits pro Stichprobe und die Stichprobenrate identisch sind.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-113">The audio encoder accepts only inputs and outputs for which the number of channels, bits per sample, and sample rate are identical.</span></span> <span data-ttu-id="e8b3d-114">In diesen Parametern können Sie nur Inhalte in eine niedrigere Bitrate transcodieren.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-114">You can transcode content only to a lower bit rate within those parameters.</span></span> <span data-ttu-id="e8b3d-115">In jedem Fall müssen Sie den Inhalt decodieren und die nicht komprimierten Beispiele als Eingabe an den Encoder übergeben.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-115">In any case, you must decode the content and pass the uncompressed samples as input to the encoder.</span></span> <span data-ttu-id="e8b3d-116">Durch Festlegen dieser Eigenschaft erhält der Encoder einige Informationen über die Verarbeitung, die bereits für den Inhalt durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="e8b3d-116">Setting this property gives the encoder some information about the processing that has already been performed on the content.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b3d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8b3d-117">Requirements</span></span>



| <span data-ttu-id="e8b3d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8b3d-118">Requirement</span></span> | <span data-ttu-id="e8b3d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e8b3d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b3d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8b3d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b3d-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8b3d-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e8b3d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8b3d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b3d-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8b3d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8b3d-124">Header</span><span class="sxs-lookup"><span data-stu-id="e8b3d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8b3d-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8b3d-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b3d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8b3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b3d-127">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e8b3d-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
