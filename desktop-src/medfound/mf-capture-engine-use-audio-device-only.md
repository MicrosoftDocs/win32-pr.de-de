---
description: Gibt an, ob die Aufzeichnungs-Engine Audiodaten erfasst, aber kein Video.
ms.assetid: 0A905D55-CEE5-44FC-97A5-9474872D5724
title: MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f02e0b8f1002bcfff12f8a2bea93612456b6072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959050"
---
# <a name="mf_capture_engine_use_audio_device_only-attribute"></a><span data-ttu-id="a6573-103">Die \_ MF \_ -Erfassungs \_ -Engine verwendet \_ \_ nur Audiogeräte \_ Attribute</span><span class="sxs-lookup"><span data-stu-id="a6573-103">MF\_CAPTURE\_ENGINE\_USE\_AUDIO\_DEVICE\_ONLY attribute</span></span>

<span data-ttu-id="a6573-104">Gibt an, ob die Aufzeichnungs-Engine Audiodaten erfasst, aber kein Video.</span><span class="sxs-lookup"><span data-stu-id="a6573-104">Specifies whether the capture engine captures audio but not video.</span></span>

## <a name="data-type"></a><span data-ttu-id="a6573-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a6573-105">Data type</span></span>

<span data-ttu-id="a6573-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a6573-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a6573-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6573-107">Remarks</span></span>

<span data-ttu-id="a6573-108">Wenn dieses Attribut **true** ist, wird von der Aufzeichnungs-Engine kein Video Erfassungsgerät ausgewählt oder verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6573-108">If this attribute is **TRUE**, the capture engine does not select or use a video capture device.</span></span> <span data-ttu-id="a6573-109">Legen Sie dieses Attribut auf " **true** " fest, wenn Sie Audiodaten ohne Video erfassen möchten.</span><span class="sxs-lookup"><span data-stu-id="a6573-109">Set this attribute to **TRUE** if you want to capture audio without video.</span></span> <span data-ttu-id="a6573-110">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6573-110">The default value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6573-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6573-111">Requirements</span></span>



| <span data-ttu-id="a6573-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6573-112">Requirement</span></span> | <span data-ttu-id="a6573-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a6573-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6573-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a6573-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a6573-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6573-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a6573-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a6573-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a6573-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a6573-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a6573-118">Header</span><span class="sxs-lookup"><span data-stu-id="a6573-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6573-119"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6573-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6573-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6573-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6573-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a6573-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6573-122">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="a6573-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="a6573-123">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="a6573-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




