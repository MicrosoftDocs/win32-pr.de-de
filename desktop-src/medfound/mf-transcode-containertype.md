---
description: Gibt den Containertyp einer codierten Datei an.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: MF_TRANSCODE_CONTAINERTYPE-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359905"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="f60f5-103">MF- \_ transcode- \_ ContainerType-Attribut</span><span class="sxs-lookup"><span data-stu-id="f60f5-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="f60f5-104">Gibt den Containertyp einer codierten Datei an.</span><span class="sxs-lookup"><span data-stu-id="f60f5-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="f60f5-105">Die Containertypen werden von Media Foundation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f60f5-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="f60f5-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f60f5-106">Data type</span></span>

<span data-ttu-id="f60f5-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="f60f5-107">**GUID**</span></span>

<span data-ttu-id="f60f5-108">Mögliche Werte für die Containertypen, die von Media Foundation bereitgestellt werden, werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f60f5-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="f60f5-109">Wert</span><span class="sxs-lookup"><span data-stu-id="f60f5-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="f60f5-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f60f5-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="f60f5-111"><dt>**MF transcodecontainertype- \_ ASF**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="f60f5-112">Der ASF-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="f60f5-113"><dt>**MF transcodecontainertype \_ MPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="f60f5-114">MP4-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="f60f5-115"><dt>**MF transcodecontainertype \_ MP3**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="f60f5-116">Der MP3-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="f60f5-117"><dt>**MF transcodecontainertype \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="f60f5-118">3GP-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="f60f5-119"><dt>**MF transcodecontainertype \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="f60f5-120">AC3-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="f60f5-121"><dt>**MF transcodecontainertype- \_ ADTs**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="f60f5-122">ADTS-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="f60f5-123"><dt>**MF transcodecontainertype ( \_ MPEG2)**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="f60f5-124">MPEG2-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="f60f5-125"><dt>**MF transcodecontainertype \_ FMPEG4**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="f60f5-126">FMPEG4-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="f60f5-127"><dt>**MF transcodecontainertype- \_ Wave**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="f60f5-128">Wave File-Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-128">WAVE file container.</span></span><br/> <span data-ttu-id="f60f5-129">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f60f5-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="f60f5-130"><dt>**MF transcodecontainertype \_ AVI**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="f60f5-131">AVI-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-131">AVI file container.</span></span><br/> <span data-ttu-id="f60f5-132">Wird in Windows 8.1 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f60f5-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="f60f5-133"><dt>**MF transcodecontainertype \_ AMR**</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="f60f5-134">AMR-Datei Container.</span><span class="sxs-lookup"><span data-stu-id="f60f5-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="f60f5-135">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="f60f5-135">Get/set</span></span>

<span data-ttu-id="f60f5-136">Um dieses Attribut abzurufen, wenden Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)an.</span><span class="sxs-lookup"><span data-stu-id="f60f5-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="f60f5-137">Um dieses Attribut festzulegen, wenden Sie [**imfattributes:: SetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)an.</span><span class="sxs-lookup"><span data-stu-id="f60f5-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="f60f5-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f60f5-138">Remarks</span></span>

<span data-ttu-id="f60f5-139">Dieses Attribut wird sowohl für die Funktion "schnelles transcode" als auch für das Objekt "Sink Writer" verwendet.</span><span class="sxs-lookup"><span data-stu-id="f60f5-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="f60f5-140">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="f60f5-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="f60f5-141">Schnelles transcode</span><span class="sxs-lookup"><span data-stu-id="f60f5-141">Fast Transcode</span></span>

<span data-ttu-id="f60f5-142">Die Anwendung muss das Container-Attribut im transcodieren-Profil vor dem Erstellen der transcodieren-Topologie festlegen.</span><span class="sxs-lookup"><span data-stu-id="f60f5-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="f60f5-143">Der topologiebuilder analysiert dieses Attribut und lädt die entsprechende Medien Senke in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f60f5-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="f60f5-144">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f60f5-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f60f5-145">**IMF transcodeprofile:: getcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="f60f5-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="f60f5-146">**IMF transcodeprofile:: setcontainerattribute**</span><span class="sxs-lookup"><span data-stu-id="f60f5-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="f60f5-147">Senke-Writer</span><span class="sxs-lookup"><span data-stu-id="f60f5-147">Sink Writer</span></span>

<span data-ttu-id="f60f5-148">Dieses Attribut kann verwendet werden, um den dateicontainertyp für den senkwriter zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f60f5-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="f60f5-149">Weitere Informationen finden Sie unter [senkenwriter-Attribute](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f60f5-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f60f5-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f60f5-150">Requirements</span></span>



| <span data-ttu-id="f60f5-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f60f5-151">Requirement</span></span> | <span data-ttu-id="f60f5-152">Wert</span><span class="sxs-lookup"><span data-stu-id="f60f5-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f60f5-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f60f5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f60f5-154">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f60f5-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f60f5-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f60f5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f60f5-156">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f60f5-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f60f5-157">Header</span><span class="sxs-lookup"><span data-stu-id="f60f5-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f60f5-158"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f60f5-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f60f5-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f60f5-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f60f5-160">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="f60f5-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f60f5-161">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="f60f5-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




