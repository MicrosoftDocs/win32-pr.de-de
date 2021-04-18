---
description: Gibt an, ob eine Media Foundation Transformation (MFT) 3D-stereografievideo unterstützt.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: MFT_SUPPORT_3DVIDEO-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357431"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="1edf1-103">MFT \_ -Unterstützung \_ 3dvideo-Attribut</span><span class="sxs-lookup"><span data-stu-id="1edf1-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="1edf1-104">Gibt an, ob eine Media Foundation Transformation (MFT) 3D-stereografievideo unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1edf1-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="1edf1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1edf1-105">Data type</span></span>

<span data-ttu-id="1edf1-106">**Bool** gespeichert als **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1edf1-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1edf1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1edf1-107">Remarks</span></span>

<span data-ttu-id="1edf1-108">Um dieses Attribut abzufragen, müssen Sie [**imftransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) aufrufen, um den globalen Attribut Speicher des MFT abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1edf1-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="1edf1-109">Wenn **GetAttributes** erfolgreich ist, können Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1edf1-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1edf1-110">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="1edf1-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="1edf1-111">Behandeln Sie dieses Attribut als schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1edf1-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="1edf1-112">Ändern Sie den Wert nicht. die MFT ignoriert alle Änderungen am Wert.</span><span class="sxs-lookup"><span data-stu-id="1edf1-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1edf1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1edf1-113">Requirements</span></span>



| <span data-ttu-id="1edf1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1edf1-114">Requirement</span></span> | <span data-ttu-id="1edf1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1edf1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1edf1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1edf1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1edf1-117">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1edf1-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1edf1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1edf1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1edf1-119">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="1edf1-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="1edf1-120">Header</span><span class="sxs-lookup"><span data-stu-id="1edf1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1edf1-121"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1edf1-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1edf1-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1edf1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edf1-123">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="1edf1-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




