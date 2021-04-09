---
description: Gibt an, ob die Aufzeichnungs-Engine Videos, aber keine Audiodaten erfasst.
ms.assetid: B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29
title: MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b687bfa7ec2f30f296dd83997f3e64ac4198fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959296"
---
# <a name="mf_capture_engine_use_video_device_only-attribute"></a><span data-ttu-id="3606c-103">Die MF- \_ Erfassungs- \_ Engine \_ verwendet \_ \_ nur Video Geräte \_ Attribute</span><span class="sxs-lookup"><span data-stu-id="3606c-103">MF\_CAPTURE\_ENGINE\_USE\_VIDEO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="3606c-104">Gibt an, ob die Aufzeichnungs-Engine Videos, aber keine Audiodaten erfasst.</span><span class="sxs-lookup"><span data-stu-id="3606c-104">Specifies whether the capture engine captures video but not audio.</span></span>

## <a name="data-type"></a><span data-ttu-id="3606c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="3606c-105">Data type</span></span>

<span data-ttu-id="3606c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3606c-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3606c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3606c-107">Remarks</span></span>

<span data-ttu-id="3606c-108">Wenn dieses Attribut **true** ist, wird von der Aufzeichnungs-Engine kein audioerfassungs-Gerät ausgewählt oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="3606c-108">If this attribute is **TRUE**, the capture engine does not select or use an audio capture device.</span></span> <span data-ttu-id="3606c-109">Legen Sie dieses Attribut auf " **true** " fest, wenn Sie Video ohne Audiodaten erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="3606c-109">Set this attribute to **TRUE** if you want to capture video without audio.</span></span> <span data-ttu-id="3606c-110">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="3606c-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3606c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3606c-111">Requirements</span></span>



| <span data-ttu-id="3606c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3606c-112">Requirement</span></span> | <span data-ttu-id="3606c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3606c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3606c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3606c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3606c-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3606c-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3606c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3606c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3606c-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3606c-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3606c-118">Header</span><span class="sxs-lookup"><span data-stu-id="3606c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3606c-119"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="3606c-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3606c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3606c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3606c-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="3606c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3606c-122">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="3606c-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="3606c-123">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="3606c-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




