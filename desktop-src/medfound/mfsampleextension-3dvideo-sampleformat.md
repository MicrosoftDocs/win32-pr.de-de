---
description: Gibt an, wie ein 3D-Videoframe in einem Medien Beispiel gespeichert wird.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131128"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a><span data-ttu-id="435b2-103">MF Sample Extension \_ 3dvideo \_ Sampleformat-Attribut</span><span class="sxs-lookup"><span data-stu-id="435b2-103">MFSampleExtension\_3DVideo\_SampleFormat attribute</span></span>

<span data-ttu-id="435b2-104">Gibt an, wie ein 3D-Videoframe in einem Medien Beispiel gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="435b2-104">Specifies how a 3D video frame is stored in a media sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="435b2-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="435b2-105">Data type</span></span>

<span data-ttu-id="435b2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="435b2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="435b2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="435b2-107">Remarks</span></span>

<span data-ttu-id="435b2-108">Der Wert dieses Attributs ist ein Member der [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="435b2-108">The value of this attribute is a member of the [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) enumeration.</span></span>

<span data-ttu-id="435b2-109">Eine Komponente, die 3D-Video Frames generiert, sollte dieses Attribut für jedes Medien Beispiel, das einen 3D-Frame enthält, auf " **true** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="435b2-109">A component that generates 3D video frames should set this attribute to **TRUE** on every media sample that contains a 3D frame.</span></span> <span data-ttu-id="435b2-110">Das Attribut wird ignoriert, wenn das Attribut " [MF Sample Extension \_ 3dvideo](mfsampleextension-3dvideo.md) " den Wert " **false** " hat oder nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="435b2-110">The attribute is ignored if the [MFSampleExtension\_3DVideo](mfsampleextension-3dvideo.md) attribute is **FALSE** or not set.</span></span>

## <a name="requirements"></a><span data-ttu-id="435b2-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="435b2-111">Requirements</span></span>



| <span data-ttu-id="435b2-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="435b2-112">Requirement</span></span> | <span data-ttu-id="435b2-113">Wert</span><span class="sxs-lookup"><span data-stu-id="435b2-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="435b2-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="435b2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="435b2-115">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="435b2-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="435b2-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="435b2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="435b2-117">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="435b2-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="435b2-118">Header</span><span class="sxs-lookup"><span data-stu-id="435b2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="435b2-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="435b2-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="435b2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="435b2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435b2-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="435b2-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="435b2-122">MF Sample Extension \_ 3dvideo</span><span class="sxs-lookup"><span data-stu-id="435b2-122">MFSampleExtension\_3DVideo</span></span>](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




