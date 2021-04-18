---
title: Text. Value
description: Das value-Attribut gibt den Text an, der im Text Steuerelement angezeigt wird, oder ruft ihn ab.
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- Text. Value-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368504"
---
# <a name="textvalue"></a><span data-ttu-id="84324-104">Text. Value</span><span class="sxs-lookup"><span data-stu-id="84324-104">TEXT.value</span></span>

<span data-ttu-id="84324-105">Das **value** -Attribut gibt den Text an, der im Text Steuerelement angezeigt wird, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="84324-105">The **value** attribute specifies or retrieves the text that is displayed in the Text control.</span></span>

``` syntax
        elementID.value
```

## <a name="possible-values"></a><span data-ttu-id="84324-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="84324-106">Possible Values</span></span>

<span data-ttu-id="84324-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="84324-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="84324-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84324-108">Remarks</span></span>

<span data-ttu-id="84324-109">Wenn die Breite des Text-Steuer Elements unzureichend ist, um den bereitgestellten Text zu enthalten, wird der Text abgeschnitten, und es wird ein Auslassungs Zeichen angezeigt, um die Tatsache zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="84324-109">If the width of the Text control is insufficient to contain the text provided, the text is cropped, and an ellipsis is shown to illustrate the fact.</span></span> <span data-ttu-id="84324-110">Wenn das **ToolTip** -Attribut nicht festgelegt wurde, wird der vollständige Text dann als QuickInfo angezeigt, wenn der Cursor über das Steuerelement bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="84324-110">If the **toolTip** attribute has not been set, the complete text will then appear as a ToolTip when the cursor hovers over the control.</span></span>

<span data-ttu-id="84324-111">Wenn keine Breite angegeben ist, ist die Standardbreite für das-Steuerelement die Breite der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="84324-111">If a width is not specified, the default width for the control is the width of the string.</span></span>

<span data-ttu-id="84324-112">Wenn die Höhe des Steuer Elements nicht angegeben wird, ist die Standardhöhe eine Zeile.</span><span class="sxs-lookup"><span data-stu-id="84324-112">If the height of the control is not specified, the default height is one line.</span></span>

<span data-ttu-id="84324-113">Wenn das **WordWrap** -Attribut auf "true" festgelegt ist und die Höhe des Steuer Elements ausreichend ist, um eine andere Textzeile aufnehmen zu können, wird der Text in eine nachfolgende Zeile umschlossen.</span><span class="sxs-lookup"><span data-stu-id="84324-113">If the **wordWrap** attribute is set to true and the height of the control is enough to accommodate another line of text, the text wraps to a subsequent line.</span></span> <span data-ttu-id="84324-114">Das umwickeln erfolgt nur zwischen Wörtern.</span><span class="sxs-lookup"><span data-stu-id="84324-114">Wrapping only occurs between words.</span></span> <span data-ttu-id="84324-115">Zeilenumbrüche können auch erzwungen werden, wie unter **WordWrap** erläutert.</span><span class="sxs-lookup"><span data-stu-id="84324-115">Line breaks may also be forced, as explained under **wordWrap**.</span></span>

## <a name="examples"></a><span data-ttu-id="84324-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84324-116">Examples</span></span>

<span data-ttu-id="84324-117">Das folgende Beispiel ist eine vollständige Skin-Definitionsdatei, die veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84324-117">The following sample is a complete skin definition file that illustrates how the attributes of the **TEXT** element are used.</span></span> <span data-ttu-id="84324-118">Sie befindet sich im Verzeichnis Samples, das mit dem SDK installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="84324-118">It can be found in the Samples directory that was installed with the SDK.</span></span>


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="84324-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84324-119">Requirements</span></span>



| <span data-ttu-id="84324-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84324-120">Requirement</span></span> | <span data-ttu-id="84324-121">Wert</span><span class="sxs-lookup"><span data-stu-id="84324-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="84324-122">Version</span><span class="sxs-lookup"><span data-stu-id="84324-122">Version</span></span><br/> | <span data-ttu-id="84324-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="84324-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84324-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84324-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84324-125">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="84324-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="84324-126">**Text. ToolTip**</span><span class="sxs-lookup"><span data-stu-id="84324-126">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="84324-127">**Text. WordWrap**</span><span class="sxs-lookup"><span data-stu-id="84324-127">**TEXT.wordWrap**</span></span>](text-wordwrap.md)
</dt> </dl>

 

 





