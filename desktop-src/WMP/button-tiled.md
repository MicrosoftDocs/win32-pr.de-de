---
title: Schaltfläche. Kachel
description: Mit dem gekachelten Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Schaltflächen Bild angezeigt wird.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- Schaltfläche. gekachelte Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354826"
---
# <a name="buttontiled"></a><span data-ttu-id="ec94d-104">Schaltfläche. Kachel</span><span class="sxs-lookup"><span data-stu-id="ec94d-104">BUTTON.tiled</span></span>

<span data-ttu-id="ec94d-105">Mit dem **gekachelten** Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das **Schalt** Flächen Bild angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec94d-105">The **tiled** attribute specifies or retrieves a value indicating whether the **BUTTON** image will be tiled.</span></span>

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a><span data-ttu-id="ec94d-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ec94d-106">Possible Values</span></span>

<span data-ttu-id="ec94d-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="ec94d-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="ec94d-108">Wert</span><span class="sxs-lookup"><span data-stu-id="ec94d-108">Value</span></span> | <span data-ttu-id="ec94d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ec94d-109">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="ec94d-110">true</span><span class="sxs-lookup"><span data-stu-id="ec94d-110">true</span></span>  | <span data-ttu-id="ec94d-111">Das Bild wird gekachelt.</span><span class="sxs-lookup"><span data-stu-id="ec94d-111">Image will be tiled.</span></span>              |
| <span data-ttu-id="ec94d-112">false</span><span class="sxs-lookup"><span data-stu-id="ec94d-112">false</span></span> | <span data-ttu-id="ec94d-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="ec94d-113">Default.</span></span> <span data-ttu-id="ec94d-114">Das Bild wird nicht gekachelt.</span><span class="sxs-lookup"><span data-stu-id="ec94d-114">Image will not be tiled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ec94d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec94d-115">Remarks</span></span>

<span data-ttu-id="ec94d-116">Wenn das Bild kleiner als der tatsächliche Bereich des Steuer Elements ist, wird es durch das Zicken des Bilds wiederholt, bis die gesamte Region ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="ec94d-116">If the image is smaller than the actual region of the control, then tiling the image will repeat it until it fills the entire region.</span></span> <span data-ttu-id="ec94d-117">Wenn kein Bild angegeben ist oder nicht abgerufen werden kann, wird die **Kachel** auf false festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ec94d-117">If an image is not specified or cannot be retrieved, **tiled** will be set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec94d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ec94d-118">Requirements</span></span>



| <span data-ttu-id="ec94d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ec94d-119">Requirement</span></span> | <span data-ttu-id="ec94d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ec94d-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ec94d-121">Version</span><span class="sxs-lookup"><span data-stu-id="ec94d-121">Version</span></span><br/> | <span data-ttu-id="ec94d-122">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="ec94d-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ec94d-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec94d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec94d-124">**Button-Element**</span><span class="sxs-lookup"><span data-stu-id="ec94d-124">**BUTTON Element**</span></span>](button-element.md)
</dt> <dt>

[<span data-ttu-id="ec94d-125">**Button. Bild**</span><span class="sxs-lookup"><span data-stu-id="ec94d-125">**BUTTON.image**</span></span>](button-image.md)
</dt> </dl>

 

 





