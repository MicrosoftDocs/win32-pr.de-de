---
title: Command. KeyTip (Eigenschaft)
description: Stellt den KeyTip für ein-Steuerelement dar.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Command. KeyTip-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343049"
---
# <a name="commandkeytip-property"></a><span data-ttu-id="df351-104">Command. KeyTip (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="df351-104">Command.Keytip property</span></span>

<span data-ttu-id="df351-105">Stellt den KeyTip für ein-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="df351-105">Represents the keytip for a control.</span></span>

## <a name="usage"></a><span data-ttu-id="df351-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="df351-106">Usage</span></span>

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a><span data-ttu-id="df351-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="df351-107">Attributes</span></span>

<span data-ttu-id="df351-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="df351-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="df351-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df351-109">Child elements</span></span>



| <span data-ttu-id="df351-110">Element</span><span class="sxs-lookup"><span data-stu-id="df351-110">Element</span></span>                                                   | <span data-ttu-id="df351-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df351-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="df351-112">**Schnür**</span><span class="sxs-lookup"><span data-stu-id="df351-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="df351-113">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="df351-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="df351-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df351-114">Parent elements</span></span>



| <span data-ttu-id="df351-115">Element</span><span class="sxs-lookup"><span data-stu-id="df351-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="df351-116">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="df351-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="df351-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df351-117">Remarks</span></span>

<span data-ttu-id="df351-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="df351-118">Optional.</span></span>

<span data-ttu-id="df351-119">Kann höchstens einmal für jedes [**Befehls**](windowsribbon-element-command.md) Element auftreten.</span><span class="sxs-lookup"><span data-stu-id="df351-119">May occur at most once for each [**Command**](windowsribbon-element-command.md) element.</span></span>

<span data-ttu-id="df351-120">**Command. KeyTip** kann einen Wert vom Typ *xs: String* enthalten, der auf eine beliebige Unicode-Zeichenfolge (einschließlich Leerzeichen) beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="df351-120">**Command.Keytip** can contain a value of type *xs:string* constrained to any sequence of Unicode characters, including white space.</span></span>

<span data-ttu-id="df351-121">Eine " **Command. KeyTip** " kann nur mit einer Zahl beginnen, wenn Sie einem Steuerelement in einer [Registerkarte](windowsribbon-controls-tab.md) oder der [Symbolleiste für den schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="df351-121">A **Command.Keytip** can begin with a number only when associated with a control within a [Tab](windowsribbon-controls-tab.md) or the [Quick Access Toolbar](windowsribbon-controls-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="df351-122">Drücken Sie die Alt-Taste, um die KeyTips anzuzeigen, die für den aktuellen Status des Menübands gültig sind.</span><span class="sxs-lookup"><span data-stu-id="df351-122">To display the keytips that are valid for the current state of the ribbon, press and hold the ALT key.</span></span> <span data-ttu-id="df351-123">Der folgende Screenshot zeigt die Ausgangs-oder erste Ebene der KeyTips, die in Microsoft Paint für Windows 7 angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="df351-123">The following screen shot shows the initial, or first level, keytips that are displayed in Microsoft Paint for Windows 7.</span></span> <span data-ttu-id="df351-124">Nachdem Sie einen KeyTip der ersten Ebene ausgewählt haben, werden nur KeyTips der zweiten Ebene angezeigt.</span><span class="sxs-lookup"><span data-stu-id="df351-124">After a first-level keytip has been selected, only second-level keytips are displayed.</span></span>

![KeyTips der ersten Ebene in Microsoft Paint für Windows 7](images/properties/ui-pkey-label-keytips.png)

<span data-ttu-id="df351-126">**Command. KeyTip** fungiert als Tastaturbeschleuniger für einen Befehl, es sei denn, dieser Befehl wird über ein Menü Element verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="df351-126">**Command.Keytip** acts as the keyboard accelerator for a command unless that command is exposed through a menu item.</span></span> <span data-ttu-id="df351-127">In diesem Fall ignoriert das Framework den **Command. KeyTip** -Wert und verwendet stattdessen ein Zeichen, dem ein kaufmännisches und-Zeichen vorangestellt ist, wie durch [**Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [UI \_ pkey- \_ Bezeichnung](windowsribbon-reference-properties-uipkey-label.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="df351-127">In this case, the framework ignores the **Command.Keytip** value and instead uses a character preceded by an ampersand as specified by [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="df351-128">Wenn kein kaufmännisches und von der Bezeichnung " **Command. labeltitle** " oder "UI pkey" angegeben wird \_ \_ , wird kein KeyTip oder keine Tastatur Beschleunigung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="df351-128">If no ampersand is specified by **Command.LabelTitle** or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

<span data-ttu-id="df351-129">Wenn für **Command. KeyTip** kein Wert angegeben wird, ist das untergeordnete [**Zeichen**](windowsribbon-element-string.md) folgen Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="df351-129">If no value is supplied for **Command.Keytip**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="df351-130">Wenn **Command. KeyTip** sowohl einen Wert als auch ein untergeordnetes [**Zeichen**](windowsribbon-element-string.md) folgen Element enthält, hat die **Zeichenfolge** Vorrang.</span><span class="sxs-lookup"><span data-stu-id="df351-130">If **Command.Keytip** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="df351-131">Standardmäßig werden die folgenden Buchstaben vom Framework verwendet, um KeyTips automatisch zu generieren:</span><span class="sxs-lookup"><span data-stu-id="df351-131">By default, the following letters are used by the framework to automatically generate keytips:</span></span>

-   <span data-ttu-id="df351-132">**F** wird dem [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="df351-132">**F** is assigned to the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>
-   <span data-ttu-id="df351-133">**Y** wird einem Befehl zugewiesen, der keinen KeyTip hat, der von der Anwendung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="df351-133">**Y** is assigned to any command that does not have a keytip specified by the application.</span></span>
-   <span data-ttu-id="df351-134">**Z** wird jedem [Gruppen](windowsribbon-controls-group.md) Steuerelement zugewiesen und kann nicht angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="df351-134">**Z** is assigned to each [Group](windowsribbon-controls-group.md) control and cannot be customized.</span></span> <span data-ttu-id="df351-135">Ein gruppenkeytip wird nur angezeigt, wenn die [**scalingpolicy**](windowsribbon-element-scalingpolicy.md) für das-Steuerelement eine **Popup** Größen Option angibt.</span><span class="sxs-lookup"><span data-stu-id="df351-135">A Group keytip is displayed only when the [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) for the control specifies a **Popup** size option.</span></span> <span data-ttu-id="df351-136">Weitere Informationen finden Sie unter [Anpassen eines Menübands durch Größen Definitionen und Skalierungs Richtlinien](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="df351-136">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

> [!Note]  
> <span data-ttu-id="df351-137">Keiner dieser Buchstaben wird vom Framework reserviert.</span><span class="sxs-lookup"><span data-stu-id="df351-137">None of these letters are reserved by the framework.</span></span> <span data-ttu-id="df351-138">Jeder kann einem oder mehreren Befehlen nach Bedarf zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="df351-138">Each can be assigned to one or more commands as required.</span></span>

 

<span data-ttu-id="df351-139">Das Framework löst KeyTip-Konflikte wie folgt auf:</span><span class="sxs-lookup"><span data-stu-id="df351-139">The framework resolves keytip conflicts in the following ways:</span></span>

-   <span data-ttu-id="df351-140">Wenn ein oder mehrere [Register](windowsribbon-controls-tab.md) Karten-Steuerelemente demselben KeyTip zugeordnet sind, wird eine Zahl an jeden KeyTip angehängt, beginnend bei 1 und erhöht sequenziell (2, 3,...) für jedes Steuerelement in der Reihenfolge der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="df351-140">If one or more [Tab](windowsribbon-controls-tab.md) controls are associated with the same keytip, a number is appended to each keytip, starting at 1, and increasing sequentially (2, 3,...) for each control in the order of declaration.</span></span> <span data-ttu-id="df351-141">Wenn einem Tabstopp Steuerelement der Buchstabe F als KeyTip zugewiesen ist, wird dem [Anwendungsmenü](windowsribbon-controls-applicationmenu.md) F1 mit den restlichen KeyTips zugewiesen, wie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df351-141">If any Tab controls are assigned the letter F as a keytip, the [Application Menu](windowsribbon-controls-applicationmenu.md) is assigned F1 with the remaining keytips adjusted as described.</span></span>
-   <span data-ttu-id="df351-142">Wenn ein einzelnes Steuerelement innerhalb einer [Registerkarte](windowsribbon-controls-tab.md)zugeordnet ist, ist der KeyTip F sowohl für das Steuerelement als auch für das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)gültig.</span><span class="sxs-lookup"><span data-stu-id="df351-142">When associated with a single control within a [Tab](windowsribbon-controls-tab.md), the keytip F is valid for both the control and the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="df351-143">Der standardmäßige Anwendungsmenü-KeyTip wird nicht geändert, aber dem Steuerelement auf der aktiven Registerkarte wird eine Rangfolge zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="df351-143">The default Application Menu keytip is not changed, but precedence is given to the control on the active tab.</span></span>
-   <span data-ttu-id="df351-144">Wenn ein oder mehrere Steuerelemente innerhalb einer [Registerkarte](windowsribbon-controls-tab.md) demselben KeyTip zugeordnet sind, werden die KeyTips dieser Steuerelemente vom Framework automatisch neu erstellt, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="df351-144">If one or more controls within a [Tab](windowsribbon-controls-tab.md) are associated with the same keytip, the framework automatically refactors the keytips of those controls, as described previously.</span></span>

> [!Note]  
> <span data-ttu-id="df351-145">Eine geringfügige Variation der Textfarbe wird verwendet, um umgestaltete KeyTips in einer Standard-Multifunktionsleisten-Implementierung hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="df351-145">A slight variation in text color is used to highlight refactored keytips in a standard ribbon implementation.</span></span> <span data-ttu-id="df351-146">Bei einer nicht standardmäßigen Multifunktionsleisten-Implementierung, bei der die Multifunktionsleisten Farbe angepasst wurde, wird dieses frameworkverhalten außer Kraft gesetzt, und alle KeyTips werden mit der gleichen Textfarbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="df351-146">For a nonstandard ribbon implementation where the ribbon color has been customized, this framework behavior is overridden and all keytips are displayed with the same text color.</span></span> <span data-ttu-id="df351-147">Weitere Informationen finden Sie unter [Anpassen von Menüband-Farben](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="df351-147">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>

 

<span data-ttu-id="df351-148">Die maximale Länge ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="df351-148">The maximum length is unbounded.</span></span>

## <a name="examples"></a><span data-ttu-id="df351-149">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df351-149">Examples</span></span>

<span data-ttu-id="df351-150">Im folgenden Beispiel wird das Markup für ein [**Command**](windowsribbon-element-command.md) -Element mit der **Command. KeyTip** -Deklaration veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="df351-150">The following example demonstrates the markup for a [**Command**](windowsribbon-element-command.md) element with a **Command.Keytip** declaration.</span></span>


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="df351-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df351-151">Requirements</span></span>



| <span data-ttu-id="df351-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df351-152">Requirement</span></span> | <span data-ttu-id="df351-153">Wert</span><span class="sxs-lookup"><span data-stu-id="df351-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="df351-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df351-154">Minimum supported client</span></span><br/> | <span data-ttu-id="df351-155">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df351-155">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="df351-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df351-156">Minimum supported server</span></span><br/> | <span data-ttu-id="df351-157">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df351-157">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df351-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df351-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df351-159">UI- \_ pkey- \_ KeyTip</span><span class="sxs-lookup"><span data-stu-id="df351-159">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





