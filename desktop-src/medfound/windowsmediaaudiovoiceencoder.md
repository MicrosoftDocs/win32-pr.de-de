---
description: Der Windows Media Audio Voice-Encoder ist für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert. Dies ist der bevorzugte Encoder für Streams, die größtenteils aus gesprochenen Wörtern bestehen.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Media Audio sprach Encoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370789"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="82899-104">Windows Media Audio sprach Encoder</span><span class="sxs-lookup"><span data-stu-id="82899-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="82899-105">Der Windows Media Audio Voice-Encoder ist für die Codierung der menschlichen Stimme bei hohen Komprimierungs Verhältnissen optimiert.</span><span class="sxs-lookup"><span data-stu-id="82899-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="82899-106">Dies ist der bevorzugte Encoder für Streams, die größtenteils aus gesprochenen Wörtern bestehen.</span><span class="sxs-lookup"><span data-stu-id="82899-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="82899-107">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="82899-107">Class Identifier</span></span>

<span data-ttu-id="82899-108">Der Klassen Bezeichner (CLSID) für den Windows Media Audio Voice-Encoder wird durch die Konstante **CLSID \_ CWMSPEncMediaObject2** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="82899-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="82899-109">Sie können eine Instanz des Voice-Encoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="82899-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="82899-110">Ausgabeformate</span><span class="sxs-lookup"><span data-stu-id="82899-110">Output Formats</span></span>

<span data-ttu-id="82899-111">Windows Media Audio sprach codierter Inhalt wird durch das Format-Tag 0x00a identifiziert.</span><span class="sxs-lookup"><span data-stu-id="82899-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="82899-112">Codierungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82899-112">Encoder Properties</span></span>

<span data-ttu-id="82899-113">Der Windows Media Audio Voice-Encoder unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82899-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="82899-114">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="82899-114">Property</span></span></th>
<th><span data-ttu-id="82899-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82899-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82899-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="82899-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="82899-117">Gibt das für den voicecodec verwendete Puffer Fenster in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="82899-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="82899-118">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="82899-118">Windows XP and later.</span></span><br />
<span data-ttu-id="82899-119">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="82899-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82899-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="82899-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="82899-121">Gibt die encoderwartezeit in Paketeinheiten an.</span><span class="sxs-lookup"><span data-stu-id="82899-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="82899-122">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="82899-122">Windows XP and later.</span></span><br />
<span data-ttu-id="82899-123">Nur Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="82899-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82899-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="82899-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="82899-125">Gibt die Inhalts Teile an, die vom Voice-Codec als Musik codiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="82899-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="82899-126">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="82899-126">Windows XP and later.</span></span><br />
<span data-ttu-id="82899-127">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="82899-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82899-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="82899-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="82899-129">Gibt den Modus des voicecodec an.</span><span class="sxs-lookup"><span data-stu-id="82899-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="82899-130">Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="82899-130">Windows XP and later.</span></span><br />
<span data-ttu-id="82899-131">Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="82899-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="82899-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82899-132">Requirements</span></span>



| <span data-ttu-id="82899-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82899-133">Requirement</span></span> | <span data-ttu-id="82899-134">Wert</span><span class="sxs-lookup"><span data-stu-id="82899-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82899-135">Client</span><span class="sxs-lookup"><span data-stu-id="82899-135">Client</span></span><br/> | <span data-ttu-id="82899-136">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="82899-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="82899-137">Header</span><span class="sxs-lookup"><span data-stu-id="82899-137">Header</span></span><br/> | <dl> <span data-ttu-id="82899-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="82899-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="82899-139">DLL</span><span class="sxs-lookup"><span data-stu-id="82899-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="82899-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82899-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82899-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82899-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82899-142">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="82899-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="82899-143">Verwenden des Windows Media Audio Voice-Codecs</span><span class="sxs-lookup"><span data-stu-id="82899-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




