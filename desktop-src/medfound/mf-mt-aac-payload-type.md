---
description: Gibt den Nutz Lasttyp eines AAC-Streams (Advanced audiocoding) an.
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: MF_MT_AAC_PAYLOAD_TYPE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358230"
---
# <a name="mf_mt_aac_payload_type-attribute"></a><span data-ttu-id="b5675-103">MF \_ MT- \_ AAC-Attribut für \_ Nutz Last \_ Typen</span><span class="sxs-lookup"><span data-stu-id="b5675-103">MF\_MT\_AAC\_PAYLOAD\_TYPE attribute</span></span>

<span data-ttu-id="b5675-104">Gibt den Nutz Lasttyp eines AAC-Streams (Advanced audiocoding) an.</span><span class="sxs-lookup"><span data-stu-id="b5675-104">Specifies the payload type of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="b5675-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b5675-105">Data type</span></span>

<span data-ttu-id="b5675-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b5675-106">**UINT32**</span></span>

<span data-ttu-id="b5675-107">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="b5675-107">The following values are possible.</span></span>



| <span data-ttu-id="b5675-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b5675-108">Value</span></span>                                                                        | <span data-ttu-id="b5675-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b5675-109">Meaning</span></span>                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5675-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b5675-110"><dt>0</dt></span></span> </dl> | <span data-ttu-id="b5675-111">Der Stream enthält \_ nur Rohdaten \_ Block Elemente.</span><span class="sxs-lookup"><span data-stu-id="b5675-111">The stream contains raw\_data\_block elements only.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="b5675-112"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b5675-112"><dt>1</dt></span></span> </dl> | <span data-ttu-id="b5675-113">Der audiodatentransport-Stream (ADTs).</span><span class="sxs-lookup"><span data-stu-id="b5675-113">Audio Data Transport Stream (ADTS).</span></span> <span data-ttu-id="b5675-114">Der Stream enthält eine \_ von MPEG-2 definierte ADTs-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="b5675-114">The stream contains an adts\_sequence, as defined by MPEG-2.</span></span><br/>                       |
| <dl> <span data-ttu-id="b5675-115"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b5675-115"><dt>2</dt></span></span> </dl> | <span data-ttu-id="b5675-116">Das Format für den audiodatenaustausch (ADIF).</span><span class="sxs-lookup"><span data-stu-id="b5675-116">Audio Data Interchange Format (ADIF).</span></span> <span data-ttu-id="b5675-117">Der Stream enthält eine ADIF \_ -Sequenz, wie in MPEG-2 definiert.</span><span class="sxs-lookup"><span data-stu-id="b5675-117">The stream contains an adif\_sequence, as defined by MPEG-2.</span></span><br/>                     |
| <dl> <span data-ttu-id="b5675-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b5675-118"><dt>3</dt></span></span> </dl> | <span data-ttu-id="b5675-119">Der Stream enthält einen MPEG-4-audiotransportstream mit einer Synchronisierungs Schicht (LoAs) und einer Multiplex Schicht (latm).</span><span class="sxs-lookup"><span data-stu-id="b5675-119">The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="b5675-120">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b5675-120">Get/set</span></span>

<span data-ttu-id="b5675-121">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b5675-121">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b5675-122">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b5675-122">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b5675-123">Gilt für</span><span class="sxs-lookup"><span data-stu-id="b5675-123">Applies To</span></span>

[<span data-ttu-id="b5675-124">**IMF MediaType**</span><span class="sxs-lookup"><span data-stu-id="b5675-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="b5675-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5675-125">Remarks</span></span>

<span data-ttu-id="b5675-126">Der MF \_ MT- \_ AAC- \_ Nutz \_ Lasttyp ist optional.</span><span class="sxs-lookup"><span data-stu-id="b5675-126">MF\_MT\_AAC\_PAYLOAD\_TYPE is optional.</span></span> <span data-ttu-id="b5675-127">Wenn dieses Attribut nicht angegeben wird, wird der Standardwert 0 verwendet, der angibt, dass der Stream \_ \_ nur rohdatenblock-Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="b5675-127">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw\_data\_block elements only.</span></span>

<span data-ttu-id="b5675-128">Gilt nur für **mfaudioformat- \_ AAC**.</span><span class="sxs-lookup"><span data-stu-id="b5675-128">Applies only to **MFAudioFormat\_AAC**.</span></span>

<span data-ttu-id="b5675-129">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="b5675-129">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5675-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5675-130">Requirements</span></span>



| <span data-ttu-id="b5675-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5675-131">Requirement</span></span> | <span data-ttu-id="b5675-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b5675-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5675-133">Header</span><span class="sxs-lookup"><span data-stu-id="b5675-133">Header</span></span><br/> | <dl> <span data-ttu-id="b5675-134"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5675-134"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5675-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5675-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5675-136">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b5675-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b5675-137">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="b5675-137">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




