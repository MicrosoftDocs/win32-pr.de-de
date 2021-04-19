---
title: ButtonGroup. disabledImage
description: Das disabledImage-Attribut gibt den Namen des Bilds an, das den deaktivierten Zustand der Schaltflächen in der ButtonGroup darstellt, oder ruft ihn ab.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- ButtonGroup. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352854"
---
# <a name="buttongroupdisabledimage"></a><span data-ttu-id="70481-104">ButtonGroup. disabledImage</span><span class="sxs-lookup"><span data-stu-id="70481-104">BUTTONGROUP.disabledImage</span></span>

<span data-ttu-id="70481-105">Das **disabledImage** -Attribut gibt den Namen des Bilds an, das den deaktivierten Zustand der Schaltflächen in der **ButtonGroup** darstellt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="70481-105">The **disabledImage** attribute specifies or retrieves the name of the image representing the disabled state of the buttons in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="70481-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="70481-106">Possible Values</span></span>

<span data-ttu-id="70481-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="70481-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="70481-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70481-108">Remarks</span></span>

<span data-ttu-id="70481-109">Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.</span><span class="sxs-lookup"><span data-stu-id="70481-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span> <span data-ttu-id="70481-110">Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="70481-110">If the image is an 8-bit BMP file, its hue and saturation values can be changed dynamically using the **hueShift** and **saturation** attributes.</span></span>

<span data-ttu-id="70481-111">Wenn das **Deaktivierte** Attribut eines **ButtonElement** -Elements auf true festgelegt ist, wird der zugehörige Bereich von **disabledImage** für die **ButtonGroup** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70481-111">When the **disabled** attribute of a **BUTTONELEMENT** element is set to true, the corresponding region of the **disabledImage** for the **BUTTONGROUP** is displayed.</span></span> <span data-ttu-id="70481-112">Wenn das deaktivierte Bild größer als der definierte Bereich ist, wird das deaktivierte Bild beschnitten.</span><span class="sxs-lookup"><span data-stu-id="70481-112">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="70481-113">Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="70481-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="70481-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="70481-114">Requirements</span></span>



| <span data-ttu-id="70481-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="70481-115">Requirement</span></span> | <span data-ttu-id="70481-116">Wert</span><span class="sxs-lookup"><span data-stu-id="70481-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="70481-117">Version</span><span class="sxs-lookup"><span data-stu-id="70481-117">Version</span></span><br/> | <span data-ttu-id="70481-118">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="70481-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70481-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70481-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70481-120">**ButtonGroup-Element**</span><span class="sxs-lookup"><span data-stu-id="70481-120">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="70481-121">**ButtonGroup. hueshift**</span><span class="sxs-lookup"><span data-stu-id="70481-121">**BUTTONGROUP.hueShift**</span></span>](buttongroup-hueshift.md)
</dt> <dt>

[<span data-ttu-id="70481-122">**ButtonGroup. Sättigung**</span><span class="sxs-lookup"><span data-stu-id="70481-122">**BUTTONGROUP.saturation**</span></span>](buttongroup-saturation.md)
</dt> </dl>

 

 





