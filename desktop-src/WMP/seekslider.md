---
title: SeekSlider
description: Dies ist ein vordefinierter Schieberegler mit den folgenden Standardwerten. | SeekSlider
ms.assetid: 9fdb0f70-e5ce-4dbc-aeba-44fa0e2c9b3c
keywords:
- SeekSlider-Fenster Media Player
topic_type:
- apiref
api_name:
- SEEKSLIDER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59808fa7c41acfcc28b715362b8724c7f113faee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370598"
---
# <a name="seekslider"></a><span data-ttu-id="0b8d8-105">SeekSlider</span><span class="sxs-lookup"><span data-stu-id="0b8d8-105">SEEKSLIDER</span></span>

<span data-ttu-id="0b8d8-106">Dies ist ein vordefinierter **Schieberegler** mit den folgenden Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="0b8d8-106">This is a predefined **SLIDER** with the following default values.</span></span>

``` syntax
toolTip="Seek"
foregroundProgress="wmpprop:player.network.downloadProgress"
max="wmpprop:player.currentMedia.duration"
min="0"
value="wmpprop:player.controls.currentPosition"
onDragEnd="jscript:player.controls.currentPosition=value;"
useForegroundProgress="true"
```

## <a name="remarks"></a><span data-ttu-id="0b8d8-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b8d8-107">Remarks</span></span>

<span data-ttu-id="0b8d8-108">Dadurch wird ein **Schieberegler** -Steuerelement erstellt, das die Mediendatei an einer beliebigen Position sucht.</span><span class="sxs-lookup"><span data-stu-id="0b8d8-108">This creates a **SLIDER** control that seeks the media file to any position.</span></span> <span data-ttu-id="0b8d8-109">Die Quick Infos sind lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="0b8d8-109">The ToolTips are localized.</span></span> <span data-ttu-id="0b8d8-110">Alle Eigenschaften dieses **Schiebereglers** können überschrieben werden, indem Sie explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0b8d8-110">All properties of this **SLIDER** can be overridden by explicitly specifying them.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8d8-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0b8d8-111">Requirements</span></span>



| <span data-ttu-id="0b8d8-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0b8d8-112">Requirement</span></span> | <span data-ttu-id="0b8d8-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0b8d8-113">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="0b8d8-114">Version</span><span class="sxs-lookup"><span data-stu-id="0b8d8-114">Version</span></span><br/> | <span data-ttu-id="0b8d8-115">Windows Media Player 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0b8d8-115">Windows Media Player 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b8d8-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0b8d8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8d8-117">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="0b8d8-117">**SLIDER Element**</span></span>](slider-element.md)
</dt> </dl>

 

 





