---
title: Column. columnresizemode
description: Das columnresizemode-Attribut gibt den Größenänderung Modus für diese Spalte an oder ruft ihn ab.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- Column. columnresizemode-Windows-Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52d17b1a2edd878fb15e69c595e3c061c1963a5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369687"
---
# <a name="columncolumnresizemode"></a><span data-ttu-id="0abaf-104">Column. columnresizemode</span><span class="sxs-lookup"><span data-stu-id="0abaf-104">COLUMN.columnResizeMode</span></span>

<span data-ttu-id="0abaf-105">Das **columnresizemode** -Attribut gibt den Größenänderung Modus für diese Spalte an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="0abaf-105">The **columnResizeMode** attribute specifies or retrieves the resize mode for this column.</span></span>

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a><span data-ttu-id="0abaf-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0abaf-106">Possible Values</span></span>

<span data-ttu-id="0abaf-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="0abaf-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="0abaf-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0abaf-108">Value</span></span>          | <span data-ttu-id="0abaf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0abaf-109">Description</span></span>                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0abaf-110">Autosizeheader</span><span class="sxs-lookup"><span data-stu-id="0abaf-110">AutosizeHeader</span></span> | <span data-ttu-id="0abaf-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="0abaf-111">Default.</span></span> <span data-ttu-id="0abaf-112">Die Größe der Spaltengröße wird an alle Daten in der Spalte und in der Kopfzeile angepasst.</span><span class="sxs-lookup"><span data-stu-id="0abaf-112">The column resizes to accommodate all data in both the column and the header.</span></span>                         |
| <span data-ttu-id="0abaf-113">Autosizedata</span><span class="sxs-lookup"><span data-stu-id="0abaf-113">AutosizeData</span></span>   | <span data-ttu-id="0abaf-114">Die Spaltengröße ändert sich, um nur alle Daten in der Spalte zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0abaf-114">The column resizes to accommodate all data in the column only.</span></span>                                                 |
| <span data-ttu-id="0abaf-115">Fest</span><span class="sxs-lookup"><span data-stu-id="0abaf-115">Fixed</span></span>          | <span data-ttu-id="0abaf-116">Die Spalte hat eine Größe mit fester Größe.</span><span class="sxs-lookup"><span data-stu-id="0abaf-116">The column is a fixed size.</span></span>                                                                                    |
| <span data-ttu-id="0abaf-117">Dehn</span><span class="sxs-lookup"><span data-stu-id="0abaf-117">Stretches</span></span>      | <span data-ttu-id="0abaf-118">Die Größe der Spalte ändert sich, um den verbleibenden Platz im **Wiedergabe** Listen-Steuerelement zu verwenden, nachdem alle anderen Spalten geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="0abaf-118">The column resizes to use the remaining space in the **PLAYLIST** control after all other columns are resized.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0abaf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0abaf-119">Requirements</span></span>



| <span data-ttu-id="0abaf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0abaf-120">Requirement</span></span> | <span data-ttu-id="0abaf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0abaf-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="0abaf-122">Version</span><span class="sxs-lookup"><span data-stu-id="0abaf-122">Version</span></span><br/> | <span data-ttu-id="0abaf-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0abaf-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0abaf-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0abaf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abaf-125">**Column-Element**</span><span class="sxs-lookup"><span data-stu-id="0abaf-125">**COLUMN Element**</span></span>](column-element.md)
</dt> </dl>

 

 





