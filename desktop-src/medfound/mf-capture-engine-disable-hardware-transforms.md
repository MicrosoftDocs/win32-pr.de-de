---
description: Deaktiviert die Verwendung von hardwarebasierten Media Foundation Transformationen (MFTs) in der Erfassungs-Engine.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343403"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="0c3c0-103">MF \_ Capture- \_ Engine-Attribut " \_ \_ Hardware \_ Transformationen deaktivieren"</span><span class="sxs-lookup"><span data-stu-id="0c3c0-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="0c3c0-104">Deaktiviert die Verwendung von hardwarebasierten Media Foundation Transformationen (MFTs) in der Erfassungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="0c3c0-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="0c3c0-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0c3c0-105">Data type</span></span>

<span data-ttu-id="0c3c0-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c3c0-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0c3c0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c3c0-107">Remarks</span></span>

<span data-ttu-id="0c3c0-108">Standardmäßig verwendet die Aufzeichnungs-Engine Hardware Decoder oder Encoder.</span><span class="sxs-lookup"><span data-stu-id="0c3c0-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="0c3c0-109">Um die Verwendung von Hardware-MFTs zu deaktivieren, legen Sie dieses Attribut auf " **true** " fest, wenn Sie die Aufzeichnungs-Engine erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c3c0-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c3c0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c3c0-110">Requirements</span></span>



| <span data-ttu-id="0c3c0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c3c0-111">Requirement</span></span> | <span data-ttu-id="0c3c0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="0c3c0-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3c0-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0c3c0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3c0-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c3c0-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="0c3c0-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0c3c0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3c0-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0c3c0-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c3c0-117">Header</span><span class="sxs-lookup"><span data-stu-id="0c3c0-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c3c0-118"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c3c0-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c3c0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c3c0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3c0-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0c3c0-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c3c0-121">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="0c3c0-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c3c0-122">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="0c3c0-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




