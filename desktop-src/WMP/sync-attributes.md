---
title: Synchronisierungs Attribute
description: Die Attribute Sync01 through Sync16 sind Zeichen folgen Darstellungen von 32-Bit-Werten, die von Windows Media Player beim Synchronisieren von Wiedergabelisten mit einem von bis zu 16 tragbaren Geräten verwendet werden.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Synchronisierungs Attribute (Windows Media Player)
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364607"
---
# <a name="sync-attributes"></a><span data-ttu-id="2a3a6-104">Synchronisierungs Attribute</span><span class="sxs-lookup"><span data-stu-id="2a3a6-104">Sync Attributes</span></span>

<span data-ttu-id="2a3a6-105">Die Attribute **Sync01** through **Sync16** sind Zeichen folgen Darstellungen von 32-Bit-Werten, die von Windows Media Player beim Synchronisieren von Wiedergabelisten mit einem von bis zu 16 tragbaren Geräten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="2a3a6-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="2a3a6-106">Applies To</span></span>

-   [<span data-ttu-id="2a3a6-107">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="2a3a6-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="2a3a6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a3a6-108">Remarks</span></span>

<span data-ttu-id="2a3a6-109">Diese Attribute sind Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-109">These are read/write attributes.</span></span> <span data-ttu-id="2a3a6-110">Der Wert 0 (null) gibt an, dass Windows Media Player die Wiedergabeliste nicht mit dem zugeordneten Gerät synchronisieren soll.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="2a3a6-111">Ein Wert größer als 0 (null) gibt eine Synchronisierungs Priorität für die angegebene Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="2a3a6-112">Basierend auf der Benutzereingabe legt Windows Media Player dieses Attribut für jede der Wiedergabelisten in der Bibliothek fest.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="2a3a6-113">Wenn Windows Media Player versucht, eine Wiedergabeliste mit einem tragbaren Gerät zu synchronisieren, wird jede Wiedergabeliste überprüft, um die Werte für die **Sync**_xx_ -Attribute zu vergleichen, die die Geräte Partnerschaft darstellen.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="2a3a6-114">Wiedergabelisten, die niedrigere **Sync**_xx_ -Werte aufweisen, erhalten eine höhere Synchronisierungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="2a3a6-115">Die Bibliothek kann z. b. die folgenden vier Wiedergabelisten und die entsprechenden **Sync**_xx_ -Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="2a3a6-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="2a3a6-116">Wiedergabelisten Name</span><span class="sxs-lookup"><span data-stu-id="2a3a6-116">Playlist Name</span></span> | <span data-ttu-id="2a3a6-117">Sync01-Wert</span><span class="sxs-lookup"><span data-stu-id="2a3a6-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="2a3a6-118">"Gymmusic. wpl"</span><span class="sxs-lookup"><span data-stu-id="2a3a6-118">GymMusic.WPL</span></span>  | <span data-ttu-id="2a3a6-119">0x0000000d</span><span class="sxs-lookup"><span data-stu-id="2a3a6-119">0x0000000D</span></span>   |
| <span data-ttu-id="2a3a6-120">"Relax. wpl"</span><span class="sxs-lookup"><span data-stu-id="2a3a6-120">Relax.WPL</span></span>     | <span data-ttu-id="2a3a6-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2a3a6-121">0x00000020</span></span>   |
| <span data-ttu-id="2a3a6-122">Drivehome. wpl</span><span class="sxs-lookup"><span data-stu-id="2a3a6-122">DriveHome.WPL</span></span> | <span data-ttu-id="2a3a6-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2a3a6-123">0x00000001</span></span>   |
| <span data-ttu-id="2a3a6-124">Nogo. wpl</span><span class="sxs-lookup"><span data-stu-id="2a3a6-124">NoGo.WPL</span></span>      | <span data-ttu-id="2a3a6-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2a3a6-125">0x00000000</span></span>   |



 

<span data-ttu-id="2a3a6-126">Wenn Windows Media Player das dem-Attribut zugeordnete Gerät synchronisiert, werden die Wiedergabelisten in der folgenden Reihenfolge synchronisiert:</span><span class="sxs-lookup"><span data-stu-id="2a3a6-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="2a3a6-127">Drivehome. wpl</span><span class="sxs-lookup"><span data-stu-id="2a3a6-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="2a3a6-128">"Gymmusic. wpl"</span><span class="sxs-lookup"><span data-stu-id="2a3a6-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="2a3a6-129">"Relax. wpl"</span><span class="sxs-lookup"><span data-stu-id="2a3a6-129">Relax.WPL</span></span>

<span data-ttu-id="2a3a6-130">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2a3a6-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3a6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a3a6-131">Requirements</span></span>



| <span data-ttu-id="2a3a6-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a3a6-132">Requirement</span></span> | <span data-ttu-id="2a3a6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="2a3a6-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="2a3a6-134">Version</span><span class="sxs-lookup"><span data-stu-id="2a3a6-134">Version</span></span><br/> | <span data-ttu-id="2a3a6-135">Windows Media Player 10 oder höher</span><span class="sxs-lookup"><span data-stu-id="2a3a6-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a3a6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a3a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3a6-137">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="2a3a6-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="2a3a6-138">**Auflisten von Synchronisierungs Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="2a3a6-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





