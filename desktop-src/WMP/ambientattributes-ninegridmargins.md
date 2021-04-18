---
title: Ambientattribute. ninegridmargin
description: Das ninegridmargin-Attribut gibt die Rand breiten für die nicht einheitliche Skalierung des Skin-Elements an.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- Ambientattribute. ninegridmargins-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372291"
---
# <a name="ambientattributesninegridmargins"></a><span data-ttu-id="7545f-104">Ambientattribute. ninegridmargin</span><span class="sxs-lookup"><span data-stu-id="7545f-104">AmbientAttributes.nineGridMargins</span></span>

<span data-ttu-id="7545f-105">Das **ninegridmargin** -Attribut gibt die Rand breiten für die nicht einheitliche Skalierung des Skin-Elements an.</span><span class="sxs-lookup"><span data-stu-id="7545f-105">The **nineGridMargins** attribute specifies margin widths for non-uniform scaling of the skin element.</span></span>

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a><span data-ttu-id="7545f-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7545f-106">Possible Values</span></span>

<span data-ttu-id="7545f-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die die Breite der Ränder in der Form "*widthleft*,*widthtop*,*widthright*,*widthbottom*" enthält.</span><span class="sxs-lookup"><span data-stu-id="7545f-107">This attribute is a read/write **String** that contains the widths of the margins in the form "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*".</span></span> <span data-ttu-id="7545f-108">Jeder width-Wert ist eine Zahl, die die Breite eines Randes neun Rasters in Pixel darstellt.</span><span class="sxs-lookup"><span data-stu-id="7545f-108">Each width value is a number representing the width, in pixels, of a margin for the nine grid.</span></span>

## <a name="remarks"></a><span data-ttu-id="7545f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7545f-109">Remarks</span></span>

<span data-ttu-id="7545f-110">Ein *neun Raster* ist eine Technik, mit der Benutzeroberflächen Elemente in neun rechteckige Bereiche aufgeteilt werden, die in einer 3 x 3-Matrix angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7545f-110">A *nine grid* is a technique used to divide user interface elements into nine rectangular regions arranged in a 3 by 3 matrix.</span></span> <span data-ttu-id="7545f-111">Wenn die Größe eines Elements geändert wird, können die neun Raster Bereiche jeweils mit einem anderen Faktor skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="7545f-111">When an element is resized, the nine grid regions can each scale by a different factor.</span></span>

<span data-ttu-id="7545f-112">Jeder der vier Width-Werte, die Sie angeben, stellt die Breite einer Zeile oder Spalte von drei angrenzenden Regionen dar.</span><span class="sxs-lookup"><span data-stu-id="7545f-112">Each of the four width values you specify represents the width of a row or column of three adjacent regions.</span></span> <span data-ttu-id="7545f-113">Jede Zeile oder Spalte bildet die linke Seite, die obere, die Rechte Seite oder das Ende des neun Rasters.</span><span class="sxs-lookup"><span data-stu-id="7545f-113">Each row or column forms the left side, top, right side, or bottom of the nine grid.</span></span>

<span data-ttu-id="7545f-114">" [Ambientattribute. resizeimages](ambientattributes-resizeimages.md) " muss auf "true" festgelegt werden, damit dieses Attribut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7545f-114">[AmbientAttributes.resizeImages](ambientattributes-resizeimages.md) must be set to true for this attribute to work.</span></span>

## <a name="requirements"></a><span data-ttu-id="7545f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7545f-115">Requirements</span></span>



| <span data-ttu-id="7545f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7545f-116">Requirement</span></span> | <span data-ttu-id="7545f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7545f-117">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="7545f-118">Version</span><span class="sxs-lookup"><span data-stu-id="7545f-118">Version</span></span><br/> | <span data-ttu-id="7545f-119">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="7545f-119">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7545f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7545f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7545f-121">**Ambient-Attribute**</span><span class="sxs-lookup"><span data-stu-id="7545f-121">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





