---
description: Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Audiopfad der Daten Satz Senke gepuffert werden können.
ms.assetid: C959ED58-77EB-47EC-8D5D-BBFA9342295D
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442e9b5eca3354e87b8e36b55a3c6cb92ec6f131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344579"
---
# <a name="mf_capture_engine_record_sink_audio_max_unprocessed_samples-attribute"></a><span data-ttu-id="754f1-103">Daten \_ \_ Satz \ \_ \_ \_ \_ Maximales \_ nicht verarbeitetes \_ Samples-Attribut der MF-Erfassung</span><span class="sxs-lookup"><span data-stu-id="754f1-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="754f1-104">Legt die maximale Anzahl nicht verarbeiteter Beispiele fest, die für die Verarbeitung im Audiopfad der Daten Satz Senke gepuffert werden können.</span><span class="sxs-lookup"><span data-stu-id="754f1-104">Sets the maximum number of unprocessed samples that can be buffered for processing in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="754f1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="754f1-105">Data type</span></span>

<span data-ttu-id="754f1-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="754f1-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="754f1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="754f1-107">Remarks</span></span>

<span data-ttu-id="754f1-108">Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="754f1-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="754f1-109">Der Höchstwert für dieses Attribut ist 100.</span><span class="sxs-lookup"><span data-stu-id="754f1-109">The maximum value for this attribute is 100.</span></span>

<span data-ttu-id="754f1-110">Nachdem der Datensatz die maximale Anzahl nicht verarbeiteter Stichproben gepuffert hat, die durch die MF \_ -Erfassungs \_ -Engine aufgezeichnet wurde, die \_ \_ \_ \_ \_ nicht verarbeiteten \_ Beispiele enthält, wird die Framerate durch Verwerfen von Beispielen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="754f1-110">Once the record has buffered the maximum number of unprocessed samples, specified by MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_UNPROCESSED\_SAMPLES, it drops the frame rate by dropping samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="754f1-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="754f1-111">Requirements</span></span>



| <span data-ttu-id="754f1-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="754f1-112">Requirement</span></span> | <span data-ttu-id="754f1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="754f1-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="754f1-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="754f1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="754f1-115">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="754f1-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="754f1-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="754f1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="754f1-117">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="754f1-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="754f1-118">Header</span><span class="sxs-lookup"><span data-stu-id="754f1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="754f1-119"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="754f1-119"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="754f1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="754f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754f1-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="754f1-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="754f1-122">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="754f1-122">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="754f1-123">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="754f1-123">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




