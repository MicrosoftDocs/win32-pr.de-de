---
description: Der Medienstrom verwendet dieses Ereignis, um Schutzsystem spezifische Metadaten an den Decoder zu senden.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Mecontentschutzmetadata-Ereignis (mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863179"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="33eb3-103">Mecontentschutzmetadata-Ereignis</span><span class="sxs-lookup"><span data-stu-id="33eb3-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="33eb3-104">Der Medienstrom verwendet dieses Ereignis, um Schutzsystem spezifische Metadaten an den Decoder zu senden.</span><span class="sxs-lookup"><span data-stu-id="33eb3-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="33eb3-105">Ereigniswerte</span><span class="sxs-lookup"><span data-stu-id="33eb3-105">Event values</span></span>

<span data-ttu-id="33eb3-106">Mögliche Werte, die von [**imfmediaevent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) abgerufen werden, sind folgende.</span><span class="sxs-lookup"><span data-stu-id="33eb3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="33eb3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="33eb3-107">VARTYPE</span></span>              | <span data-ttu-id="33eb3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33eb3-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="33eb3-109">VT \_ leer</span><span class="sxs-lookup"><span data-stu-id="33eb3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="33eb3-110">Keine Ereignisdaten.</span><span class="sxs-lookup"><span data-stu-id="33eb3-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="33eb3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="33eb3-111">Attributes</span></span>

<span data-ttu-id="33eb3-112">Für dieses Ereignis sind die folgenden Attribute definiert:</span><span class="sxs-lookup"><span data-stu-id="33eb3-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="33eb3-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="33eb3-113">Attribute</span></span>                                                                                              | <span data-ttu-id="33eb3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33eb3-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33eb3-115">\_ \_ \_ \_ Schlüsseldaten für den MF-Ereignisdaten Strom</span><span class="sxs-lookup"><span data-stu-id="33eb3-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="33eb3-116">Dies ist ein optionales Attribut.</span><span class="sxs-lookup"><span data-stu-id="33eb3-116">This is an optional attribute.</span></span> <span data-ttu-id="33eb3-117">Spezifische Daten des Schutzsystems.</span><span class="sxs-lookup"><span data-stu-id="33eb3-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="33eb3-118">Daten \_ \_ Strom- \_ Schlüssel \_ - \_ IDs des MF-Ereignisdaten Stroms</span><span class="sxs-lookup"><span data-stu-id="33eb3-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="33eb3-119">Inhalts Schlüssel-IDs, denen das Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="33eb3-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="33eb3-120">MF- \_ Ereignisdaten \_ Strom Metadaten-System \_ \_ Mid</span><span class="sxs-lookup"><span data-stu-id="33eb3-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="33eb3-121">Dies ist ein optionales Attribut.</span><span class="sxs-lookup"><span data-stu-id="33eb3-121">This is an optional attribute.</span></span> <span data-ttu-id="33eb3-122">Die System-ID, für die die Schlüsseldaten vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="33eb3-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="33eb3-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33eb3-123">Remarks</span></span>

<span data-ttu-id="33eb3-124">Dieses Ereignis wird z. b. zum kommunizieren eines Schlüssel Rotations Ereignisses verwendet.</span><span class="sxs-lookup"><span data-stu-id="33eb3-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="33eb3-125">In diesem Fall sollte Sie so früh wie möglich gesendet werden, um dem Decoder Zeit zu geben, sich selbst vorzubereiten, bevor mit der neuen Schlüssel-ID verschlüsselte Beispiele gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="33eb3-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="33eb3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33eb3-126">Requirements</span></span>



| <span data-ttu-id="33eb3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33eb3-127">Requirement</span></span> | <span data-ttu-id="33eb3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="33eb3-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33eb3-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33eb3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="33eb3-130">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="33eb3-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="33eb3-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33eb3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="33eb3-132">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="33eb3-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="33eb3-133">Header</span><span class="sxs-lookup"><span data-stu-id="33eb3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="33eb3-134"><dt>Mfobjects. h (Include mfdl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33eb3-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33eb3-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33eb3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33eb3-136">Ereignisse Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33eb3-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




