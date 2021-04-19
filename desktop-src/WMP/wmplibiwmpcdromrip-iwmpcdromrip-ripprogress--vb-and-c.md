---
title: Iwmpcdromrip-ripprogress (Eigenschaft)
description: Die ripprogress-Eigenschaft ruft den CD-einreißen-Status als Prozentsatz ab.
ms.assetid: 00d4f074-a16d-4c5f-930f-4411b90303f1
keywords:
- ripprogress-Eigenschaften Fenster Media Player
- ripprogress-Eigenschaften Fenster Media Player, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle Windows Media Player, ripprogress (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPCdromRip.ripProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 113b9fc716698156aa4f7731a7b19888e0edf438
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373818"
---
# <a name="iwmpcdromripripprogress-property"></a><span data-ttu-id="23de0-106">Iwmpcdromrip:: ripprogress (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="23de0-106">IWMPCdromRip::ripProgress property</span></span>

<span data-ttu-id="23de0-107">Die **ripprogress** -Eigenschaft ruft den CD-einreißen-Status als Prozentsatz ab.</span><span class="sxs-lookup"><span data-stu-id="23de0-107">The **ripProgress** property gets the CD ripping progress as percent complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="23de0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="23de0-108">Syntax</span></span>


```CSharp
public System.Int32 ripProgress {get; set;}
```


```VB

Public ReadOnly Property ripProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="23de0-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="23de0-109">Property value</span></span>

<span data-ttu-id="23de0-110">Ein **System. Int32** -Wert, der der Fortschritts Wert ist.</span><span class="sxs-lookup"><span data-stu-id="23de0-110">A **System.Int32** that is the progress value.</span></span> <span data-ttu-id="23de0-111">Die Statuswerte liegen im Bereich von 0 bis 100.</span><span class="sxs-lookup"><span data-stu-id="23de0-111">Progress values range from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="23de0-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23de0-112">Remarks</span></span>

<span data-ttu-id="23de0-113">Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten rippingprozesses dar.</span><span class="sxs-lookup"><span data-stu-id="23de0-113">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="23de0-114">Verwenden Sie zum Bestimmen des Status einer bestimmten Spur " [iwmpmedia. getiteminfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) " mit " **ripprogress** " als Attributnamen.</span><span class="sxs-lookup"><span data-stu-id="23de0-114">To determine the progress of a specific track, use [IWMPMedia.getItemInfo](wmplibiwmpplaylist-iwmpplaylist-getiteminfo--vb-and-c.md) with **RipProgress** as the attribute name.</span></span> <span data-ttu-id="23de0-115">Um den Index des aktuell ausgetauppten Titels abzurufen, nennen Sie iwmpwiedergabe. getiteminfo mit "currentriptrackindex" als Attribut Name.</span><span class="sxs-lookup"><span data-stu-id="23de0-115">To get the index of the track currently being ripped, call IWMPPlaylist.getItemInfo with "CurrentRipTrackIndex" as the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="23de0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23de0-116">Requirements</span></span>



| <span data-ttu-id="23de0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23de0-117">Requirement</span></span> | <span data-ttu-id="23de0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="23de0-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23de0-119">Version</span><span class="sxs-lookup"><span data-stu-id="23de0-119">Version</span></span><br/>   | <span data-ttu-id="23de0-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="23de0-120">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="23de0-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="23de0-121">Namespace</span></span><br/> | <span data-ttu-id="23de0-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="23de0-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="23de0-123">Assembly</span><span class="sxs-lookup"><span data-stu-id="23de0-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="23de0-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="23de0-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23de0-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23de0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23de0-126">**Iwmpcdromrip-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="23de0-126">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="23de0-127">**Ripping einer CD**</span><span class="sxs-lookup"><span data-stu-id="23de0-127">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> </dl>

 

 





