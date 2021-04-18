---
description: Enthält Flags, die die Funktionen der Medien Sitzung basierend auf der aktuellen Präsentation definieren.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: MF_EVENT_SESSIONCAPS-Attribut (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347879"
---
# <a name="mf_event_sessioncaps-attribute"></a><span data-ttu-id="9fd75-103">MF- \_ Ereignis \_ sessioncaps-Attribut</span><span class="sxs-lookup"><span data-stu-id="9fd75-103">MF\_EVENT\_SESSIONCAPS attribute</span></span>

<span data-ttu-id="9fd75-104">Enthält Flags, die die Funktionen der Medien Sitzung basierend auf der aktuellen Präsentation definieren.</span><span class="sxs-lookup"><span data-stu-id="9fd75-104">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="9fd75-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="9fd75-105">Data type</span></span>

<span data-ttu-id="9fd75-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9fd75-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9fd75-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fd75-107">Remarks</span></span>

<span data-ttu-id="9fd75-108">Dieses Attribut enthält ein bitweises **or** von 0 (null) oder mehr Flags.</span><span class="sxs-lookup"><span data-stu-id="9fd75-108">This attribute contains a bitwise **OR** of zero or more flags.</span></span> <span data-ttu-id="9fd75-109">Eine Liste möglicher Flags finden Sie unter [**imfmediasession:: gezession-Funktionen**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="9fd75-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span>

<span data-ttu-id="9fd75-110">Dieses Attribut wird mit dem [mesessioncapabilitieschge](mesessioncapabilitieschanged.md) -Ereignis verwendet.</span><span class="sxs-lookup"><span data-stu-id="9fd75-110">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="9fd75-111">Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.</span><span class="sxs-lookup"><span data-stu-id="9fd75-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fd75-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fd75-112">Requirements</span></span>



| <span data-ttu-id="9fd75-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fd75-113">Requirement</span></span> | <span data-ttu-id="9fd75-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9fd75-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd75-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fd75-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9fd75-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fd75-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9fd75-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fd75-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9fd75-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9fd75-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9fd75-119">Header</span><span class="sxs-lookup"><span data-stu-id="9fd75-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fd75-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd75-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd75-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fd75-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd75-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="9fd75-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9fd75-123">Ereignisattribute</span><span class="sxs-lookup"><span data-stu-id="9fd75-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="9fd75-124">**Imfattributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9fd75-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="9fd75-125">**Imfattributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="9fd75-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




