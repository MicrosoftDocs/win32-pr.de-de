---
description: Gibt an, ob ein Flash für den aufgezeichneten Frame ausgelöst wurde.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349105"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a><span data-ttu-id="02430-103">"MF \_ Capture \_ Metadata \_ Photo \_ Frame \_ Flash Attribute"</span><span class="sxs-lookup"><span data-stu-id="02430-103">MF\_CAPTURE\_METADATA\_PHOTO\_FRAME\_FLASH attribute</span></span>

<span data-ttu-id="02430-104">Gibt an, ob ein Flash für den aufgezeichneten Frame ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="02430-104">Indicates if a flash was triggered for the captured frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="02430-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="02430-105">Data type</span></span>

<span data-ttu-id="02430-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="02430-106">**UINT32**</span></span>



| <span data-ttu-id="02430-107">Wert</span><span class="sxs-lookup"><span data-stu-id="02430-107">Value</span></span>                                                                               | <span data-ttu-id="02430-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="02430-108">Meaning</span></span>                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="02430-109"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02430-109"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="02430-110">Ein Flash wurde für diesen Frame nicht ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="02430-110">A flash was not triggered on this frame.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="02430-111"><dt>ungleich null</dt></span><span class="sxs-lookup"><span data-stu-id="02430-111"><dt>non-zero</dt></span></span> </dl> | <span data-ttu-id="02430-112">Ein Flash wurde für diesen Frame ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="02430-112">A flash was triggered on this frame.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="02430-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="02430-113"><dt>1</dt></span></span> </dl>        | <span data-ttu-id="02430-114">Reserviert</span><span class="sxs-lookup"><span data-stu-id="02430-114">Reserved</span></span><br/> <span data-ttu-id="02430-115">Überprüfen Sie nicht explizit den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="02430-115">Do not explicitly check for a value of 1.</span></span> <span data-ttu-id="02430-116">Anwendungen sollten nur nach! = 0 suchen, um anzugeben, ob ein Flash ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="02430-116">Applications should only check for !=0 to indicate if a flash was triggered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02430-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02430-117">Requirements</span></span>



| <span data-ttu-id="02430-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02430-118">Requirement</span></span> | <span data-ttu-id="02430-119">Wert</span><span class="sxs-lookup"><span data-stu-id="02430-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02430-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02430-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02430-121">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="02430-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="02430-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02430-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02430-123">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02430-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="02430-124">Header</span><span class="sxs-lookup"><span data-stu-id="02430-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02430-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="02430-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02430-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02430-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02430-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="02430-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




