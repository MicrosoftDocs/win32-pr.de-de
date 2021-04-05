---
description: Gibt an, wie viele Puffer der Video-Sample-Zuweisung für jedes Video Beispiel erstellt.
ms.assetid: A782BF8A-822A-407D-A30A-F2045BBB0BC0
title: MF_SA_BUFFERS_PER_SAMPLE-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d658ae72c53d986b364b2b6a3f405ae0052ea3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753176"
---
# <a name="mf_sa_buffers_per_sample-attribute"></a><span data-ttu-id="6f49e-103">MF- \_ sa- \_ Puffer \_ pro Sample- \_ Attribut</span><span class="sxs-lookup"><span data-stu-id="6f49e-103">MF\_SA\_BUFFERS\_PER\_SAMPLE attribute</span></span>

<span data-ttu-id="6f49e-104">Gibt an, wie viele Puffer der Video-Sample-Zuweisung für jedes Video Beispiel erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f49e-104">Specifies how many buffers the video-sample allocator creates for each video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="6f49e-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6f49e-105">Data type</span></span>

<span data-ttu-id="6f49e-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6f49e-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6f49e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f49e-107">Remarks</span></span>

<span data-ttu-id="6f49e-108">Wenn Sie Videobeispiele mit der [**imfvideosamplealloerorex**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) -Schnittstelle zuordnen, können Sie mit diesem Attribut Videobeispiele erstellen, die mehrere Puffer enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f49e-108">If you use the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate video samples, you can use this attribute to create video samples that contain multiple buffers.</span></span> <span data-ttu-id="6f49e-109">Wenn der-Attribut Wert z. b. 2 ist, erstellt die Zuweisung zwei Video Puffer für jedes Video Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6f49e-109">For example, if the attribute value is 2, the allocator creates two video buffers for each video sample.</span></span> <span data-ttu-id="6f49e-110">Legen Sie das-Attribut im *pattributes* -Parameter der [**IMF videosamplezuzuweisung:: initializesamplezuweisung**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="6f49e-110">Set the attribute in the *pAttributes* parameter of the [**IMFVideoSampleAllocatorEx::InitializeSampleAllocatorEx**](/windows/desktop/api/mfidl/nf-mfidl-imfvideosampleallocatorex-initializesampleallocatorex) method.</span></span>

<span data-ttu-id="6f49e-111">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="6f49e-111">The default value is 1.</span></span> <span data-ttu-id="6f49e-112">Wenn das-Attribut nicht festgelegt ist, erstellt die Zuweisung Videobeispiele, die einen einzelnen Puffer pro Stichprobe enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f49e-112">If the attribute is not set, the allocator creates video samples that contain a single buffer per sample.</span></span>

<span data-ttu-id="6f49e-113">Dieses Attribut ist in der folgenden Situation primär für Media Foundation Transformationen (MFTs) vorgesehen, die eine Stereo-3D-Ausgabe unterstützen:</span><span class="sxs-lookup"><span data-stu-id="6f49e-113">This attribute is primarily intended for Media Foundation transforms (MFTs) that support stereo 3D output, in the following situation:</span></span>

-   <span data-ttu-id="6f49e-114">Der MFT unterstützt die Microsoft DirectX Graphics Infrastructure (DXGI).</span><span class="sxs-lookup"><span data-stu-id="6f49e-114">The MFT supports Microsoft DirectX Graphics Infrastructure (DXGI).</span></span>
-   <span data-ttu-id="6f49e-115">Der MFT weist seine eigenen Ausgabe Beispiele zu.</span><span class="sxs-lookup"><span data-stu-id="6f49e-115">The MFT allocates its own output samples.</span></span>
-   <span data-ttu-id="6f49e-116">Die MFT verwendet die [**imfvideosamplealloerorex**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) -Schnittstelle, um die Ausgabe Beispiele zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="6f49e-116">The MFT uses the [**IMFVideoSampleAllocatorEx**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex) interface to allocate the output samples.</span></span>
-   <span data-ttu-id="6f49e-117">Das 3D-Videoformat verwendet für jede Ansicht einen separaten Puffer.</span><span class="sxs-lookup"><span data-stu-id="6f49e-117">The 3D video format uses a separate buffer for each view.</span></span>

<span data-ttu-id="6f49e-118">Wenn alle diese Kriterien zutreffen, sollte der MFT den Attribut Wert auf 2 festlegen (ein Puffer pro Ansicht).</span><span class="sxs-lookup"><span data-stu-id="6f49e-118">If all of these criteria are true, the MFT should set the attribute value to 2 (one buffer per view).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f49e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f49e-119">Requirements</span></span>



| <span data-ttu-id="6f49e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f49e-120">Requirement</span></span> | <span data-ttu-id="6f49e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6f49e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f49e-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f49e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6f49e-123">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6f49e-123">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6f49e-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f49e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6f49e-125">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6f49e-125">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="6f49e-126">Header</span><span class="sxs-lookup"><span data-stu-id="6f49e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f49e-127"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="6f49e-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f49e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f49e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f49e-129">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6f49e-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




