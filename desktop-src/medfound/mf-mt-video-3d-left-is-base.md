---
description: Gibt für ein 3D-Videoformat an, welche Sicht die Basis Ansicht ist.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363313"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="9eeab-103">MF \_ \_ -MT \_ -Video 3D \_ ist das \_ \_ Basis Attribut</span><span class="sxs-lookup"><span data-stu-id="9eeab-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="9eeab-104">Gibt für ein 3D-Videoformat an, welche Sicht die Basis Ansicht ist.</span><span class="sxs-lookup"><span data-stu-id="9eeab-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="9eeab-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9eeab-105">Data type</span></span>

<span data-ttu-id="9eeab-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9eeab-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9eeab-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eeab-107">Remarks</span></span>

<span data-ttu-id="9eeab-108">Standardmäßig ist die linke Ansicht in einer 3D-Videosequenz die Basis Ansicht.</span><span class="sxs-lookup"><span data-stu-id="9eeab-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="9eeab-109">Wenn die Rechte Ansicht die Basis Ansicht ist, legen Sie dieses Attribut auf " **false**" fest.</span><span class="sxs-lookup"><span data-stu-id="9eeab-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="9eeab-110">Um das Stereovideo in 2D zu konvertieren, behalten Sie die Basis Ansicht bei und verwerfen die andere Sicht.</span><span class="sxs-lookup"><span data-stu-id="9eeab-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eeab-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9eeab-111">Requirements</span></span>



| <span data-ttu-id="9eeab-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9eeab-112">Requirement</span></span> | <span data-ttu-id="9eeab-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9eeab-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9eeab-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9eeab-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9eeab-115">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9eeab-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="9eeab-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9eeab-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9eeab-117">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="9eeab-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="9eeab-118">Header</span><span class="sxs-lookup"><span data-stu-id="9eeab-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9eeab-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eeab-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eeab-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9eeab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eeab-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9eeab-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




