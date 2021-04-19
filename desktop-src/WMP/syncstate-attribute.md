---
title: SyncState-Attribut
description: Das SyncState-Attribut ist eine Zeichen folgen Darstellung eines 32-Bit-Werts, der von Windows Media Player beim Synchronisieren von Wiedergabelisten mit tragbaren Geräten verwendet wird.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- SyncState-Attribut (Windows Media Player)
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373650"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="8066d-104">SyncState-Attribut</span><span class="sxs-lookup"><span data-stu-id="8066d-104">SyncState Attribute</span></span>

<span data-ttu-id="8066d-105">Das **SyncState** -Attribut ist eine Zeichen folgen Darstellung eines 32-Bit-Werts, der von Windows Media Player beim Synchronisieren von Wiedergabelisten mit tragbaren Geräten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8066d-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="8066d-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="8066d-106">Applies To</span></span>

-   [<span data-ttu-id="8066d-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="8066d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="8066d-108">Andere Elemente</span><span class="sxs-lookup"><span data-stu-id="8066d-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="8066d-109">Foto Elemente</span><span class="sxs-lookup"><span data-stu-id="8066d-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="8066d-110">Video Elemente</span><span class="sxs-lookup"><span data-stu-id="8066d-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="8066d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8066d-111">Remarks</span></span>

<span data-ttu-id="8066d-112">Dieses Attribut besteht aus 16 2-Bit-Werten, von denen jeder den Synchronisierungs Status eines tragbaren Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="8066d-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="8066d-113">Das signifikanteste Bit (MSB) dieses 32-Bit-Werts entspricht Gerät 16.</span><span class="sxs-lookup"><span data-stu-id="8066d-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="8066d-114">Das unwichtigste Bit (LSB) entspricht Gerät 1.</span><span class="sxs-lookup"><span data-stu-id="8066d-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="8066d-115">Der MSB-Wert jedes 2-Bit-Werts gibt an, ob Windows den Inhalt mit dem entsprechenden Gerät synchronisiert Media Player.</span><span class="sxs-lookup"><span data-stu-id="8066d-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="8066d-116">Der Wert 1 gibt an, dass dies geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="8066d-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="8066d-117">Der Wert 0 gibt an, dass dies nicht der Fall war.</span><span class="sxs-lookup"><span data-stu-id="8066d-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="8066d-118">Wenn MSB den Wert 0 hat, gibt der LSB an, warum die Synchronisierung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8066d-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="8066d-119">Der Wert 1 in der LSB gibt an, dass nicht genügend freier Speicherplatz für den Inhalt vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="8066d-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="8066d-120">Der Wert 0 in der LSB gibt an, dass eine Synchronisierung durch einen anderen Grund verhindert wurde.</span><span class="sxs-lookup"><span data-stu-id="8066d-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="8066d-121">Gehen Sie folgendermaßen vor, um den Synchronisierungs Status eines bestimmten Geräts abzurufen:</span><span class="sxs-lookup"><span data-stu-id="8066d-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="8066d-122">Rufen Sie **iwmpsyncdevice:: get \_ Status** auf, um zu bestimmen, ob ein bestimmtes Gerät synchronisiert ist.</span><span class="sxs-lookup"><span data-stu-id="8066d-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="8066d-123">Wenn Sie synchronisiert ist, rufen Sie **iwmpsyncdevice:: get \_ partnershipindex** auf, um den Index des bitpaars des Geräts im **SyncState** -Attribut abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8066d-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="8066d-124">Maskieren Sie mit diesem Index das entsprechende bitpaar des **SyncState** -Attributs, und untersuchen Sie das Ergebnis, um den Synchronisierungs Status der Wiedergabeliste mit dem Gerät zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8066d-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="8066d-125">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8066d-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8066d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8066d-126">Requirements</span></span>



| <span data-ttu-id="8066d-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8066d-127">Requirement</span></span> | <span data-ttu-id="8066d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8066d-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="8066d-129">Version</span><span class="sxs-lookup"><span data-stu-id="8066d-129">Version</span></span><br/> | <span data-ttu-id="8066d-130">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="8066d-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8066d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8066d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8066d-132">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="8066d-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="8066d-133">**Status der Wiedergabelisten Synchronisierung**</span><span class="sxs-lookup"><span data-stu-id="8066d-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="8066d-134">**Iwmpsyncdevice:: get \_ Partner shipindex**</span><span class="sxs-lookup"><span data-stu-id="8066d-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="8066d-135">**Iwmpsyncdevice:: get- \_ Status**</span><span class="sxs-lookup"><span data-stu-id="8066d-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





