---
description: Gibt an, ob ein Medien Beispiel einen 3D-Videoframe enthält.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: MFSampleExtension_3DVideo-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e30ea247f6f12f05414df0ae4305ecaaa6e3e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355570"
---
# <a name="mfsampleextension_3dvideo-attribute"></a><span data-ttu-id="4e547-103">MF Sample Extension \_ 3dvideo-Attribut</span><span class="sxs-lookup"><span data-stu-id="4e547-103">MFSampleExtension\_3DVideo attribute</span></span>

<span data-ttu-id="4e547-104">Gibt an, ob ein Medien Beispiel einen 3D-Videoframe enthält.</span><span class="sxs-lookup"><span data-stu-id="4e547-104">Specifies whether a media sample contains a 3D video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="4e547-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="4e547-105">Data type</span></span>

<span data-ttu-id="4e547-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e547-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4e547-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e547-107">Remarks</span></span>

<span data-ttu-id="4e547-108">Wenn dieses Attribut " **true**" ist, enthält das Beispiel "Media" einen Videorahmen mit mindestens zwei stereoskopischen Ansichten.</span><span class="sxs-lookup"><span data-stu-id="4e547-108">If this attribute is **TRUE**, the media sample contains a video frame that has two or more stereoscopic views.</span></span> <span data-ttu-id="4e547-109">Der Standardwert ist **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4e547-109">The default value is **FALSE**.</span></span>

<span data-ttu-id="4e547-110">Eine Komponente, die 3D-Video Frames generiert, sollte dieses Attribut für jedes Medien Beispiel, das einen 3D-Frame enthält, auf " **true** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="4e547-110">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e547-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e547-111">Requirements</span></span>



| <span data-ttu-id="4e547-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e547-112">Requirement</span></span> | <span data-ttu-id="4e547-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4e547-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4e547-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4e547-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4e547-115">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4e547-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="4e547-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4e547-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4e547-117">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4e547-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4e547-118">Header</span><span class="sxs-lookup"><span data-stu-id="4e547-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e547-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e547-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e547-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e547-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e547-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="4e547-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e547-122">MF Sample Extension \_ 3dvideo \_ Sample Format</span><span class="sxs-lookup"><span data-stu-id="4e547-122">MFSampleExtension\_3DVideo\_SampleFormat</span></span>](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




