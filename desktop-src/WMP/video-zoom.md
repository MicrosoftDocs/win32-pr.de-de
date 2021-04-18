---
title: Video. Zoom
description: Das Zoom Attribut gibt den Prozentsatz an, um den das Video skaliert werden soll.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- Video. Zoom-Fenster Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354438"
---
# <a name="videozoom"></a><span data-ttu-id="0d1ce-104">Video. Zoom</span><span class="sxs-lookup"><span data-stu-id="0d1ce-104">VIDEO.zoom</span></span>

<span data-ttu-id="0d1ce-105">Das **Zoom** Attribut gibt den Prozentsatz an, um den das Video skaliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="0d1ce-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0d1ce-106">Possible Values</span></span>

<span data-ttu-id="0d1ce-107">Dieses Attribut ist eine Lese-/schreibzahl (**Long**), die zwischen 1 und der maximalen Größe liegt, die von der Breite und Höhe des Video Steuer Elements untergebracht wird. </span><span class="sxs-lookup"><span data-stu-id="0d1ce-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="0d1ce-108">Der Standardwert ist 100.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d1ce-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d1ce-109">Remarks</span></span>

<span data-ttu-id="0d1ce-110">Dieses Attribut kann nicht in Verbindung mit dem **Fullscreen** -Attribut verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="0d1ce-111">Wenn " **Width** " und " **height** " angegeben sind und das resultierende Videofenster größer als das Video ist, das abgespielt wird, kann das Video durch zentrales hochskalieren auf die maximale Größe des Fensters vergrößert werden.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="0d1ce-112">Wenn " **Width** " und " **height** " nicht angegeben sind, ist " **Zoom** " auf Werte von 100 oder weniger beschränkt.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="0d1ce-113">Wenn die Eigenschaft **ShrinkToFit** den Wert false hat, ändert sich das Video proportional beim Zoomen, um sich an den verfügbaren Platz anzupassen.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="0d1ce-114">Wenn **ShrinkToFit** den Wert true hat, wird das Video verkleinert, damit es in die restriktivste Dimension passt, wobei die ursprünglichen Proportionen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1ce-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d1ce-115">Requirements</span></span>



| <span data-ttu-id="0d1ce-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d1ce-116">Requirement</span></span> | <span data-ttu-id="0d1ce-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0d1ce-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0d1ce-118">Version</span><span class="sxs-lookup"><span data-stu-id="0d1ce-118">Version</span></span><br/> | <span data-ttu-id="0d1ce-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0d1ce-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d1ce-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d1ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1ce-121">**Video-Element**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="0d1ce-122">**Video. Fullscreen**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="0d1ce-123">**Video. ShrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="0d1ce-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 





