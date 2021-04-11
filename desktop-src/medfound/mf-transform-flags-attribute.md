---
description: Enthält Flags für ein Media Foundation Transform-Aktivierungs Objekt (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: MF_TRANSFORM_FLAGS_Attribute-Attribut (MF Transform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959144"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="b3c96-103">MF \_ - \_ Attribut Attribut für Transformations Flags \_</span><span class="sxs-lookup"><span data-stu-id="b3c96-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="b3c96-104">Enthält Flags für ein Media Foundation Transform-Aktivierungs Objekt (MFT).</span><span class="sxs-lookup"><span data-stu-id="b3c96-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3c96-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b3c96-105">Data type</span></span>

<span data-ttu-id="b3c96-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b3c96-106">**UINT32**</span></span>

<span data-ttu-id="b3c96-107">Der Wert ist ein bitweises **or** -Flag aus der Enumeration des [**\_ MFT \_ \_**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) -Enumerationsflags.</span><span class="sxs-lookup"><span data-stu-id="b3c96-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="b3c96-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="b3c96-108">Get/set</span></span>

<span data-ttu-id="b3c96-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b3c96-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b3c96-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b3c96-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c96-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3c96-111">Remarks</span></span>

<span data-ttu-id="b3c96-112">Dieses Attribut wird für die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festgelegt, die von der [**motenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b3c96-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="b3c96-113">Das-Attribut enthält Flags, die die MFT beschreiben.</span><span class="sxs-lookup"><span data-stu-id="b3c96-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c96-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3c96-114">Requirements</span></span>



| <span data-ttu-id="b3c96-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3c96-115">Requirement</span></span> | <span data-ttu-id="b3c96-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b3c96-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c96-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3c96-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c96-118">Windows 7 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b3c96-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b3c96-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3c96-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c96-120">Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="b3c96-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b3c96-121">Header</span><span class="sxs-lookup"><span data-stu-id="b3c96-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c96-122"><dt>"MF Transform. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b3c96-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c96-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3c96-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c96-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="b3c96-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3c96-125">Transformations Attribute</span><span class="sxs-lookup"><span data-stu-id="b3c96-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
