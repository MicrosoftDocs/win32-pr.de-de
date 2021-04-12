---
description: Gibt an, ob ein Medien Beispiel nach einer Lücke im Stream das erste Beispiel ist.
ms.assetid: f9e1e700-9958-404d-8b83-08f846f5a1b0
title: MFSampleExtension_Discontinuity-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e401a26c269a3b77d881bc74ae2c7b30d9d88f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527944"
---
# <a name="mfsampleextension_discontinuity-attribute"></a><span data-ttu-id="918c3-103">Discontinuity-Attribut für MF SampleExtension \_</span><span class="sxs-lookup"><span data-stu-id="918c3-103">MFSampleExtension\_Discontinuity attribute</span></span>

<span data-ttu-id="918c3-104">Gibt an, ob ein Medien Beispiel nach einer Lücke im Stream das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="918c3-104">Specifies whether a media sample is the first sample after a gap in the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="918c3-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="918c3-105">Data type</span></span>

<span data-ttu-id="918c3-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="918c3-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="918c3-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="918c3-107">Get/set</span></span>

<span data-ttu-id="918c3-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="918c3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="918c3-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="918c3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="918c3-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="918c3-110">Applies to</span></span>

[<span data-ttu-id="918c3-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="918c3-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="918c3-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="918c3-112">Remarks</span></span>

<span data-ttu-id="918c3-113">Dieses Attribut gilt für Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="918c3-113">This attribute applies to media samples.</span></span> <span data-ttu-id="918c3-114">Wenn dieses Attribut **true** ist, bedeutet dies, dass es eine Diskontinuität im Stream gab, und dieses Beispiel ist der erste, der nach der Lücke angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="918c3-114">If this attribute is **TRUE**, it means there was a discontinuity in the stream and this sample is the first to appear after the gap.</span></span>

<span data-ttu-id="918c3-115">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert **false**.</span><span class="sxs-lookup"><span data-stu-id="918c3-115">If this attribute is not set, the default value is **FALSE**.</span></span>

<span data-ttu-id="918c3-116">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="918c3-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="918c3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="918c3-117">Requirements</span></span>



| <span data-ttu-id="918c3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="918c3-118">Requirement</span></span> | <span data-ttu-id="918c3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="918c3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="918c3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="918c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="918c3-121">Windows Vista \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="918c3-121">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="918c3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="918c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="918c3-123">Windows Server 2008 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="918c3-123">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="918c3-124">Header</span><span class="sxs-lookup"><span data-stu-id="918c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="918c3-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="918c3-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="918c3-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="918c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="918c3-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="918c3-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="918c3-128">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="918c3-128">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="918c3-129">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="918c3-129">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




