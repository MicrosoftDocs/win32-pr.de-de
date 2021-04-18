---
description: Gibt eine Zahl zwischen 0 und 100 an, die den Kompromiss zwischen Codierungsqualität und Codierungs Geschwindigkeit angibt.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: MF_TRANSCODE_QUALITYVSSPEED-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371476"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="0594b-103">MF- \_ transcode \_ qualityvsspeed-Attribut</span><span class="sxs-lookup"><span data-stu-id="0594b-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="0594b-104">Gibt eine Zahl zwischen 0 und 100 an, die den Kompromiss zwischen Codierungsqualität und Codierungs Geschwindigkeit angibt.</span><span class="sxs-lookup"><span data-stu-id="0594b-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="0594b-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0594b-105">Data type</span></span>

<span data-ttu-id="0594b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0594b-106">**UINT32**</span></span>

<span data-ttu-id="0594b-107">Der Wert dieser Eigenschaft hat den folgenden Bereich.</span><span class="sxs-lookup"><span data-stu-id="0594b-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="0594b-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0594b-108">Value</span></span>                                                                          | <span data-ttu-id="0594b-109">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="0594b-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="0594b-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0594b-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="0594b-111">Niedrigere Qualität, schnellere Codierung.</span><span class="sxs-lookup"><span data-stu-id="0594b-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="0594b-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="0594b-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="0594b-113">Höhere Qualität, langsamere Codierung.</span><span class="sxs-lookup"><span data-stu-id="0594b-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="0594b-114">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="0594b-114">Get/set</span></span>

<span data-ttu-id="0594b-115">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0594b-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0594b-116">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0594b-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0594b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0594b-117">Remarks</span></span>

<span data-ttu-id="0594b-118">Dieses Attribut hat denselben GUID-Wert wie die Eigenschaft " [avenccommonqualityvsspeed](../directshow/avenccommonqualityvsspeed-property.md) ", die für [**icodecapi**](/windows/win32/api/strmif/nn-strmif-icodecapi)definiert ist, und hat dieselbe Interpretation.</span><span class="sxs-lookup"><span data-stu-id="0594b-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="0594b-119">Die Anwendung kann dieses Attribut für das transcodieren-Profil festlegen, bevor die transcodieren-Topologie für Windows Media Codecs zu erstellen ist.</span><span class="sxs-lookup"><span data-stu-id="0594b-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="0594b-120">Der Wert muss zwischen 0 und 100 liegen.</span><span class="sxs-lookup"><span data-stu-id="0594b-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="0594b-121">Für den Videostream ordnet der transcodieren-Topologiegenerator dem von der Anwendung angegebenen Wert einen Wert zu und gibt den zugeordneten Wert an die **\_ complexityex-Eigenschaft von mfpkey** des Encoders an.</span><span class="sxs-lookup"><span data-stu-id="0594b-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="0594b-122">Niedrigere Werte ermöglichen es dem Encoder, weniger komplizierte Codierungs Algorithmen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0594b-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="0594b-123">Die Verwendung einfacherer Algorithmen erzeugt eine Ausgabe mit geringerer Qualität, aber der Codierungsprozess ist schneller und erfordert weniger Verarbeitungsleistung.</span><span class="sxs-lookup"><span data-stu-id="0594b-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="0594b-124">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0594b-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0594b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0594b-125">Requirements</span></span>



| <span data-ttu-id="0594b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0594b-126">Requirement</span></span> | <span data-ttu-id="0594b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0594b-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0594b-128">Header</span><span class="sxs-lookup"><span data-stu-id="0594b-128">Header</span></span><br/> | <dl> <span data-ttu-id="0594b-129"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0594b-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0594b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0594b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0594b-131">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0594b-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0594b-132">Transcode-API</span><span class="sxs-lookup"><span data-stu-id="0594b-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="0594b-133">**IMF transcodeprofile:: setvideoattribute**</span><span class="sxs-lookup"><span data-stu-id="0594b-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
