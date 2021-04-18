---
description: Gibt die früheren Merkmale der Medienquelle an.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: MF_EVENT_SOURCE_CHARACTERISTICS_OLD-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347880"
---
# <a name="mf_event_source_characteristics_old-attribute"></a><span data-ttu-id="d89b0-103">Eigenschaften der MF- \_ Ereignis \_ Quelle \_ \_ Altes Attribut</span><span class="sxs-lookup"><span data-stu-id="d89b0-103">MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD attribute</span></span>

<span data-ttu-id="d89b0-104">Gibt die früheren Merkmale der Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="d89b0-104">Specifies the previous characteristics of the media source.</span></span> <span data-ttu-id="d89b0-105">Bei den Attributdaten handelt es sich um ein bitweises **or** von-Flags aus der [**mfmediasource- \_ Eigenschaften**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d89b0-105">The attribute data is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="data-type"></a><span data-ttu-id="d89b0-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d89b0-106">Data type</span></span>

<span data-ttu-id="d89b0-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d89b0-107">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d89b0-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d89b0-108">Remarks</span></span>

<span data-ttu-id="d89b0-109">Dieses Attribut wird mit dem [mesourcecharakteristicschangi-Ereignis](mesourcecharacteristicschanged.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d89b0-109">This attribute is used with the [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) event.</span></span>

<span data-ttu-id="d89b0-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="d89b0-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d89b0-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d89b0-111">Requirements</span></span>



| <span data-ttu-id="d89b0-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d89b0-112">Requirement</span></span> | <span data-ttu-id="d89b0-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d89b0-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d89b0-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d89b0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d89b0-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d89b0-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d89b0-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d89b0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d89b0-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d89b0-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d89b0-118">Header</span><span class="sxs-lookup"><span data-stu-id="d89b0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d89b0-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89b0-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89b0-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d89b0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89b0-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="d89b0-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d89b0-122">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="d89b0-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="d89b0-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d89b0-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d89b0-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d89b0-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d89b0-125">**Imfmediasource**</span><span class="sxs-lookup"><span data-stu-id="d89b0-125">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




