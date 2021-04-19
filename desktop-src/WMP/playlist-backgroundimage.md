---
title: Wiedergabeliste. BackgroundImage
description: Das BackgroundImage-Attribut gibt das Hintergrundbild an oder ruft es ab.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Wiedergabeliste. BackgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369125"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="fa5c5-104">Wiedergabeliste. BackgroundImage</span><span class="sxs-lookup"><span data-stu-id="fa5c5-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="fa5c5-105">Das **BackgroundImage** -Attribut gibt das Hintergrundbild an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="fa5c5-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="fa5c5-106">Possible Values</span></span>

<span data-ttu-id="fa5c5-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="fa5c5-108">Er besitzt keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5c5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa5c5-109">Remarks</span></span>

<span data-ttu-id="fa5c5-110">Wenn die Bildhöhe und-Breite kleiner als die Höhe und Breite des **Wiedergabe** Listen Elements sind, wird das Bild gekachelt.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="fa5c5-111">Die unterstützten Formate sind BMP, JPG, GIF und PNG.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="fa5c5-112">Das Angeben des Werts "Gradient" für das Hintergrundbild bewirkt, dass der Hintergrund der Wiedergabeliste als Farbverlauf angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="fa5c5-113">Dies bedeutet, dass die Hintergrundfarbe allmählich zwischen der [Wiedergabeliste. BackgroundColor](playlist-backgroundcolor.md) (am oberen Rand des Hintergrunds) und den [Wiedergabelisten. statusColor](playlist-statuscolor.md) -Werten übergeht.</span><span class="sxs-lookup"><span data-stu-id="fa5c5-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5c5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fa5c5-114">Requirements</span></span>



| <span data-ttu-id="fa5c5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fa5c5-115">Requirement</span></span> | <span data-ttu-id="fa5c5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fa5c5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5c5-117">Version</span><span class="sxs-lookup"><span data-stu-id="fa5c5-117">Version</span></span><br/> | <span data-ttu-id="fa5c5-118">Windows Media Player, Version 7,0 oder höher, Windows Media Player 10 für das Farbverlaufs Feature</span><span class="sxs-lookup"><span data-stu-id="fa5c5-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa5c5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa5c5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa5c5-120">**Wiedergabelisten Element**</span><span class="sxs-lookup"><span data-stu-id="fa5c5-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





