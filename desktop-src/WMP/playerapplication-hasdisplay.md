---
title: Playerapplication. hasdisplay
description: Die hasdisplay-Eigenschaft ruft einen Wert ab, der angibt, ob Videos über das Remote Player-Steuerelement angezeigt werden können.
ms.assetid: f90c5470-f985-4b98-823f-7395f89b238b
keywords:
- Playerapplication. hasdisplay-Windows-Media Player
topic_type:
- apiref
api_name:
- PlayerApplication.hasDisplay
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef77cb42109decef6ab435aa031240f89b6cb98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358353"
---
# <a name="playerapplicationhasdisplay"></a><span data-ttu-id="c201b-104">Playerapplication. hasdisplay</span><span class="sxs-lookup"><span data-stu-id="c201b-104">PlayerApplication.hasDisplay</span></span>

<span data-ttu-id="c201b-105">Die **hasdisplay** -Eigenschaft ruft einen Wert ab, der angibt, ob Videos über das Remote Player-Steuerelement angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="c201b-105">The **hasDisplay** property retrieves a value indicating whether video can display through the remoted Player control.</span></span>

## <a name="syntax"></a><span data-ttu-id="c201b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c201b-106">Syntax</span></span>

<span data-ttu-id="c201b-107">*playerapplication*. **hasdisplay**</span><span class="sxs-lookup"><span data-stu-id="c201b-107">*playerApplication*.**hasDisplay**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c201b-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="c201b-108">Possible Values</span></span>

<span data-ttu-id="c201b-109">Diese Eigenschaft ist ein Schreib geschützter **boolescher** Wert.</span><span class="sxs-lookup"><span data-stu-id="c201b-109">This property is a read-only **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c201b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c201b-110">Remarks</span></span>

<span data-ttu-id="c201b-111">Diese Eigenschaft wird nur verwendet, wenn das Windows Media Player-Steuerelement Remoting ist.</span><span class="sxs-lookup"><span data-stu-id="c201b-111">This property is used only when remoting the Windows Media Player control.</span></span>

<span data-ttu-id="c201b-112">Mehrere Windows Media Player-Steuerelemente können gleichzeitig remote ausgeführt werden, aber Video kann nur jeweils an einer Stelle angezeigt werden, entweder im vollständigen Modus des Players oder in einem der remoten Windows Media Player-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="c201b-112">Several Windows Media Player controls can be running remotely at the same time, but video can only display in one location at a time, either in the full mode of the Player or in one of the remoted Windows Media Player controls.</span></span> <span data-ttu-id="c201b-113">Verwenden Sie diese Eigenschaft, um zu bestimmen, ob das aktuelle Steuerelement das aktuelle Steuerelement ist, durch das Video angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c201b-113">Use this property to determine whether the current control is the one through which video can be displayed.</span></span>

<span data-ttu-id="c201b-114">**Windows Media Player 10 Mobile:** Diese Eigenschaft gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="c201b-114">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c201b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c201b-115">Requirements</span></span>



| <span data-ttu-id="c201b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c201b-116">Requirement</span></span> | <span data-ttu-id="c201b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c201b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c201b-118">Version</span><span class="sxs-lookup"><span data-stu-id="c201b-118">Version</span></span><br/> | <span data-ttu-id="c201b-119">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c201b-119">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c201b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c201b-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="c201b-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c201b-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c201b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c201b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c201b-123">**Playerapplication-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c201b-123">**PlayerApplication Object**</span></span>](playerapplication-object.md)
</dt> <dt>

[<span data-ttu-id="c201b-124">**Remoting des Windows Media Player-Steuerelements**</span><span class="sxs-lookup"><span data-stu-id="c201b-124">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





