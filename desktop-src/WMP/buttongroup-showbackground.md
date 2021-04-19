---
title: ButtonGroup. showbackground
description: Mit dem showbackground-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob in der ButtonGroup nur die Schaltflächen angezeigt werden, oder es wird die im Image-Attribut angegebene vollständige Bitmap angezeigt.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- ButtonGroup. showbackground-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364643"
---
# <a name="buttongroupshowbackground"></a><span data-ttu-id="b1485-104">ButtonGroup. showbackground</span><span class="sxs-lookup"><span data-stu-id="b1485-104">BUTTONGROUP.showBackground</span></span>

<span data-ttu-id="b1485-105">Mit dem **showbackground** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob in der **ButtonGroup** nur die Schaltflächen angezeigt werden, oder es wird die im **Image** -Attribut angegebene vollständige Bitmap angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1485-105">The **showBackground** attribute specifies or retrieves a value indicating whether the **BUTTONGROUP** displays only the buttons, or displays the full bitmap specified in the **image** attribute.</span></span>

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a><span data-ttu-id="b1485-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b1485-106">Possible Values</span></span>

<span data-ttu-id="b1485-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b1485-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="b1485-108">Wert</span><span class="sxs-lookup"><span data-stu-id="b1485-108">Value</span></span> | <span data-ttu-id="b1485-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1485-109">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1485-110">true</span><span class="sxs-lookup"><span data-stu-id="b1485-110">true</span></span>  | <span data-ttu-id="b1485-111">Schaltflächen werden angezeigt, und der Bereich, der nicht von Schaltflächen besetzt ist, wird aus der Bild Bitmap gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b1485-111">Buttons are displayed and the area not occupied by buttons is drawn from the Image bitmap.</span></span> |
| <span data-ttu-id="b1485-112">false</span><span class="sxs-lookup"><span data-stu-id="b1485-112">false</span></span> | <span data-ttu-id="b1485-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="b1485-113">Default.</span></span> <span data-ttu-id="b1485-114">Es werden nur die Schaltflächen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1485-114">Only the buttons are displayed.</span></span>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="b1485-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1485-115">Remarks</span></span>

<span data-ttu-id="b1485-116">Wenn **showbackground** den Wert true hat, wird das gesamte **Hauptbild** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1485-116">When **showBackground** is true, the entire main **image** will be visible.</span></span>

<span data-ttu-id="b1485-117">Wenn **showbackground** den Wert false hat, werden nur die Bereiche gerendert, die den zugewiesenen **mappingImage** -Farben entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b1485-117">When **showBackground** is false, only the areas corresponding to assigned **mappingImage** colors will be rendered.</span></span> <span data-ttu-id="b1485-118">Das heißt, dass nur **buttonelements** mit ihrer zugewiesenen **mappingColor** sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="b1485-118">In other words, only **BUTTONELEMENTs** with their **mappingColor** assigned will be visible.</span></span>

<span data-ttu-id="b1485-119">Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b1485-119">If an invalid value is specified, the previous state is maintained.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1485-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1485-120">Requirements</span></span>



| <span data-ttu-id="b1485-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1485-121">Requirement</span></span> | <span data-ttu-id="b1485-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b1485-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="b1485-123">Version</span><span class="sxs-lookup"><span data-stu-id="b1485-123">Version</span></span><br/> | <span data-ttu-id="b1485-124">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="b1485-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b1485-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1485-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1485-126">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="b1485-126">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="b1485-127">**ButtonElement. mappingColor**</span><span class="sxs-lookup"><span data-stu-id="b1485-127">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="b1485-128">**ButtonGroup. Image**</span><span class="sxs-lookup"><span data-stu-id="b1485-128">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="b1485-129">**ButtonGroup. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="b1485-129">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





