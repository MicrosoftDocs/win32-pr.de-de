---
description: Gibt an, ob die Videostabilisierung auf einen Videoframe angewendet wurde.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode-Attribut (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350581"
---
# <a name="mfsampleextension_videodspmode-attribute"></a><span data-ttu-id="3116d-103">MF Sample Extension \_ videodspmode-Attribut</span><span class="sxs-lookup"><span data-stu-id="3116d-103">MFSampleExtension\_VideoDSPMode attribute</span></span>

<span data-ttu-id="3116d-104">Gibt an, ob die Videostabilisierung auf einen Videoframe angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3116d-104">Indicates whether video stabilization was applied to a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="3116d-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3116d-105">Data type</span></span>

<span data-ttu-id="3116d-106">**MF videodspmode** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3116d-106">**MFVideoDSPMode** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="3116d-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="3116d-107">Get/set</span></span>

<span data-ttu-id="3116d-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="3116d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="3116d-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="3116d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="3116d-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="3116d-110">Applies to</span></span>

[<span data-ttu-id="3116d-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="3116d-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="3116d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3116d-112">Remarks</span></span>

<span data-ttu-id="3116d-113">Das [**Videostabilisierung-MFT**](video-stabilization-mft.md) legt dieses Attribut auf die Ausgabe Beispiele fest, die es erzeugt.</span><span class="sxs-lookup"><span data-stu-id="3116d-113">The [**Video Stabilization MFT**](video-stabilization-mft.md) sets this attribute on the output samples that it produces.</span></span> <span data-ttu-id="3116d-114">Der Wert des-Attributs ist ein [**MF videodspmode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) -Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="3116d-114">The value of the attribute is an [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) enumeration value.</span></span> <span data-ttu-id="3116d-115">Wenn der Wert **mfvideodspmode- \_ Stabilisierung** ist, bedeutet dies, dass die MFT die Bildstabilisierung auf den Frame angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="3116d-115">If the value is **MFVideoDSPMode\_Stabilization**, it means that the MFT applied image stabilization to the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="3116d-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3116d-116">Requirements</span></span>



| <span data-ttu-id="3116d-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3116d-117">Requirement</span></span> | <span data-ttu-id="3116d-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3116d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3116d-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3116d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3116d-120">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3116d-120">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3116d-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3116d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3116d-122">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3116d-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3116d-123">Header</span><span class="sxs-lookup"><span data-stu-id="3116d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3116d-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3116d-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3116d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3116d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3116d-126">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3116d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3116d-127">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="3116d-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="3116d-128">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="3116d-128">Media Samples</span></span>](media-samples.md)
</dt> <dt>

[<span data-ttu-id="3116d-129">**Videostabilisierung-MFT**</span><span class="sxs-lookup"><span data-stu-id="3116d-129">**Video Stabilization MFT**</span></span>](video-stabilization-mft.md)
</dt> </dl>

 

 




