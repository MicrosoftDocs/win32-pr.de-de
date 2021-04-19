---
title: Text. WordWrap
description: Mit dem WordWrap-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Zeilenumbruch aktiviert oder deaktiviert ist.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Text. WordWrap-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372688"
---
# <a name="textwordwrap"></a><span data-ttu-id="7c727-104">Text. WordWrap</span><span class="sxs-lookup"><span data-stu-id="7c727-104">TEXT.wordWrap</span></span>

<span data-ttu-id="7c727-105">Mit dem **WordWrap** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob der Zeilenumbruch aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7c727-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="7c727-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7c727-106">Possible Values</span></span>

<span data-ttu-id="7c727-107">Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7c727-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7c727-108">Wert</span><span class="sxs-lookup"><span data-stu-id="7c727-108">Value</span></span> | <span data-ttu-id="7c727-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c727-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c727-110">true</span><span class="sxs-lookup"><span data-stu-id="7c727-110">true</span></span>  | <span data-ttu-id="7c727-111">Der Zeilenumbruch ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7c727-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="7c727-112">false</span><span class="sxs-lookup"><span data-stu-id="7c727-112">false</span></span> | <span data-ttu-id="7c727-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="7c727-113">Default.</span></span> <span data-ttu-id="7c727-114">Der Zeilenumbruch ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7c727-114">Word wrap is disabled.</span></span> <span data-ttu-id="7c727-115">Wenn der Text nicht in das Steuerelement passt, wird der Text abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="7c727-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7c727-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c727-116">Remarks</span></span>

<span data-ttu-id="7c727-117">Das Text Steuerelement teilt Wörter nicht voneinander ab.</span><span class="sxs-lookup"><span data-stu-id="7c727-117">The Text control does not split words apart.</span></span> <span data-ttu-id="7c727-118">Wenn ein Wort über die Breite des Steuer Elements hinausgeht, wird das Wort Wrap verwendet, um das Wort in die nächste Zeile zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="7c727-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="7c727-119">Wenn ein einzelnes Wort länger als die Steuerelement Breite ist, wird dieses Wort abgeschnitten und belegt eine einzelne Zeile.</span><span class="sxs-lookup"><span data-stu-id="7c727-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="7c727-120">Wenn das **Width** -Attribut nicht angegeben wird, wird **WordWrap** ignoriert, und die Größe des Text Steuer Elements wird geändert, anstatt den Text zu umschließen.</span><span class="sxs-lookup"><span data-stu-id="7c727-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="7c727-121">Wenn an bestimmten Orten Zeilenumbrüche gewünscht werden, müssen Sie explizit mit "  &\# 13;" oder "r" in einem Wert angegeben werden \\ .</span><span class="sxs-lookup"><span data-stu-id="7c727-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="7c727-122">Wenn das letztere Formular verwendet wird, wenn der Wert direkt angegeben wird, muss der Zeichenfolge "JScript:" vorangestellt werden, und der tatsächliche Wert muss in einfache Anführungszeichen eingeschlossen werden, wie unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7c727-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="7c727-123">Dies ist nicht erforderlich, wenn der Wert innerhalb eines Ereignis Handlers dynamisch festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="7c727-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="7c727-124">Wenn **WordWrap** auf true festgelegt ist **und die** QuickInfo nicht angegeben ist, wird in der QuickInfo der vollständige Text des **value** -Attributs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c727-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="7c727-125">Wenn keine QuickInfo erwünscht ist, **legen Sie** die QuickInfo auf "" (leere Zeichenfolge) fest.</span><span class="sxs-lookup"><span data-stu-id="7c727-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="7c727-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c727-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="7c727-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c727-127">Requirements</span></span>



| <span data-ttu-id="7c727-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c727-128">Requirement</span></span> | <span data-ttu-id="7c727-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7c727-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7c727-130">Version</span><span class="sxs-lookup"><span data-stu-id="7c727-130">Version</span></span><br/> | <span data-ttu-id="7c727-131">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="7c727-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7c727-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c727-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c727-133">**Ambientattribute. Width**</span><span class="sxs-lookup"><span data-stu-id="7c727-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="7c727-134">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="7c727-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="7c727-135">**Text. ToolTip**</span><span class="sxs-lookup"><span data-stu-id="7c727-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="7c727-136">**Text. Value**</span><span class="sxs-lookup"><span data-stu-id="7c727-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





