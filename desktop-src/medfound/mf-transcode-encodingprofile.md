---
description: Gibt das Geräte Konformitäts Profil für die Codierung von ASF-Dateien (Advanced Streaming Format) an.
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: MF_TRANSCODE_ENCODINGPROFILE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527407"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="a24c4-103">MF- \_ transcode- \_ encodingprofile-Attribut</span><span class="sxs-lookup"><span data-stu-id="a24c4-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="a24c4-104">Gibt das Geräte Konformitäts Profil für die Codierung von ASF-Dateien (Advanced Streaming Format) an.</span><span class="sxs-lookup"><span data-stu-id="a24c4-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="a24c4-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a24c4-105">Data type</span></span>

<span data-ttu-id="a24c4-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="a24c4-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="a24c4-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="a24c4-107">Get/set</span></span>

<span data-ttu-id="a24c4-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: getalloeredstring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span><span class="sxs-lookup"><span data-stu-id="a24c4-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="a24c4-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a24c4-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="a24c4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a24c4-110">Remarks</span></span>

<span data-ttu-id="a24c4-111">Verwenden Sie dieses Attribut bei der Transcodierung auf ein Gerät, das Windows-Medien unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a24c4-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="a24c4-112">Wenn dieses Attribut festgelegt ist, verwendet der Encoder das Geräte Konformitäts Profil bzw. die Vorlage für Windows Media Codecs.</span><span class="sxs-lookup"><span data-stu-id="a24c4-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="a24c4-113">Legen Sie das-Attribut für das transcodieren-Profil fest, bevor Sie die transcodieren-Topologie erstellen.</span><span class="sxs-lookup"><span data-stu-id="a24c4-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="a24c4-114">Der Wert dieses Attributs kann eine der in den folgenden Themen aufgeführten Konformitäts Vorlagen Zeichenfolgen sein:</span><span class="sxs-lookup"><span data-stu-id="a24c4-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="a24c4-115">Konformitäts Vorlagen für Audiogeräte</span><span class="sxs-lookup"><span data-stu-id="a24c4-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="a24c4-116">Vorlagen für die Konformitäts Konformität von Video Geräten</span><span class="sxs-lookup"><span data-stu-id="a24c4-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="a24c4-117">Bei Windows Media Video Codierung verwendet der topologiebuilder dieses Attribut, um die [**mfpkey- \_ decodercomplexityangeforderten**](mfpkey-decodercomplexityrequestedproperty.md) -Eigenschaft für den Encoder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a24c4-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="a24c4-118">Der Encoder versucht, die angegebene Vorlage zu verwenden, um den Inhalt zu codieren.</span><span class="sxs-lookup"><span data-stu-id="a24c4-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="a24c4-119">Um die tatsächliche Vorlage zu erhalten, Durchsuchen Sie die Knoten der transcodieren-Topologie, um einen Zeiger auf den encoderknoten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a24c4-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="a24c4-120">Dann erhalten Sie den Wert der Eigenschaft [**mfpkey \_ decodercomplexityprofile**](mfpkey-decodercomplexityprofileproperty.md) aus dem Encoder.</span><span class="sxs-lookup"><span data-stu-id="a24c4-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="a24c4-121">Der Topologiegenerator verwendet auch den Wert dieses Attributs, um die Eigenschaft "opviceconformancetemplate" in der ASF-Medien Senke festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a24c4-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="a24c4-122">Wenn dieses Attribut festgelegt ist, wird das Metadatenobjekt der ASF-Datei immer generiert, unabhängig davon, welcher Wert von [der Anwendung \_ \_ \_ \_ ](mf-transcode-skip-metadata-transfer.md) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a24c4-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="a24c4-123">Die folgenden Werte sind für dieses Attribut typisch:</span><span class="sxs-lookup"><span data-stu-id="a24c4-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="a24c4-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a24c4-124">Value</span></span>   | <span data-ttu-id="a24c4-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a24c4-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="a24c4-126">Unglücks</span><span class="sxs-lookup"><span data-stu-id="a24c4-126">"AP"</span></span>    | <span data-ttu-id="a24c4-127">Video zum erweiterten Profil</span><span class="sxs-lookup"><span data-stu-id="a24c4-127">Advanced profile video</span></span>           |
| <span data-ttu-id="a24c4-128">Schlanken</span><span class="sxs-lookup"><span data-stu-id="a24c4-128">"MP"</span></span>    | <span data-ttu-id="a24c4-129">Video zum Hauptprofil</span><span class="sxs-lookup"><span data-stu-id="a24c4-129">Main profile video</span></span>               |
| <span data-ttu-id="a24c4-130">El</span><span class="sxs-lookup"><span data-stu-id="a24c4-130">"SP"</span></span>    | <span data-ttu-id="a24c4-131">Video zu einfachem Profil</span><span class="sxs-lookup"><span data-stu-id="a24c4-131">Simple profile video</span></span>             |
| <span data-ttu-id="a24c4-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="a24c4-132">"MP@LL"</span></span> | <span data-ttu-id="a24c4-133">Hauptprofil, Video auf mittlerer Ebene</span><span class="sxs-lookup"><span data-stu-id="a24c4-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="a24c4-134">L2</span><span class="sxs-lookup"><span data-stu-id="a24c4-134">"L2"</span></span>    | <span data-ttu-id="a24c4-135">Audioprofil, <= 160 KBit/s</span><span class="sxs-lookup"><span data-stu-id="a24c4-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="a24c4-136">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a24c4-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24c4-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a24c4-137">Requirements</span></span>



| <span data-ttu-id="a24c4-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a24c4-138">Requirement</span></span> | <span data-ttu-id="a24c4-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a24c4-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a24c4-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a24c4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a24c4-141">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a24c4-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a24c4-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a24c4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a24c4-143">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a24c4-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a24c4-144">Header</span><span class="sxs-lookup"><span data-stu-id="a24c4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24c4-145"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a24c4-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24c4-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a24c4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24c4-147">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a24c4-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a24c4-148">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="a24c4-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="a24c4-149">**IMF transcodeprofile:: getaudioattribute**</span><span class="sxs-lookup"><span data-stu-id="a24c4-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="a24c4-150">**IMF transcodeprofile:: setaudioattribute**</span><span class="sxs-lookup"><span data-stu-id="a24c4-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="a24c4-151">**IMF transcodeprofile:: setvideoattribute**</span><span class="sxs-lookup"><span data-stu-id="a24c4-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="a24c4-152">**IMF transcodeprofile:: getvideoattribute**</span><span class="sxs-lookup"><span data-stu-id="a24c4-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
