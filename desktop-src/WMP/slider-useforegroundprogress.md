---
title: Schieberegler. useforegroundprogress
description: Mit dem useforegroundprogress-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob die Statusleiste des Vordergrunds verwendet wird.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Schieberegler. useforegroundprogress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360323"
---
# <a name="slideruseforegroundprogress"></a><span data-ttu-id="673ec-104">Schieberegler. useforegroundprogress</span><span class="sxs-lookup"><span data-stu-id="673ec-104">SLIDER.useForegroundProgress</span></span>

<span data-ttu-id="673ec-105">Mit dem **useforegroundprogress** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob die Statusleiste des Vordergrunds verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="673ec-105">The **useForegroundProgress** attribute specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="673ec-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="673ec-106">Possible Values</span></span>

<span data-ttu-id="673ec-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="673ec-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="673ec-108">Wert</span><span class="sxs-lookup"><span data-stu-id="673ec-108">Value</span></span> | <span data-ttu-id="673ec-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="673ec-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="673ec-110">true</span><span class="sxs-lookup"><span data-stu-id="673ec-110">true</span></span>  | <span data-ttu-id="673ec-111">Verwenden Sie den Vordergrund Fortschritt.</span><span class="sxs-lookup"><span data-stu-id="673ec-111">Use foreground progress.</span></span>                 |
| <span data-ttu-id="673ec-112">false</span><span class="sxs-lookup"><span data-stu-id="673ec-112">false</span></span> | <span data-ttu-id="673ec-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="673ec-113">Default.</span></span> <span data-ttu-id="673ec-114">Verwenden Sie den Vordergrund Status nicht.</span><span class="sxs-lookup"><span data-stu-id="673ec-114">Do not use foreground progress.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="673ec-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="673ec-115">Remarks</span></span>

<span data-ttu-id="673ec-116">Dieses Attribut ermöglicht die Verwendung des **foregroundprogress** -Attributs, das hauptsächlich verwendet wird, um den Download Fortschritt einer Mediendatei zu verfolgen, während gleichzeitig die aktuelle Wiedergabe Position der Datei mithilfe des **value** -Attributs nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="673ec-116">This attribute allows the use of the **foregroundProgress** attribute, which is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="673ec-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="673ec-117">Requirements</span></span>



| <span data-ttu-id="673ec-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="673ec-118">Requirement</span></span> | <span data-ttu-id="673ec-119">Wert</span><span class="sxs-lookup"><span data-stu-id="673ec-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="673ec-120">Version</span><span class="sxs-lookup"><span data-stu-id="673ec-120">Version</span></span><br/> | <span data-ttu-id="673ec-121">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="673ec-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="673ec-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="673ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673ec-123">**Slider-Element**</span><span class="sxs-lookup"><span data-stu-id="673ec-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="673ec-124">**Schieberegler. foregroundprogress**</span><span class="sxs-lookup"><span data-stu-id="673ec-124">**SLIDER.foregroundProgress**</span></span>](slider-foregroundprogress.md)
</dt> <dt>

[<span data-ttu-id="673ec-125">**Slider. Wert**</span><span class="sxs-lookup"><span data-stu-id="673ec-125">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





