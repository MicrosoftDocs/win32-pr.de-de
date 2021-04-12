---
description: 'Gibt an, dass der Ausgabetyp für die Aufzeichnungs-Engine als Antwort auf IMFCaptureSink2:: setoutputtype festgelegt wurde.'
ms.assetid: A48CBC82-87C2-4AED-B7E0-B7C60FCCE4CC
title: MF_CAPTURE_ENGINE_OUTPUT_MEDIA_TYPE_SET-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5819de6a07f3b6a339400d65ff9260c33b14c592
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351648"
---
# <a name="mf_capture_engine_output_media_type_set-attribute"></a><span data-ttu-id="25695-103">Set-Attribut der MF- \_ Erfassungs- \_ Engine- \_ Ausgabe \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="25695-103">MF\_CAPTURE\_ENGINE\_OUTPUT\_MEDIA\_TYPE\_SET attribute</span></span>

<span data-ttu-id="25695-104">Gibt an, dass der Ausgabetyp für die Aufzeichnungs-Engine als Antwort auf [**IMFCaptureSink2:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="25695-104">Indicates that the output type has been set on the capture engine in response to [**IMFCaptureSink2::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

## <a name="data-type"></a><span data-ttu-id="25695-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25695-105">Data type</span></span>

<span data-ttu-id="25695-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="25695-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="25695-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25695-107">Remarks</span></span>

<span data-ttu-id="25695-108">Sie können [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) aufrufen, um herauszufinden, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="25695-108">You can call [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstatus) to find out if the operation was successful or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="25695-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25695-109">Requirements</span></span>



| <span data-ttu-id="25695-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25695-110">Requirement</span></span> | <span data-ttu-id="25695-111">Wert</span><span class="sxs-lookup"><span data-stu-id="25695-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25695-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25695-112">Minimum supported client</span></span><br/> | <span data-ttu-id="25695-113">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="25695-113">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="25695-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25695-114">Minimum supported server</span></span><br/> | <span data-ttu-id="25695-115">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="25695-115">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25695-116">Header</span><span class="sxs-lookup"><span data-stu-id="25695-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="25695-117"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="25695-117"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="25695-118">IDL</span><span class="sxs-lookup"><span data-stu-id="25695-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25695-119"><dt>MF-Engine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25695-119"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25695-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25695-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25695-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="25695-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="25695-122">**IMFCaptureSink2:: setoutputtype**</span><span class="sxs-lookup"><span data-stu-id="25695-122">**IMFCaptureSink2::SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
</dt> </dl>

 

 




