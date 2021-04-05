---
description: Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Video Pfad der Daten Satz Senke gepuffert werden können.
ms.assetid: 5AFA197E-5A7F-402E-A62B-4F624A5DD917
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70c3840f449cebb6579b2c1df5f330379ba30655
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752456"
---
# <a name="mf_capture_engine_record_sink_video_max_processed_samples-attribute"></a><span data-ttu-id="a8061-103">\_ \_ \_ Daten Satz-Sink-Video Daten Satz- \_ Sink- \_ Video \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="a8061-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="a8061-104">Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Video Pfad der Daten Satz Senke gepuffert werden können.</span><span class="sxs-lookup"><span data-stu-id="a8061-104">Sets the maximum number of processed samples that can be buffered in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="a8061-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a8061-105">Data type</span></span>

<span data-ttu-id="a8061-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a8061-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a8061-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8061-107">Remarks</span></span>

<span data-ttu-id="a8061-108">Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a8061-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="a8061-109">Der Maximalwert für dieses Attribut ist 17.</span><span class="sxs-lookup"><span data-stu-id="a8061-109">The maximum value for this attribute is 17.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8061-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8061-110">Requirements</span></span>



| <span data-ttu-id="a8061-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8061-111">Requirement</span></span> | <span data-ttu-id="a8061-112">Wert</span><span class="sxs-lookup"><span data-stu-id="a8061-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8061-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8061-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a8061-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8061-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a8061-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8061-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a8061-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8061-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a8061-117">Header</span><span class="sxs-lookup"><span data-stu-id="a8061-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8061-118"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8061-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8061-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8061-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8061-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a8061-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8061-121">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="a8061-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="a8061-122">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="a8061-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




