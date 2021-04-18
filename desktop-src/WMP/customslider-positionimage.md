---
title: Customslider. positionImage
description: Das positionImage-Attribut gibt die ImageMap an oder ruft Sie ab, um zu bestimmen, welches Positions Bild aus der Bilddatei angezeigt werden soll.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- Windows-Media Player "customslider. positionImage"
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365373"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="e2cdc-104">Customslider. positionImage</span><span class="sxs-lookup"><span data-stu-id="e2cdc-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="e2cdc-105">Das **positionImage** -Attribut gibt die ImageMap an oder ruft Sie ab, um zu bestimmen, welches Positions Bild aus der Bilddatei angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="e2cdc-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e2cdc-106">Possible Values</span></span>

<span data-ttu-id="e2cdc-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2cdc-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2cdc-108">Remarks</span></span>

<span data-ttu-id="e2cdc-109">Dieses Attribut ist erforderlich und muss angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="e2cdc-110">Das **positionImage** wird nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="e2cdc-111">Stattdessen dient sie als Karte, die die durch Klicken aktivierbaren Bereiche des angezeigten Bilds definiert.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="e2cdc-112">Das angezeigte Bild ist eines der untergeordneten Bilder der Bilddatei und stellt den tatsächlichen Zustand des Schiebereglers dar.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="e2cdc-113">Das **positionImage** enthält eine Reihe von grauen Skalierungs Regionen, die der Anzahl dieser untergeordneten Images entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="e2cdc-114">Die untergeordneten Bilder müssen die gleichen Dimensionen wie das **positionImage** aufweisen, oder der benutzerdefinierte Schieberegler funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="e2cdc-115">Alle Regionen, die nicht Graustufen sind, können nicht geklickt werden.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="e2cdc-116">Die durch Klicken aktivierbaren Bereiche sollten auf Farbwerte festgelegt werden, die gleichmäßig über das graue Skalierungs Spektrum reichen, von Schwarz bis weiß, wobei die erste Region rein schwarz und die letzte Region rein weiß ist.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="e2cdc-117">Die Farbwerte für jeden aufeinander folgenden Bereich sollten um einen Wert von 255 (dividiert durch die Gesamtzahl der Regionen minus 1) erhöht werden, wobei auf die nächste ganze Zahl gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="e2cdc-118">Wenn z. b. sechs Regionen vorhanden sind, ist das Inkrement 51 (255 dividiert durch 5), und die sechs Graustufen Werte lauten 0, 51, 102, 153, 204 und 255.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="e2cdc-119">Bei den hexadezimalen Farbwerten für die sechs Regionen handelt es sich dann um \# 000000, \# 333333, \# 666666, \# 999999, \# cccccc und \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="e2cdc-120">Auf diese Weise wird für die Regionen eine Sequenz durch ihre Graustufen Farbwerte vorgegeben, und diese Sequenz entspricht der Sequenz von Unterbildern in der Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="e2cdc-121">Wenn auf eine der Regionen geklickt wird, wird das entsprechende untergeordnete Bild angezeigt, und der **Wert** des benutzerdefinierten Schiebereglers wird entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="e2cdc-122">Die unterstützten Bild Dateitypen sind BMP, JPG, PNG und GIF (keine animierten GIFs).</span><span class="sxs-lookup"><span data-stu-id="e2cdc-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="e2cdc-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e2cdc-123">Examples</span></span>

<span data-ttu-id="e2cdc-124">Im folgenden finden Sie ein Beispiel für ein benutzerdefiniertes **Positions Bild** für den Schieberegler.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="e2cdc-125">Das entsprechende Bild wird im Beispiel Abschnitt der **Image** -Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![Beispiel Grafik für "positionImage"](images/dialmap.png)

<span data-ttu-id="e2cdc-127">Der folgende Code veranschaulicht die Verwendung von **customslider** -Attributen.</span><span class="sxs-lookup"><span data-stu-id="e2cdc-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
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



## <a name="requirements"></a><span data-ttu-id="e2cdc-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2cdc-128">Requirements</span></span>



| <span data-ttu-id="e2cdc-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2cdc-129">Requirement</span></span> | <span data-ttu-id="e2cdc-130">Wert</span><span class="sxs-lookup"><span data-stu-id="e2cdc-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e2cdc-131">Version</span><span class="sxs-lookup"><span data-stu-id="e2cdc-131">Version</span></span><br/> | <span data-ttu-id="e2cdc-132">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e2cdc-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2cdc-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2cdc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cdc-134">**Customslider-Element**</span><span class="sxs-lookup"><span data-stu-id="e2cdc-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="e2cdc-135">**Customslider. Image**</span><span class="sxs-lookup"><span data-stu-id="e2cdc-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





