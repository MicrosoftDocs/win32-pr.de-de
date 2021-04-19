---
description: Gibt die aktuellen Merkmale der Medienquelle an.
ms.assetid: af2a2b75-cd4e-453c-876e-3be2db695e4e
title: MF_EVENT_SOURCE_CHARACTERISTICS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c775c0d3471d3d3442e565879ba8b42e07a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350481"
---
# <a name="mf_event_source_characteristics-attribute"></a><span data-ttu-id="bd354-103">Attribut "MF- \_ Ereignis \_ Quell \_ Merkmale"</span><span class="sxs-lookup"><span data-stu-id="bd354-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="bd354-104">Gibt die aktuellen Merkmale der Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="bd354-104">Specifies the current characteristics of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="bd354-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bd354-105">Data type</span></span>

<span data-ttu-id="bd354-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bd354-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bd354-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd354-107">Remarks</span></span>

<span data-ttu-id="bd354-108">Der Wert dieses Attributs ist ein bitweises **or** von Flags aus der [**mfmediasource- \_**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) eigenschaftenumeration.</span><span class="sxs-lookup"><span data-stu-id="bd354-108">The value of this attribute is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

<span data-ttu-id="bd354-109">Dieses Attribut wird mit dem [mesourcecharakteristicschangi-Ereignis](mesourcecharacteristicschanged.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd354-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="bd354-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="bd354-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd354-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd354-111">Requirements</span></span>



| <span data-ttu-id="bd354-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bd354-112">Requirement</span></span> | <span data-ttu-id="bd354-113">Wert</span><span class="sxs-lookup"><span data-stu-id="bd354-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bd354-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bd354-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bd354-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd354-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd354-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bd354-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bd354-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bd354-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bd354-118">Header</span><span class="sxs-lookup"><span data-stu-id="bd354-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd354-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd354-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd354-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd354-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd354-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="bd354-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd354-122">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="bd354-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="bd354-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bd354-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bd354-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bd354-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




