---
description: Offset zwischen dem Zeitstempel jedes Beispiels, das von der Sample Webbannergrabber empfangen wurde, und dem Zeitpunkt, zu dem der Sample Webbannergrabber das Beispiel darstellt.
ms.assetid: 8d06b415-aafc-4276-9a88-4b7262df62f1
title: MF_SAMPLEGRABBERSINK_SAMPLE_TIME_OFFSET-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d99f65c5023bbe8705e21269dfb07d6f24db4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359906"
---
# <a name="mf_samplegrabbersink_sample_time_offset-attribute"></a><span data-ttu-id="01a75-103">MF \_ samplegrabbersink- \_ Beispiel für \_ Zeit \_ Offset Attribut</span><span class="sxs-lookup"><span data-stu-id="01a75-103">MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="01a75-104">Offset zwischen dem Zeitstempel jedes Beispiels, das von der Sample Webbannergrabber empfangen wurde, und dem Zeitpunkt, zu dem der Sample Webbannergrabber das Beispiel darstellt.</span><span class="sxs-lookup"><span data-stu-id="01a75-104">Offset between the time stamp on each sample received by the sample grabber, and the time when the sample grabber presents the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="01a75-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="01a75-105">Data type</span></span>

<span data-ttu-id="01a75-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="01a75-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="01a75-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01a75-107">Remarks</span></span>

<span data-ttu-id="01a75-108">Sie können dieses Attribut für das [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt festlegen, das von der [**mfikreatesamplegrabbersink Aktivierungs**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) -Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="01a75-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object that is returned by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="01a75-109">Mit diesem Attribut kann die Rückruffunktion des beispielgrabers Beispiele vor der Präsentationszeit empfangen.</span><span class="sxs-lookup"><span data-stu-id="01a75-109">This attribute enables the sample grabber's callback function to receive samples earlier than the presentation time.</span></span>

<span data-ttu-id="01a75-110">Wenn der Sample Webbannergrabber ein neues Beispiel erhält, wird das Beispiel zum Zeitpunkt *t* - *Offset* dargestellt, wobei *t* der Zeitstempel für das Beispiel und *Offset* der Wert dieses Attributs ist.</span><span class="sxs-lookup"><span data-stu-id="01a75-110">When the sample grabber receives a new sample, it presents the sample at time *t* − *offset*, where *t* is the time stamp on the sample and *offset* is the value of this attribute.</span></span> <span data-ttu-id="01a75-111">Wenn dieses Attribut nicht festgelegt ist, ist der Standardwert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="01a75-111">If this attribute is not set, the default value is zero.</span></span>

<span data-ttu-id="01a75-112">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="01a75-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="01a75-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01a75-113">Requirements</span></span>



| <span data-ttu-id="01a75-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01a75-114">Requirement</span></span> | <span data-ttu-id="01a75-115">Wert</span><span class="sxs-lookup"><span data-stu-id="01a75-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="01a75-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="01a75-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01a75-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01a75-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="01a75-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="01a75-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01a75-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="01a75-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="01a75-120">Header</span><span class="sxs-lookup"><span data-stu-id="01a75-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="01a75-121"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="01a75-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01a75-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01a75-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01a75-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="01a75-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="01a75-124">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="01a75-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="01a75-125">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="01a75-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="01a75-126">**Imbersamplegrabbersinkcallback**</span><span class="sxs-lookup"><span data-stu-id="01a75-126">**IMFSampleGrabberSinkCallback**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback)
</dt> <dt>

[<span data-ttu-id="01a75-127">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="01a75-127">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




