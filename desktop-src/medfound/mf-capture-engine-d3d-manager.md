---
description: Legt einen Zeiger auf den DXGI-Device Manager für die Aufzeichnungs-Engine fest.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: MF_CAPTURE_ENGINE_D3D_MANAGER-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129800"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a><span data-ttu-id="5bace-103">MF- \_ Erfassungs Modul \_ \_ D3D \_ Manager-Attribut</span><span class="sxs-lookup"><span data-stu-id="5bace-103">MF\_CAPTURE\_ENGINE\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="5bace-104">Legt einen Zeiger auf den DXGI-Device Manager für die Aufzeichnungs-Engine fest.</span><span class="sxs-lookup"><span data-stu-id="5bace-104">Sets a pointer to the DXGI Device Manager on the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="5bace-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5bace-105">Data type</span></span>

<span data-ttu-id="5bace-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="5bace-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="5bace-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bace-107">Remarks</span></span>

<span data-ttu-id="5bace-108">Der Wert dieses Attributs ist ein Zeiger auf die [_ *imfdxgidebug Manager* \*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5bace-108">The value of this attribute is a pointer to the [_ *IMFDXGIDeviceManager*\*](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface.</span></span> <span data-ttu-id="5bace-109">Mit diesem Attribut kann die Aufzeichnungs-Engine Video Frames mithilfe von DXGI-Oberflächen zuordnen und Hardwarebeschleunigung für Decodierung und Videoverarbeitung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5bace-109">This attribute enables the capture engine to allocate video frames using DXGI surfaces, and to use hardware acceleration for decoding and video processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bace-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bace-110">Requirements</span></span>



| <span data-ttu-id="5bace-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bace-111">Requirement</span></span> | <span data-ttu-id="5bace-112">Wert</span><span class="sxs-lookup"><span data-stu-id="5bace-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bace-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5bace-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5bace-114">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bace-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="5bace-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5bace-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5bace-116">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5bace-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5bace-117">Header</span><span class="sxs-lookup"><span data-stu-id="5bace-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bace-118"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bace-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bace-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bace-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bace-120">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="5bace-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5bace-121">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="5bace-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="5bace-122">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="5bace-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




