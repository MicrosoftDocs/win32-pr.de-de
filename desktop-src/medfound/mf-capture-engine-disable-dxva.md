---
description: Gibt an, ob die Aufzeichnungs-Engine die DirectX-Videobeschleunigung (DXVA) zum Decodieren von Videos verwendet.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA-Attribut (MF. Engine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343938"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a><span data-ttu-id="7f4ad-103">\_ \_ \_ \_ DXVA-Attribut für MF-Erfassungs Modul deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7f4ad-103">MF\_CAPTURE\_ENGINE\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="7f4ad-104">Gibt an, ob die Aufzeichnungs-Engine die DirectX-Videobeschleunigung (DXVA) zum Decodieren von Videos verwendet.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-104">Specifies whether the capture engine uses DirectX Video Acceleration (DXVA) for video decoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f4ad-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7f4ad-105">Data type</span></span>

<span data-ttu-id="7f4ad-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7f4ad-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f4ad-107">Remarks</span></span>

<span data-ttu-id="7f4ad-108">Dieses Attribut gilt, wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="7f4ad-108">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="7f4ad-109">Die Aufzeichnungs-Engine decodiert einen komprimierten Videostream aus dem Erfassungsgerät (z. b. wenn das Erfassungsgerät H. 264-Video ausgibt).</span><span class="sxs-lookup"><span data-stu-id="7f4ad-109">The capture engine decodes a compressed video stream from the capture device (for example, if the capture device outputs H.264 video).</span></span>
-   <span data-ttu-id="7f4ad-110">Der Video Decoder unterstützt die hardwarebeschleunigte Decodierung mithilfe von DXVA.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-110">The video decoder supports hardware-accelerated decoding using DXVA.</span></span>
-   <span data-ttu-id="7f4ad-111">Die Anwendung verwendet das [ \_ \_ \_ D3D \_ Manager](mf-capture-engine-d3d-manager.md) -Attribut der MF-Erfassungs-Engine zum Festlegen der DXGI-Device Manager für die Aufzeichnungs-Engine.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-111">The application uses the [MF\_CAPTURE\_ENGINE\_D3D\_MANAGER](mf-capture-engine-d3d-manager.md) attribute to set the DXGI Device Manager on the capture engine.</span></span>

<span data-ttu-id="7f4ad-112">Andernfalls wird dieses Attribut ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-112">Otherwise, this attribute is ignored.</span></span>

<span data-ttu-id="7f4ad-113">Dieses Attribut ermöglicht es der Anwendung, DXVA zu deaktivieren, während die Decodierung an Direct3D-Oberflächen noch nicht</span><span class="sxs-lookup"><span data-stu-id="7f4ad-113">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="7f4ad-114">Der Standardwert dieses Attributs ist **false**. Dies bedeutet, dass die DXVA-Decodierung aktiviert ist, wenn verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f4ad-114">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f4ad-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f4ad-115">Requirements</span></span>



| <span data-ttu-id="7f4ad-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f4ad-116">Requirement</span></span> | <span data-ttu-id="7f4ad-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7f4ad-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4ad-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f4ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4ad-119">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f4ad-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="7f4ad-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f4ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4ad-121">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f4ad-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f4ad-122">Header</span><span class="sxs-lookup"><span data-stu-id="7f4ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4ad-123"><dt>"MF"-Engine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f4ad-123"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f4ad-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f4ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4ad-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="7f4ad-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f4ad-126">Attribute der Aufzeichnungs-Engine</span><span class="sxs-lookup"><span data-stu-id="7f4ad-126">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f4ad-127">**IMF captureengine:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="7f4ad-127">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




