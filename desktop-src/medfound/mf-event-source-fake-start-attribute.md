---
description: Gibt an, ob die aktuelle Segment Topologie leer ist.
ms.assetid: efd497dc-affc-4453-975c-09c5dca06374
title: MF_EVENT_SOURCE_FAKE_START-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae47bbfdedb7535ff46763ad5bc36f552ffe4780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869119"
---
# <a name="mf_event_source_fake_start-attribute"></a><span data-ttu-id="555e5-103">\_ \_ \_ Gefälschtes \_ Start Attribut der MF-Ereignis Quelle</span><span class="sxs-lookup"><span data-stu-id="555e5-103">MF\_EVENT\_SOURCE\_FAKE\_START attribute</span></span>

<span data-ttu-id="555e5-104">Gibt an, ob die aktuelle Segment Topologie leer ist.</span><span class="sxs-lookup"><span data-stu-id="555e5-104">Specifies whether the current segment topology is empty.</span></span>

## <a name="data-type"></a><span data-ttu-id="555e5-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="555e5-105">Data type</span></span>

<span data-ttu-id="555e5-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="555e5-106">**UINT32**</span></span>

<span data-ttu-id="555e5-107">Als booleschen Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="555e5-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="555e5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="555e5-108">Remarks</span></span>

<span data-ttu-id="555e5-109">Dieses Attribut wird mit dem [mesourcestarted](mesourcestarted.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="555e5-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="555e5-110">Die Sequencer-Quelle legt dieses Attribut auf **true** fest, wenn die aktuelle Segment Topologie leer ist.</span><span class="sxs-lookup"><span data-stu-id="555e5-110">The sequencer source sets this attribute to **TRUE** if the current segment topology is empty.</span></span> <span data-ttu-id="555e5-111">Wenn dieses Attribut **true** ist, wurde die Wiedergabe noch nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="555e5-111">If this attribute is **TRUE**, playback has not started yet.</span></span> <span data-ttu-id="555e5-112">Der Standardwert dieses Attributs ist **false**.</span><span class="sxs-lookup"><span data-stu-id="555e5-112">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="555e5-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="555e5-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="555e5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="555e5-114">Requirements</span></span>



| <span data-ttu-id="555e5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="555e5-115">Requirement</span></span> | <span data-ttu-id="555e5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="555e5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="555e5-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="555e5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="555e5-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="555e5-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="555e5-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="555e5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="555e5-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="555e5-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="555e5-121">Header</span><span class="sxs-lookup"><span data-stu-id="555e5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="555e5-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="555e5-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="555e5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="555e5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555e5-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="555e5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="555e5-125">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="555e5-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="555e5-126">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="555e5-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="555e5-127">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="555e5-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




