---
description: Enthält den Zeitstempel des Gerätetreibers.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: MFSampleExtension_DeviceTimestamp-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285b354ecd0e399fc297d3677d29b88847f9eba8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863972"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a><span data-ttu-id="e34b2-103">Devicetimestamp-Attribut für MF Sample Extension \_</span><span class="sxs-lookup"><span data-stu-id="e34b2-103">MFSampleExtension\_DeviceTimestamp attribute</span></span>

<span data-ttu-id="e34b2-104">Enthält den Zeitstempel des Gerätetreibers.</span><span class="sxs-lookup"><span data-stu-id="e34b2-104">Contains the time stamp from the device driver.</span></span>

## <a name="data-type"></a><span data-ttu-id="e34b2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e34b2-105">Data type</span></span>

<span data-ttu-id="e34b2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e34b2-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="e34b2-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="e34b2-107">Get/set</span></span>

<span data-ttu-id="e34b2-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="e34b2-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="e34b2-109">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="e34b2-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e34b2-110">Gilt für:</span><span class="sxs-lookup"><span data-stu-id="e34b2-110">Applies to</span></span>

[<span data-ttu-id="e34b2-111">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="e34b2-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="e34b2-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e34b2-112">Remarks</span></span>

<span data-ttu-id="e34b2-113">Dieses Attribut wird für Medien Beispiele festgelegt, die von einer Medienquelle für ein Erfassungsgerät erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="e34b2-113">This attribute is set on media samples created by a media source for a capture device.</span></span> <span data-ttu-id="e34b2-114">Der Wert dieses Attributs ist in der [**MF-Zeit**](mftime.md) Domäne, und es wird eine Epoche mit der QPC-Zeit (Query Performance Counter) gemeinsam genutzt, die immer in 100-ns-Einheiten ausgedrückt wird</span><span class="sxs-lookup"><span data-stu-id="e34b2-114">This attribute's value is in the [**MFTIME**](mftime.md) domain, sharing an epoch with query performance counter (QPC) time and always expressed in 100ns units.</span></span> <span data-ttu-id="e34b2-115">Dieses Attribut ist für MFTs verfügbar, die in die Aufzeichnungs Pipeline eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e34b2-115">This attribute is available for MFTs inserted into the capture pipeline.</span></span>

<span data-ttu-id="e34b2-116">Um den Zeitstempel relativ zum Start des Streamings abzurufen, müssen Sie die [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e34b2-116">To get the time stamp relative to the start of streaming, call the [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) method.</span></span>

<span data-ttu-id="e34b2-117">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="e34b2-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e34b2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e34b2-118">Requirements</span></span>



| <span data-ttu-id="e34b2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e34b2-119">Requirement</span></span> | <span data-ttu-id="e34b2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e34b2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e34b2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e34b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e34b2-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e34b2-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e34b2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e34b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e34b2-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e34b2-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e34b2-125">Header</span><span class="sxs-lookup"><span data-stu-id="e34b2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e34b2-126"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e34b2-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e34b2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e34b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e34b2-128">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="e34b2-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e34b2-129">Audio-/Videoerfassung in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e34b2-129">Audio/Video Capture in Media Foundation</span></span>](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="e34b2-130">Beispiel Attribute</span><span class="sxs-lookup"><span data-stu-id="e34b2-130">Sample Attributes</span></span>](sample-attributes.md)
</dt> </dl>

 

 




