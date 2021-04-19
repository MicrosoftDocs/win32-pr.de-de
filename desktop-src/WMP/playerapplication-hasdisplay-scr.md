---
title: Playerapplication. hasdisplay-Attribut
description: Das hasdisplay-Attribut Ruft einen Wert ab, der angibt, ob Videos über das Remote Fenster Media Player-Steuerelement angezeigt werden können.
ms.assetid: c6a735a4-29ae-401c-9381-d8aad2c456eb
keywords:
- Playerapplication. hasdisplay-Windows-Media Player
topic_type:
- apiref
api_name:
- PLAYERAPPLICATION.hasDisplay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7579c724496ee2f36ce12adb01c2f13a0962e7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372335"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="3dc8f-104">Playerapplication. hasdisplay</span><span class="sxs-lookup"><span data-stu-id="3dc8f-104">PLAYERAPPLICATION.hasDisplay</span></span>

<span data-ttu-id="3dc8f-105">Das **hasdisplay** -Attribut Ruft einen Wert ab, der angibt, ob Videos über das Remote Fenster Media Player-Steuerelement angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-105">The **hasDisplay** attribute retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span>

``` syntax
        elementID.hasDisplay
```

## <a name="possible-values"></a><span data-ttu-id="3dc8f-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="3dc8f-106">Possible Values</span></span>

<span data-ttu-id="3dc8f-107">Dieses Attribut ist ein Schreib geschützter **boolescher** Wert.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="3dc8f-108">Wert</span><span class="sxs-lookup"><span data-stu-id="3dc8f-108">Value</span></span> | <span data-ttu-id="3dc8f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dc8f-109">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="3dc8f-110">True</span><span class="sxs-lookup"><span data-stu-id="3dc8f-110">True</span></span>  | <span data-ttu-id="3dc8f-111">Das Video kann angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-111">The video can display.</span></span>    |
| <span data-ttu-id="3dc8f-112">False</span><span class="sxs-lookup"><span data-stu-id="3dc8f-112">False</span></span> | <span data-ttu-id="3dc8f-113">Das Video kann nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-113">The video cannot display.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3dc8f-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dc8f-114">Remarks</span></span>

<span data-ttu-id="3dc8f-115">Dieses Attribut wird nur verwendet, wenn das Windows Media Player-Steuerelement Remoting ist.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-115">This attribute is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="3dc8f-116">Mehrere Windows Media Player-Steuerelemente können gleichzeitig remote ausgeführt werden, aber Video kann nur jeweils an einer Stelle angezeigt werden, entweder im vollständigen Modus des Players oder in einem der Remote Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-116">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted controls.</span></span> <span data-ttu-id="3dc8f-117">Verwenden Sie diese Eigenschaft, um zu bestimmen, ob das aktuelle Steuerelement das aktuelle Steuerelement ist, durch das Video angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3dc8f-117">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc8f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dc8f-118">Requirements</span></span>



| <span data-ttu-id="3dc8f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dc8f-119">Requirement</span></span> | <span data-ttu-id="3dc8f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3dc8f-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="3dc8f-121">Version</span><span class="sxs-lookup"><span data-stu-id="3dc8f-121">Version</span></span><br/> | <span data-ttu-id="3dc8f-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="3dc8f-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3dc8f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dc8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc8f-124">**Playerapplication-Element**</span><span class="sxs-lookup"><span data-stu-id="3dc8f-124">**PLAYERAPPLICATION Element**</span></span>](playerapplication-element.md)
</dt> <dt>

[<span data-ttu-id="3dc8f-125">**Remoting des Windows Media Player-Steuerelements**</span><span class="sxs-lookup"><span data-stu-id="3dc8f-125">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





