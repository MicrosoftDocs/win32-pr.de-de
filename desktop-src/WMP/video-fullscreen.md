---
title: Video. Fullscreen
description: Mit dem Fullscreen-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Video im Vollbildmodus angezeigt wird.
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- Video. Fullscreen-Fenster Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368634"
---
# <a name="videofullscreen"></a><span data-ttu-id="7c115-104">Video. Fullscreen</span><span class="sxs-lookup"><span data-stu-id="7c115-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="7c115-105">Mit dem **Fullscreen** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Video im Vollbildmodus angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7c115-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="7c115-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7c115-106">Possible Values</span></span>

<span data-ttu-id="7c115-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c115-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7c115-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7c115-108">Value</span></span> | <span data-ttu-id="7c115-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c115-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="7c115-110">true</span><span class="sxs-lookup"><span data-stu-id="7c115-110">true</span></span>  | <span data-ttu-id="7c115-111">Video wird im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c115-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="7c115-112">false</span><span class="sxs-lookup"><span data-stu-id="7c115-112">false</span></span> | <span data-ttu-id="7c115-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="7c115-113">Default.</span></span> <span data-ttu-id="7c115-114">Video wird nicht im Vollbildmodus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c115-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7c115-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c115-115">Remarks</span></span>

<span data-ttu-id="7c115-116">Diese Eigenschaft kann nur zur Laufzeit angegeben werden, nachdem eine Datei geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="7c115-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="7c115-117">Daher muss Sie in einem Skript Ereignishandler festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7c115-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="7c115-118">Die Schaltfläche "Escape" wird verwendet, um zur normalen Anzeige zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="7c115-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c115-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c115-119">Requirements</span></span>



| <span data-ttu-id="7c115-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c115-120">Requirement</span></span> | <span data-ttu-id="7c115-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7c115-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7c115-122">Version</span><span class="sxs-lookup"><span data-stu-id="7c115-122">Version</span></span><br/> | <span data-ttu-id="7c115-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7c115-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c115-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c115-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c115-125">**Video-Element**</span><span class="sxs-lookup"><span data-stu-id="7c115-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="7c115-126">**Video. wart AspectRatio**</span><span class="sxs-lookup"><span data-stu-id="7c115-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="7c115-127">**Video. ShrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="7c115-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="7c115-128">**Video. stretchdefit**</span><span class="sxs-lookup"><span data-stu-id="7c115-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





