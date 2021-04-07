---
description: Gibt an, welcher Stream ein Aufzeichnungs Ereignis generiert hat.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863596"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a><span data-ttu-id="a5203-103">Daten \_ \_ Strom- \_ \_ \_ Index Attribut für das MF-Erfassungs Modul</span><span class="sxs-lookup"><span data-stu-id="a5203-103">MF\_CAPTURE\_ENGINE\_EVENT\_STREAM\_INDEX attribute</span></span>

<span data-ttu-id="a5203-104">Gibt an, welcher Stream ein Aufzeichnungs Ereignis generiert hat.</span><span class="sxs-lookup"><span data-stu-id="a5203-104">Identifies which stream generated a capture event.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5203-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="a5203-105">Data type</span></span>

<span data-ttu-id="a5203-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a5203-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="a5203-107">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="a5203-107">Get/set</span></span>

<span data-ttu-id="a5203-108">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="a5203-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5203-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5203-109">Remarks</span></span>

<span data-ttu-id="a5203-110">Dieses Attribut wird für einige Ereignisse der Aufzeichnungs-Engine angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a5203-110">This attribute appears on some events from the capture engine.</span></span> <span data-ttu-id="a5203-111">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) für das Ereignis Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5203-111">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) on the event object.</span></span> <span data-ttu-id="a5203-112">Das Ereignis Objekt wird über die [**imfcaptureengineoneventcallback:: OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) -Methode an die Anwendung übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a5203-112">The event object is passed to the application through the [**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5203-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5203-113">Requirements</span></span>



| <span data-ttu-id="a5203-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5203-114">Requirement</span></span> | <span data-ttu-id="a5203-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a5203-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5203-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5203-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5203-117">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5203-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="a5203-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5203-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5203-119">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5203-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a5203-120">Header</span><span class="sxs-lookup"><span data-stu-id="a5203-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5203-121"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5203-121"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5203-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5203-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5203-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="a5203-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a5203-124">**IMF captureengineoneventcallback:: OnEvent**</span><span class="sxs-lookup"><span data-stu-id="a5203-124">**IMFCaptureEngineOnEventCallback::OnEvent**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




