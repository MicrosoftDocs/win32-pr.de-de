---
description: Gibt die endgültige Ebene des Codierungs Puffers am Ende des Codierungs Prozesses in Bits an. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Avenccommonbufferoutlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346202"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="b1316-104">Avenccommonbufferoutlevel (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b1316-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="b1316-105">Gibt die endgültige Ebene des Codierungs Puffers am Ende des Codierungs Prozesses in Bits an.</span><span class="sxs-lookup"><span data-stu-id="b1316-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="b1316-106">Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.</span><span class="sxs-lookup"><span data-stu-id="b1316-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="b1316-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b1316-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="b1316-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b1316-108">Data type</span></span>

<span data-ttu-id="b1316-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="b1316-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b1316-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="b1316-110">Property GUID</span></span>

<span data-ttu-id="b1316-111">**Codecapi \_ avenccommonbufferoutlevel**</span><span class="sxs-lookup"><span data-stu-id="b1316-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="b1316-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b1316-112">Property value</span></span>

<span data-ttu-id="b1316-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="b1316-113">This property has a linear range of values.</span></span> <span data-ttu-id="b1316-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="b1316-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1316-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1316-115">Remarks</span></span>

<span data-ttu-id="b1316-116">Die-Eigenschaft ist nur verfügbar, wenn die Codierungs Dauer im Voraus mithilfe der Eigenschaft " [**avencvideonooffieldstoencode**](avencvideonooffieldstoencode-property.md) " oder der Eigenschaft " [**avencaudiointervaltoencode**](avencaudiointervaltoencode-property.md) " definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b1316-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="b1316-117">Bei MPEG-Videos definiert diese Eigenschaft am Ende des Codierungs Prozesses den VBV-Füllungs Bereich (Video Buffer Verifier).</span><span class="sxs-lookup"><span data-stu-id="b1316-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="b1316-118">Die Verkettung von Streams während der Codierung wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b1316-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1316-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1316-119">Requirements</span></span>



| <span data-ttu-id="b1316-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1316-120">Requirement</span></span> | <span data-ttu-id="b1316-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b1316-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1316-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1316-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1316-123">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b1316-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="b1316-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1316-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1316-125">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b1316-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b1316-126">Header</span><span class="sxs-lookup"><span data-stu-id="b1316-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1316-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1316-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1316-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1316-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1316-129">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="b1316-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="b1316-130">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b1316-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




