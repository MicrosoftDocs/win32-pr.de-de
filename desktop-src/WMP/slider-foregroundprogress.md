---
title: Schieberegler. foregroundprogress
description: Das foregroundprogress-Attribut gibt die aktuelle Position der Statusanzeige im Vordergrund als Prozentsatz des Schieberegler-Bereichs an oder ruft diese ab.
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- Schieberegler. foregroundprogress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373894"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="4f128-104">Schieberegler. foregroundprogress</span><span class="sxs-lookup"><span data-stu-id="4f128-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="4f128-105">Das **foregroundprogress** -Attribut gibt die aktuelle Position der Statusanzeige im Vordergrund als Prozentsatz des Schieberegler-Bereichs an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="4f128-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="4f128-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4f128-106">Possible Values</span></span>

<span data-ttu-id="4f128-107">Dieses Attribut ist eine Lese-/schreibnummer (**float**) im Bereich von 0 bis 100. </span><span class="sxs-lookup"><span data-stu-id="4f128-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f128-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f128-108">Remarks</span></span>

<span data-ttu-id="4f128-109">Dieses Attribut wird hauptsächlich verwendet, um den Download Fortschritt einer Mediendatei zu verfolgen, während gleichzeitig die aktuelle Wiedergabe Position der Datei mithilfe des **value** -Attributs nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="4f128-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="4f128-110">Die Position des Zieh Punkts für den Schieberegler ist auf den Bereich des Vordergrund Fortschritts beschränkt.</span><span class="sxs-lookup"><span data-stu-id="4f128-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="4f128-111">Dadurch wird die interaktive Suche nur innerhalb des verfügbaren Teils einer Downloaddatei ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4f128-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="4f128-112">Um diese Funktion verwenden zu können, muss das **useforegroundprogress** -Attribut auf "true" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4f128-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="4f128-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f128-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="4f128-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f128-114">Requirements</span></span>



| <span data-ttu-id="4f128-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f128-115">Requirement</span></span> | <span data-ttu-id="4f128-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4f128-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4f128-117">Version</span><span class="sxs-lookup"><span data-stu-id="4f128-117">Version</span></span><br/> | <span data-ttu-id="4f128-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4f128-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f128-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f128-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f128-120">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="4f128-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="4f128-121">**Schieberegler. min.**</span><span class="sxs-lookup"><span data-stu-id="4f128-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="4f128-122">**Schieberegler. Max**</span><span class="sxs-lookup"><span data-stu-id="4f128-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="4f128-123">**Schieberegler. useforegroundprogress**</span><span class="sxs-lookup"><span data-stu-id="4f128-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="4f128-124">**Slider. Wert**</span><span class="sxs-lookup"><span data-stu-id="4f128-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





