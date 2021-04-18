---
title: ButtonElement. mappingColor
description: Das mappingColor-Attribut gibt den Farbschlüssel an, der dieses ButtonElement in der ButtonGroup identifiziert, oder ruft ihn ab.
ms.assetid: e7b1663c-3263-41d5-9a69-4cf1dcf0fc1f
keywords:
- ButtonElement. mappingColor-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.mappingColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7318f01246578fe8ff34118427c95afb7b3bb098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365932"
---
# <a name="buttonelementmappingcolor"></a><span data-ttu-id="af1ac-104">ButtonElement. mappingColor</span><span class="sxs-lookup"><span data-stu-id="af1ac-104">BUTTONELEMENT.mappingColor</span></span>

<span data-ttu-id="af1ac-105">Das **mappingColor** -Attribut gibt den Farbschlüssel an, der dieses **ButtonElement** in der **ButtonGroup** identifiziert, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="af1ac-105">The **mappingColor** attribute specifies or retrieves the color key that identifies this **BUTTONELEMENT** in the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingColor
```

## <a name="possible-values"></a><span data-ttu-id="af1ac-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="af1ac-106">Possible Values</span></span>

<span data-ttu-id="af1ac-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert.</span><span class="sxs-lookup"><span data-stu-id="af1ac-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value.</span></span> <span data-ttu-id="af1ac-108">Er besitzt keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="af1ac-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af1ac-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af1ac-109">Remarks</span></span>

<span data-ttu-id="af1ac-110">Dieses Attribut gibt die Farbe des Bereichs in der Schaltflächen Gruppe **mappingImage** an, die diesem Schaltflächen Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="af1ac-110">This attribute specifies the color of the region in the button group **mappingImage** that corresponds to this button element.</span></span> <span data-ttu-id="af1ac-111">Alle Klicks in diesem Bereich werden von diesem Schaltflächen Element behandelt.</span><span class="sxs-lookup"><span data-stu-id="af1ac-111">All clicks on this region are handled by this button element.</span></span>

<span data-ttu-id="af1ac-112">Wenn eine ungültige Farbe angegeben ist, wird das **ButtonElement** nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af1ac-112">If an invalid color is specified, the **BUTTONELEMENT** is not activated.</span></span>

## <a name="examples"></a><span data-ttu-id="af1ac-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af1ac-113">Examples</span></span>

<span data-ttu-id="af1ac-114">Das folgende Beispiel ist eine komplette Skin-Definitionsdatei, die veranschaulicht, wie einige der **ButtonElement** -Attribute verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af1ac-114">The following sample is a complete skin definition file that illustrates how some of the **BUTTONELEMENT** attributes are used.</span></span> <span data-ttu-id="af1ac-115">Sie befindet sich im Verzeichnis Samples, das mit dem SDK installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="af1ac-115">It can be found in the Samples directory that was installed with the SDK.</span></span>


```
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >
    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    />
    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "150"
    />
    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    >
      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />
      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />
    </BUTTONGROUP>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="af1ac-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af1ac-116">Requirements</span></span>



| <span data-ttu-id="af1ac-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af1ac-117">Requirement</span></span> | <span data-ttu-id="af1ac-118">Wert</span><span class="sxs-lookup"><span data-stu-id="af1ac-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="af1ac-119">Version</span><span class="sxs-lookup"><span data-stu-id="af1ac-119">Version</span></span><br/> | <span data-ttu-id="af1ac-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="af1ac-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af1ac-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af1ac-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1ac-122">**Farb Verweis**</span><span class="sxs-lookup"><span data-stu-id="af1ac-122">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="af1ac-123">**ButtonElement-Element**</span><span class="sxs-lookup"><span data-stu-id="af1ac-123">**BUTTONELEMENT Element**</span></span>](buttonelement-element.md)
</dt> <dt>

[<span data-ttu-id="af1ac-124">**ButtonGroup. mappingImage**</span><span class="sxs-lookup"><span data-stu-id="af1ac-124">**BUTTONGROUP.mappingImage**</span></span>](buttongroup-mappingimage.md)
</dt> </dl>

 

 





