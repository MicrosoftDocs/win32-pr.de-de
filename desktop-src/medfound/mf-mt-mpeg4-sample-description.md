---
description: Enthält das Beispiel Beschreibungsfeld für eine MP4-oder 3GP-Datei.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867544"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a><span data-ttu-id="a2b76-103">"MF \_ MT \_ MPEG4 \_ Sample \_ Description"-Attribut</span><span class="sxs-lookup"><span data-stu-id="a2b76-103">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute</span></span>

<span data-ttu-id="a2b76-104">Enthält das Beispiel Beschreibungsfeld für eine MP4-oder 3GP-Datei.</span><span class="sxs-lookup"><span data-stu-id="a2b76-104">Contains the sample description box for an MP4 or 3GP file.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2b76-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a2b76-105">Data type</span></span>

<span data-ttu-id="a2b76-106">**Hobby\[\]**</span><span class="sxs-lookup"><span data-stu-id="a2b76-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="a2b76-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="a2b76-107">Get/set</span></span>

<span data-ttu-id="a2b76-108">Zum Abrufen dieses Attributs müssen Sie [**imfattributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a2b76-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="a2b76-109">Um dieses Attribut festzulegen, müssen Sie [**imfattributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a2b76-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a2b76-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="a2b76-110">Applies to</span></span>

[<span data-ttu-id="a2b76-111">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="a2b76-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="a2b76-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a2b76-112">Remarks</span></span>

<span data-ttu-id="a2b76-113">Das Feld Beispiel Beschreibung beschreibt die Codierung, die für einen Datenstrom in der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a2b76-113">The sample description box describes the encoding used for a stream in the file.</span></span>

<span data-ttu-id="a2b76-114">Die MPEG-4-Datei Quelle legt dieses Attribut für den Medientyp für jeden Stream fest.</span><span class="sxs-lookup"><span data-stu-id="a2b76-114">The MPEG-4 file source sets this attribute on the media type for each stream.</span></span> <span data-ttu-id="a2b76-115">Der Wert des-Attributs sind die Rohdaten im Feld für die Beispiel Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a2b76-115">The value of the attribute is the raw data in the sample description box.</span></span> <span data-ttu-id="a2b76-116">Wenn die MPEG-4-Datei Quelle die Beispiel Beschreibung analysieren kann, werden auch die Format Details dem Medientyp hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2b76-116">If the MPEG-4 file source can parse the sample description, it also adds the format details to the media type.</span></span> <span data-ttu-id="a2b76-117">Andernfalls muss die Anwendung oder der Decoder die Beispiel Beschreibung aus dem MF \_ MT \_ MPEG4 \_ Sample \_ Description-Attribut analysieren.</span><span class="sxs-lookup"><span data-stu-id="a2b76-117">Otherwise, the application or the decoder must parse the sample description from the MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION attribute.</span></span>

<span data-ttu-id="a2b76-118">Beim Festlegen dieses Attributs für die MPEG-4-Senke über die [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) -Methode sollten sich die Daten für die Beschreibung des Attributs "MF \_ \_ \_ . MPEG4 Sample \_ Description" nicht ändern, nachdem mindestens ein Muster an die Senke in der [**imfstreamsink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) -Schnittstelle des entsprechenden Streams gesendet wurde</span><span class="sxs-lookup"><span data-stu-id="a2b76-118">When setting this attribute on MPEG-4 sink through [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) method, the data for the attribute MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION should not change after one or more samples have been sent to the sink on the corresponding stream's [**IMFStreamSink::ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) interface.</span></span>

<span data-ttu-id="a2b76-119">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="a2b76-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2b76-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a2b76-120">Requirements</span></span>



| <span data-ttu-id="a2b76-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a2b76-121">Requirement</span></span> | <span data-ttu-id="a2b76-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a2b76-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2b76-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a2b76-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a2b76-124">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b76-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="a2b76-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a2b76-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a2b76-126">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="a2b76-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="a2b76-127">Header</span><span class="sxs-lookup"><span data-stu-id="a2b76-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2b76-128"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2b76-128"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2b76-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2b76-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2b76-130">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a2b76-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2b76-131">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="a2b76-131">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




