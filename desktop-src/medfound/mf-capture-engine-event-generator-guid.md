---
description: Identifiziert die Komponente, die ein Aufzeichnungs Ereignis generiert hat.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9a5068db357523a626404910fb7d752ea0b621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349039"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a><span data-ttu-id="d07a6-103">\_ \_ \_ \_ \_ GUID-Attribut des MF-Erfassungs Moduls</span><span class="sxs-lookup"><span data-stu-id="d07a6-103">MF\_CAPTURE\_ENGINE\_EVENT\_GENERATOR\_GUID attribute</span></span>

<span data-ttu-id="d07a6-104">Identifiziert die Komponente, die ein Aufzeichnungs Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="d07a6-104">Identifies the component that generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="d07a6-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d07a6-105">Data type</span></span>

<span data-ttu-id="d07a6-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="d07a6-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="d07a6-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d07a6-107">Remarks</span></span>

<span data-ttu-id="d07a6-108">Dieses Attribut wird für einige Ereignisse der Aufzeichnungs-Engine angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d07a6-108">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="d07a6-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) für das Ereignis Objekt.</span><span class="sxs-lookup"><span data-stu-id="d07a6-109">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) on the event object.</span></span> <span data-ttu-id="d07a6-110">Das Ereignis Objekt wird über die [**imfcaptureengineoneventcallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) -Methode an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d07a6-110">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

<span data-ttu-id="d07a6-111">Der Wert ist ein Schnittstellen Bezeichner für die Komponente, die das Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="d07a6-111">The value is an interface identifier for the component that generated the event.</span></span> <span data-ttu-id="d07a6-112">Beispielsweise gibt der Wert **IID \_ IMF capturepreviewsink** die Vorschau Senke ([**IMF capturepreviewsink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)) an.</span><span class="sxs-lookup"><span data-stu-id="d07a6-112">For example, the value **IID\_IMFCapturePreviewSink** indicates the preview sink ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)).</span></span> <span data-ttu-id="d07a6-113">Nicht jedes Aufzeichnungs Ereignis enthält dieses Attribut.</span><span class="sxs-lookup"><span data-stu-id="d07a6-113">Not every capture event contains this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="d07a6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d07a6-114">Requirements</span></span>



| <span data-ttu-id="d07a6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d07a6-115">Requirement</span></span> | <span data-ttu-id="d07a6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d07a6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d07a6-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d07a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d07a6-118">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d07a6-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d07a6-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d07a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d07a6-120">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d07a6-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d07a6-121">Header</span><span class="sxs-lookup"><span data-stu-id="d07a6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d07a6-122"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d07a6-122"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d07a6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d07a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d07a6-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d07a6-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d07a6-125">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="d07a6-125">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="d07a6-126">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="d07a6-126">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




