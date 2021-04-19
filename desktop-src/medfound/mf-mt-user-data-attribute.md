---
description: Enthält zusätzliche Formatierungsdaten für einen Medientyp.
ms.assetid: 020832c4-40a1-4d8b-ada0-7a04ce097bce
title: MF_MT_USER_DATA-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6042ded0e2d441b0f86c5e1f97557959ce08cd1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351011"
---
# <a name="mf_mt_user_data-attribute"></a><span data-ttu-id="4cec0-103">\_ \_ Benutzer \_ Daten Attribut für MF-MT</span><span class="sxs-lookup"><span data-stu-id="4cec0-103">MF\_MT\_USER\_DATA attribute</span></span>

<span data-ttu-id="4cec0-104">Enthält zusätzliche Formatierungsdaten für einen Medientyp.</span><span class="sxs-lookup"><span data-stu-id="4cec0-104">Contains additional format data for a media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="4cec0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4cec0-105">Data type</span></span>

<span data-ttu-id="4cec0-106">Bytearray</span><span class="sxs-lookup"><span data-stu-id="4cec0-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="4cec0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4cec0-107">Remarks</span></span>

<span data-ttu-id="4cec0-108">Die Bedeutung der Daten in diesem Attribut hängt von dem Format ab, das vom Medientyp beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="4cec0-108">The meaning of the data in this attribute depends on the format that is described by the media type.</span></span>



| <span data-ttu-id="4cec0-109">Formattyp</span><span class="sxs-lookup"><span data-stu-id="4cec0-109">Format Type</span></span>                                                                                                           | <span data-ttu-id="4cec0-110">Zusätzliche Formatierungsdaten</span><span class="sxs-lookup"><span data-stu-id="4cec0-110">Additional Format Data</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cec0-111">Windows Media-Codec.</span><span class="sxs-lookup"><span data-stu-id="4cec0-111">Windows Media codec.</span></span>                                                                                                  | <span data-ttu-id="4cec0-112">Private Codec-Daten.</span><span class="sxs-lookup"><span data-stu-id="4cec0-112">Codec private data.</span></span>                                                                                                                       |
| <span data-ttu-id="4cec0-113">Die konvertierte [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4cec0-113">Converted [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span>   | <span data-ttu-id="4cec0-114">Zusätzliche Daten, die nach der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur angezeigt werden, ohne die Farbtabelle oder Farb Masken.</span><span class="sxs-lookup"><span data-stu-id="4cec0-114">Extra data that appears after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure, not including the color table or color masks.</span></span> |
| <span data-ttu-id="4cec0-115">Konvertierte [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -oder [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4cec0-115">Converted [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> | <span data-ttu-id="4cec0-116">Zusätzliche Daten, die nach der audioformatstruktur angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4cec0-116">Extra data that appears after the audio format structure.</span></span>                                                                                 |



 

<span data-ttu-id="4cec0-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="4cec0-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cec0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4cec0-118">Requirements</span></span>



| <span data-ttu-id="4cec0-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4cec0-119">Requirement</span></span> | <span data-ttu-id="4cec0-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4cec0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cec0-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4cec0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4cec0-122">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4cec0-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4cec0-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4cec0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4cec0-124">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4cec0-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4cec0-125">Header</span><span class="sxs-lookup"><span data-stu-id="4cec0-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cec0-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cec0-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cec0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4cec0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cec0-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4cec0-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4cec0-129">**Imfattributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="4cec0-129">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="4cec0-130">**Imfattributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="4cec0-130">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="4cec0-131">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="4cec0-131">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="4cec0-132">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="4cec0-132">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 
