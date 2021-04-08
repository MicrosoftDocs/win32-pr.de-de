---
description: Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Video Pfad der Daten Satz Senke gepuffert werden können.
ms.assetid: B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6
title: MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f5e297ddb5f06e71fe05a95df73aa205a7889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863595"
---
# <a name="mf_capture_engine_record_sink_video_max_unprocessed_samples-attribute"></a><span data-ttu-id="ecf1c-103">\_ \_ \_ Daten Satz-Sink \_ - \_ Video \_ \_ \_ für die MF-Erfassung-Video</span><span class="sxs-lookup"><span data-stu-id="ecf1c-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="ecf1c-104">Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Video Pfad der Daten Satz Senke gepuffert werden können.</span><span class="sxs-lookup"><span data-stu-id="ecf1c-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink video path.</span></span>

## <a name="data-type"></a><span data-ttu-id="ecf1c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ecf1c-105">Data type</span></span>

<span data-ttu-id="ecf1c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ecf1c-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf1c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ecf1c-107">Remarks</span></span>

<span data-ttu-id="ecf1c-108">Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ecf1c-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="ecf1c-109">Der Maximalwert für dieses Attribut ist 17.</span><span class="sxs-lookup"><span data-stu-id="ecf1c-109">The maximum value for this attribute is 17.</span></span>

<span data-ttu-id="ecf1c-110">Nachdem der Datensatz die maximale Anzahl nicht verarbeiteter Stichproben gepuffert hat, die von der MF-Aufzeichnungs- \_ \_ Engine- \_ Daten Satz- \_ \_ senkenvideo \_ Max \_ . nicht verarbeitete Beispiele angegeben wurde \_ , wird die Frame Rate durch Verwerfen von</span><span class="sxs-lookup"><span data-stu-id="ecf1c-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_VIDEO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf1c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ecf1c-111">Requirements</span></span>



| <span data-ttu-id="ecf1c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ecf1c-112">Requirement</span></span> | <span data-ttu-id="ecf1c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ecf1c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf1c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ecf1c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf1c-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecf1c-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="ecf1c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ecf1c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf1c-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ecf1c-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ecf1c-118">Header</span><span class="sxs-lookup"><span data-stu-id="ecf1c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf1c-119"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf1c-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf1c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecf1c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf1c-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ecf1c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecf1c-122">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="ecf1c-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="ecf1c-123">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="ecf1c-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




