---
description: Enthält einen imffieldofusemftunlock-Zeiger, der zum Entsperren einer Media Foundation Transformation (MFT) verwendet werden kann. Die imffieldofusemftunlock-Schnittstelle wird verwendet, um ein MFT mit Einschränkungen für das Feld zu entsperren.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: MFT_FIELDOFUSE_UNLOCK_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755272"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="ba357-104">MFT \_ fieldofuse \_ Unlock \_ Attribute-Attribut</span><span class="sxs-lookup"><span data-stu-id="ba357-104">MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="ba357-105">Enthält einen [**imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) -Zeiger, der zum Entsperren einer Media Foundation Transformation (MFT) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba357-105">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which can be used to unlock a Media Foundation transform (MFT).</span></span> <span data-ttu-id="ba357-106">Die **imffieldofusemftunlock** -Schnittstelle wird verwendet, um ein MFT mit Einschränkungen für das Feld zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="ba357-106">The **IMFFieldOfUseMFTUnlock** interface is used to unlock an MFT that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba357-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ba357-107">Data type</span></span>

<span data-ttu-id="ba357-108">**[**Imffieldofusemftunlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) \** _ als " _*IUnknown \*\* " gespeichert_</span><span class="sxs-lookup"><span data-stu-id="ba357-108">**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="ba357-109">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="ba357-109">Get/set</span></span>

<span data-ttu-id="ba357-110">Um dieses Attribut abzurufen, nennen Sie [_ *imfattributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="ba357-110">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="ba357-111">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="ba357-111">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba357-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ba357-112">Remarks</span></span>

<span data-ttu-id="ba357-113">Weitere Informationen zu diesem Attribut finden Sie unter [Einschränkungen](field-of-use-restrictions.md)für das Feld "Verwendung".</span><span class="sxs-lookup"><span data-stu-id="ba357-113">For more information about this attribute, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

<span data-ttu-id="ba357-114">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="ba357-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba357-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ba357-115">Requirements</span></span>



| <span data-ttu-id="ba357-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ba357-116">Requirement</span></span> | <span data-ttu-id="ba357-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ba357-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba357-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ba357-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba357-119">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ba357-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ba357-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ba357-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba357-121">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="ba357-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ba357-122">Header</span><span class="sxs-lookup"><span data-stu-id="ba357-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba357-123"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="ba357-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba357-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba357-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba357-125">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="ba357-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba357-126">Einschränkungen bei der Verwendung des Felds</span><span class="sxs-lookup"><span data-stu-id="ba357-126">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="ba357-127">**MF | atetransformaktivierungs**</span><span class="sxs-lookup"><span data-stu-id="ba357-127">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




