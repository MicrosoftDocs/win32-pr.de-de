---
description: Gibt den Status einer Topologie während der Wiedergabe an.
ms.assetid: f7c93bad-1a64-45b0-ab5c-6edea4a1c0d1
title: MF_EVENT_TOPOLOGY_STATUS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee3c6e00722239103058ca584ee1da28778511c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352391"
---
# <a name="mf_event_topology_status-attribute"></a><span data-ttu-id="0ddb1-103">MF- \_ Ereignis \_ topologiestatusattribut \_</span><span class="sxs-lookup"><span data-stu-id="0ddb1-103">MF\_EVENT\_TOPOLOGY\_STATUS attribute</span></span>

<span data-ttu-id="0ddb1-104">Gibt den Status einer Topologie während der Wiedergabe an.</span><span class="sxs-lookup"><span data-stu-id="0ddb1-104">Specifies the status of a topology during playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="0ddb1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0ddb1-105">Data type</span></span>

<span data-ttu-id="0ddb1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0ddb1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0ddb1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ddb1-107">Remarks</span></span>

<span data-ttu-id="0ddb1-108">Der Wert dieses Attributs ist ein Member der [**MF \_ topostatus**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0ddb1-108">The value of this attribute is a member of the [**MF\_TOPOSTATUS**](/windows/desktop/api/mfapi/ne-mfapi-mf_topostatus) enumeration.</span></span>

<span data-ttu-id="0ddb1-109">Dieses Attribut wird mit dem [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ddb1-109">This attribute is used with the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

<span data-ttu-id="0ddb1-110">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="0ddb1-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddb1-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ddb1-111">Requirements</span></span>



| <span data-ttu-id="0ddb1-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ddb1-112">Requirement</span></span> | <span data-ttu-id="0ddb1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0ddb1-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ddb1-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0ddb1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddb1-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ddb1-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0ddb1-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0ddb1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddb1-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0ddb1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0ddb1-118">Header</span><span class="sxs-lookup"><span data-stu-id="0ddb1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddb1-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddb1-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddb1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ddb1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddb1-121">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="0ddb1-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ddb1-122">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="0ddb1-122">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="0ddb1-123">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0ddb1-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0ddb1-124">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="0ddb1-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




