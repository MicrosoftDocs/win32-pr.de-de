---
description: Gibt die Startzeit für eine Segment Topologie an.
ms.assetid: d8902fb6-c758-4d3d-9230-e918948bda19
title: MF_EVENT_SOURCE_PROJECTSTART-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 512e2129c3104d9e7160163f03a9c28b2716273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869116"
---
# <a name="mf_event_source_projectstart-attribute"></a><span data-ttu-id="db34c-103">Projekt der MF- \_ Ereignis \_ Quelle \_ ProjectStart-Attribut</span><span class="sxs-lookup"><span data-stu-id="db34c-103">MF\_EVENT\_SOURCE\_PROJECTSTART attribute</span></span>

<span data-ttu-id="db34c-104">Gibt die Startzeit für eine Segment Topologie an.</span><span class="sxs-lookup"><span data-stu-id="db34c-104">Specifies the start time for a segment topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="db34c-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="db34c-105">Data type</span></span>

<span data-ttu-id="db34c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="db34c-106">**UINT64**</span></span>

<span data-ttu-id="db34c-107">Als **Longlong** -Wert behandeln.</span><span class="sxs-lookup"><span data-stu-id="db34c-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="db34c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db34c-108">Remarks</span></span>

<span data-ttu-id="db34c-109">Dieses Attribut wird mit dem [mesourcestarted](mesourcestarted.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="db34c-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="db34c-110">Die Sequencer-Quelle legt dieses Attribut fest, wenn die aktuelle Segment Topologie das [**MF- \_ topologieprojectstart \_**](mf-topology-projectstart-attribute.md) -Attribut aufweist.</span><span class="sxs-lookup"><span data-stu-id="db34c-110">The sequencer source sets this attribute when the current segment topology has the [**MF\_TOPOLOGY\_PROJECTSTART**](mf-topology-projectstart-attribute.md) attribute.</span></span> <span data-ttu-id="db34c-111">Die beiden Attribute haben denselben Wert.</span><span class="sxs-lookup"><span data-stu-id="db34c-111">The two attributes have the same value.</span></span>

<span data-ttu-id="db34c-112">Dieses Attribut ist ein Wert mit Vorzeichen, obwohl er als **UINT64** gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="db34c-112">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="db34c-113">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="db34c-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="db34c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db34c-114">Requirements</span></span>



| <span data-ttu-id="db34c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db34c-115">Requirement</span></span> | <span data-ttu-id="db34c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="db34c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db34c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db34c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db34c-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db34c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db34c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db34c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db34c-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db34c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db34c-121">Header</span><span class="sxs-lookup"><span data-stu-id="db34c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="db34c-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="db34c-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db34c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db34c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db34c-124">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="db34c-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="db34c-125">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="db34c-125">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="db34c-126">**Imfattributes:: GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="db34c-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="db34c-127">**Imfattributes:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="db34c-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




