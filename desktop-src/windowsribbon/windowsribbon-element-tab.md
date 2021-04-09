---
title: Registerkartenelement
description: Stellt eine zentrale oder kontextabhängige Registerkarte dar.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Registerkarten Element Windows-Menüband
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e54abc7e13906ada69c1e10f81878c77c4bf5d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039391"
---
# <a name="tab-element"></a><span data-ttu-id="c6db7-104">Registerkartenelement</span><span class="sxs-lookup"><span data-stu-id="c6db7-104">Tab element</span></span>

<span data-ttu-id="c6db7-105">Stellt eine [zentrale](windowsribbon-controls-tab.md) oder [kontextabhängige](windowsribbon-controls-tabgroup.md) Registerkarte dar.</span><span class="sxs-lookup"><span data-stu-id="c6db7-105">Represents a [core](windowsribbon-controls-tab.md) or [contextual](windowsribbon-controls-tabgroup.md) tab.</span></span>

## <a name="usage"></a><span data-ttu-id="c6db7-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="c6db7-106">Usage</span></span>

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a><span data-ttu-id="c6db7-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="c6db7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c6db7-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="c6db7-108">Attribute</span></span></th>
<th><span data-ttu-id="c6db7-109">type</span><span class="sxs-lookup"><span data-stu-id="c6db7-109">Type</span></span></th>
<th><span data-ttu-id="c6db7-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6db7-110">Required</span></span></th>
<th><span data-ttu-id="c6db7-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6db7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c6db7-112"><strong>Applicationmodes</strong></span><span class="sxs-lookup"><span data-stu-id="c6db7-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="c6db7-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="c6db7-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="c6db7-114">Nein</span><span class="sxs-lookup"><span data-stu-id="c6db7-114">No</span></span><br/></td>
<td><span data-ttu-id="c6db7-115">Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.</span><span class="sxs-lookup"><span data-stu-id="c6db7-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="c6db7-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="c6db7-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c6db7-117">Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.</span><span class="sxs-lookup"><span data-stu-id="c6db7-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="c6db7-118">Leerraum ist gültig und wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="c6db7-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="c6db7-119">Maximale Länge: 250 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c6db7-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c6db7-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="c6db7-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="c6db7-121">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="c6db7-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c6db7-122">Nein</span><span class="sxs-lookup"><span data-stu-id="c6db7-122">No</span></span><br/></td>
<td><span data-ttu-id="c6db7-123">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="c6db7-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="c6db7-124">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="c6db7-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c6db7-125">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="c6db7-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="c6db7-126">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="c6db7-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c6db7-127">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="c6db7-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c6db7-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6db7-128">Child elements</span></span>



| <span data-ttu-id="c6db7-129">Element</span><span class="sxs-lookup"><span data-stu-id="c6db7-129">Element</span></span>                                                                         | <span data-ttu-id="c6db7-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6db7-130">Description</span></span>                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c6db7-131">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="c6db7-131">**Group**</span></span>](windowsribbon-element-group.md)<br/>                         | <span data-ttu-id="c6db7-132">Kann ein-oder mehrmals vorkommen</span><span class="sxs-lookup"><span data-stu-id="c6db7-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="c6db7-133">**Tab. scalingpolicy**</span><span class="sxs-lookup"><span data-stu-id="c6db7-133">**Tab.ScalingPolicy**</span></span>](windowsribbon-element-tab-scalingpolicy.md)<br/> | <span data-ttu-id="c6db7-134">Kann höchstens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="c6db7-134">May occur at most once</span></span><br/> <br/>      |



## <a name="parent-elements"></a><span data-ttu-id="c6db7-135">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6db7-135">Parent elements</span></span>



| <span data-ttu-id="c6db7-136">Element</span><span class="sxs-lookup"><span data-stu-id="c6db7-136">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="c6db7-137">**Menüband. Registerkarten**</span><span class="sxs-lookup"><span data-stu-id="c6db7-137">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/> |
| [<span data-ttu-id="c6db7-138">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="c6db7-138">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="c6db7-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6db7-139">Remarks</span></span>

<span data-ttu-id="c6db7-140">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c6db7-140">Required.</span></span>

<span data-ttu-id="c6db7-141">Muss mindestens einmal für jedes [**Ribbon. Tabs**](windowsribbon-element-ribbon-tabs.md) -oder [**TabGroup**](windowsribbon-element-tabgroup.md) -Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="c6db7-141">Must occur at least once for each [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md) or [**TabGroup**](windowsribbon-element-tabgroup.md) element.</span></span>

<span data-ttu-id="c6db7-142">**Registerkarte** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="c6db7-142">**Tab** supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="c6db7-143">Wenn [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) für das **Tab** -Element vorhanden ist, wird ein Eintrag für jedes [**Group**](windowsribbon-element-group.md) -Element und seine ideale Größe unter **scalingpolicy. idealsizes** benötigt.</span><span class="sxs-lookup"><span data-stu-id="c6db7-143">If [**ScalingPolicy.IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) is present for the **Tab** element, then an entry for each [**Group**](windowsribbon-element-group.md) element and its ideal size is required under **ScalingPolicy.IdealSizes**.</span></span>

## <a name="examples"></a><span data-ttu-id="c6db7-144">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6db7-144">Examples</span></span>

<span data-ttu-id="c6db7-145">Im folgenden Beispiel wird das grundlegende Markup für das **Register** Karten-Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c6db7-145">The following example demonstrates the basic markup for the **Tab** element.</span></span>

<span data-ttu-id="c6db7-146">In diesem Code Abschnitt werden die **Register** Karten Befehls Deklarationen für eine Registerkarte **Home** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c6db7-146">This section of code shows the **Tab** Command declarations for a **Home** tab.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



<span data-ttu-id="c6db7-147">In diesem Code Abschnitt werden die Deklarationen des **Register** Steuer Elements dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c6db7-147">This section of code shows the **Tab** control declarations.</span></span>


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a><span data-ttu-id="c6db7-148">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c6db7-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="c6db7-149">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="c6db7-149">Minimum supported system</span></span><br/> | <span data-ttu-id="c6db7-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6db7-150">Windows 7</span></span> |
| <span data-ttu-id="c6db7-151">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="c6db7-151">Can be empty</span></span>                        | <span data-ttu-id="c6db7-152">Nein</span><span class="sxs-lookup"><span data-stu-id="c6db7-152">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="c6db7-153">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c6db7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6db7-154">Registersteuerelement</span><span class="sxs-lookup"><span data-stu-id="c6db7-154">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> <dt>

[<span data-ttu-id="c6db7-155">Registerkarten-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c6db7-155">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="c6db7-156">**Setmodes**</span><span class="sxs-lookup"><span data-stu-id="c6db7-156">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

