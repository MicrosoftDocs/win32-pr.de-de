---
description: Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Audiopfad der Daten Satz Senke gepuffert werden können.
ms.assetid: 216886DB-B206-4944-925A-C2106331F1CB
title: MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d1ce4d649c75106545eb2ff39d4f3ea742e6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526906"
---
# <a name="mf_capture_engine_record_sink_audio_max_processed_samples-attribute"></a><span data-ttu-id="bd6f6-103">MF \_ -Erfassungs Modul \_ \_ Daten Satz \_ \_ -senkendatei ( \_ Max \_ \_</span><span class="sxs-lookup"><span data-stu-id="bd6f6-103">MF\_CAPTURE\_ENGINE\_RECORD\_SINK\_AUDIO\_MAX\_PROCESSED\_SAMPLES attribute</span></span>

<span data-ttu-id="bd6f6-104">Legt die maximale Anzahl von verarbeiteten Stichproben fest, die im Audiopfad der Daten Satz Senke gepuffert werden können.</span><span class="sxs-lookup"><span data-stu-id="bd6f6-104">Sets the maximum number of processed samples that can be buffered in the record sink audio path.</span></span>

## <a name="data-type"></a><span data-ttu-id="bd6f6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bd6f6-105">Data type</span></span>

<span data-ttu-id="bd6f6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bd6f6-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6f6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd6f6-107">Remarks</span></span>

<span data-ttu-id="bd6f6-108">Um dieses Attribut für die Aufzeichnungs-Engine zu konfigurieren, fügen Sie es dem *pattributes* -Parameter hinzu, wenn Sie [**imfcaptureengine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bd6f6-108">To configure this attribute on the capture engine, add it to the *pAttributes* parameter when you call [**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize).</span></span>

<span data-ttu-id="bd6f6-109">Der Höchstwert für dieses Attribut ist 100.</span><span class="sxs-lookup"><span data-stu-id="bd6f6-109">The maximum value for this attribute is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6f6-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd6f6-110">Requirements</span></span>



| <span data-ttu-id="bd6f6-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd6f6-111">Requirement</span></span> | <span data-ttu-id="bd6f6-112">Wert</span><span class="sxs-lookup"><span data-stu-id="bd6f6-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6f6-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd6f6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6f6-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd6f6-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="bd6f6-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd6f6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6f6-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd6f6-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd6f6-117">Header</span><span class="sxs-lookup"><span data-stu-id="bd6f6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6f6-118"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6f6-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd6f6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd6f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6f6-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bd6f6-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd6f6-121">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="bd6f6-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd6f6-122">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="bd6f6-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




