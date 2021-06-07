---
title: FontControl-Element
description: Stellt ein Schriftartsteuerelement dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente für die Schriftartbearbeitung handelt.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- FontControl-Element Windows-Menüband
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443401"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="8ba7d-104">FontControl-Element</span><span class="sxs-lookup"><span data-stu-id="8ba7d-104">FontControl element</span></span>

<span data-ttu-id="8ba7d-105">Stellt ein [Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente für die Schriftartbearbeitung handelt.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="8ba7d-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="8ba7d-106">Usage</span></span>

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a><span data-ttu-id="8ba7d-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="8ba7d-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ba7d-108">attribute</span><span class="sxs-lookup"><span data-stu-id="8ba7d-108">Attribute</span></span></th>
<th><span data-ttu-id="8ba7d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="8ba7d-109">Type</span></span></th>
<th><span data-ttu-id="8ba7d-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="8ba7d-110">Required</span></span></th>
<th><span data-ttu-id="8ba7d-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ba7d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ba7d-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="8ba7d-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="8ba7d-114">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-114">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-115">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ba7d-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="8ba7d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="8ba7d-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8ba7d-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba7d-120"><strong>FontType</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="8ba7d-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="8ba7d-122">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-122">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-123">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="8ba7d-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="8ba7d-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="8ba7d-126">Das Festlegen des <em>FontType-Attributs</em> auf <code>FontOnly</code> ermöglicht die folgende Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="8ba7d-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="8ba7d-127"><strong>Kombinationsfeld der Schriftfamilie.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="8ba7d-128"><strong>Kombinationsfeld "Schriftgrad".</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="8ba7d-129"><strong>Fette,</strong> <strong>kursiv formatierte,</strong> <strong>unterstrichene</strong>und <strong>durchgestrichene</strong> Umschaltflächen.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-130">Die Umschaltflächen <strong>Durchstreichen</strong> und <strong>Unterstrichen</strong> werden standardmäßig angezeigt, können jedoch ausgeblendet werden, indem sie die Attribute <em>IsStrikethroughButtonVisible</em> und <em>IsUnderlineButtonVisible</em> auf <code>false</code> festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="8ba7d-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="8ba7d-132">Das Festlegen des <em>FontType-Attributs</em> auf <code>FontWithColor</code> ermöglicht die folgende Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="8ba7d-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="8ba7d-133"><strong>Kombinationsfeld der Schriftfamilie.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="8ba7d-134"><strong>Kombinationsfeld "Schriftgrad".</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="8ba7d-135">Schaltflächen <strong>Schriftart</strong> vergrößern und <strong>Schriftgrad verkleinern</strong> inkrementieren und verringern.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="8ba7d-136"><strong>Fette,</strong> <strong>kursiv formatierte,</strong> <strong>unterstrichene</strong>und <strong>durchgestrichene</strong> Umschaltflächen.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-137">Die Umschaltflächen <strong>Durchstreichen</strong> und <strong>Unterstrichen</strong> werden standardmäßig angezeigt, können jedoch ausgeblendet werden, indem sie die Attribute <em>IsStrikethroughButtonVisible</em> und <em>IsUnderlineButtonVisible</em> auf <code>false</code> festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="8ba7d-138"><strong>Farbauswahl für Textfarbe.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="8ba7d-139"><strong>Farbauswahl für Textmarkierung.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-140">Dieses Steuerelement ist standardmäßig ausgeblendet, kann jedoch durch Festlegen des <em>IsHighlightButtonVisible-Attributs</em> auf angezeigt <code>true</code> werden.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="8ba7d-141"><dt><span></span><span></span><strong></strong> (RichFont)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="8ba7d-142">Das Festlegen des <em>FontType-Attributs</em> auf <code>RichFont</code> ermöglicht die folgende Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="8ba7d-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="8ba7d-143"><strong>Kombinationsfeld der Schriftfamilie.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="8ba7d-144"><strong>Kombinationsfeld "Schriftgrad".</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="8ba7d-145">Schaltflächen <strong>Schriftart</strong> vergrößern und <strong>Schriftgrad verkleinern</strong> inkrementieren und verringern.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="8ba7d-146"><strong>Fette,</strong> <strong>kursiv formatierte,</strong> <strong>unterstrichene</strong>und <strong>durchgestrichene</strong> Umschaltflächen.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-147">Die Umschaltflächen <strong>Durchstreichen</strong> und <strong>Unterstrichen</strong> werden standardmäßig angezeigt und können nicht ausgeblendet werden, indem die Attribute <em>IsStrikethroughButtonVisible</em> und <em>IsUnderlineButtonVisible</em> auf festgelegt <code>false</code> werden.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="8ba7d-148"><strong>Farbauswahl für Textfarbe.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="8ba7d-149"><strong>Farbauswahl für Textmarkierung.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-150">Dieses Steuerelement wird standardmäßig angezeigt und kann nicht ausgeblendet werden, indem das <em>IsHighlightButtonVisible-Attribut</em> auf festgelegt <code>false</code> wird.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="8ba7d-151"><strong>Umschaltflächen "Tiefgestellt"</strong> und <strong>"Superscript"</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ba7d-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-153">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="8ba7d-154">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-154">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-155"><strong>Windows 8 und neuer</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="8ba7d-156">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="8ba7d-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-157">Die Schaltflächen Vergrößern/Verkleinern werden nie in der <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="8ba7d-158">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-159">Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontWithColor</code> oder <code>RichFont</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="8ba7d-160"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-161">Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba7d-162"><strong>IsHighlightButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-163">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="8ba7d-164">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-164">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-165">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="8ba7d-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-166">Die Farbhervorhebung ist nur über <strong>ein FontControl</strong> verfügbar, wenn der Wert des <em>FontType-Attributs</em> <code>FontWithColor</code> gleich oder <code>RichFont</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="8ba7d-167">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-168">Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontWithColor</code> oder <code>RichFont</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="8ba7d-169">Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontWithColor</code> oder <code>RichFont</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="8ba7d-170"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-171">Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="8ba7d-172">Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> oder <code>FontWithColor</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ba7d-173"><strong>IsStrikethroughButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-174">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="8ba7d-175">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-175">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-176">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="8ba7d-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="8ba7d-177">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-178">Standard.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-178">Default.</span></span> <br/> </dd> <span data-ttu-id="8ba7d-179"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-180">Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> oder <code>FontWithColor</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba7d-181"><strong>IsUnderlineButtonVisible</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-182">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="8ba7d-183">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-183">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-184">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="8ba7d-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="8ba7d-185">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-186">Standard.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-186">Default.</span></span> <br/> </dd> <span data-ttu-id="8ba7d-187"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-188">Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> oder <code>FontWithColor</code> ist.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ba7d-189"><strong>MaximumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="8ba7d-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="8ba7d-191">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-191">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-192">Die maximale anzuzeigende Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="8ba7d-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-194">Ein ganzzahliger Wert zwischen 1 und 9999 einschließlich.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="8ba7d-195">Der Standardwert ist <strong>9999.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba7d-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="8ba7d-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="8ba7d-198">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-198">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-199">Die minimale anzuzeigende Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="8ba7d-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-201">Ein ganzzahliger Wert zwischen 1 und 9999 einschließlich .</span><span class="sxs-lookup"><span data-stu-id="8ba7d-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="8ba7d-202">Der Standardwert ist <strong>1.</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ba7d-203"><strong>ShowTrueTypeOnly</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-204">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="8ba7d-205">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-205">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-206">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="8ba7d-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="8ba7d-207">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-208">Zeigt nur TrueType- und OpenType-Schriftarten an.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="8ba7d-209"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-210">Standard.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-210">Default.</span></span> <span data-ttu-id="8ba7d-211">Es wird keine Einschränkung für den Typ der angezeigten Schriftarten platziert.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ba7d-212"><strong>ShowVerticalFonts</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7d-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="8ba7d-213">Boolesch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="8ba7d-214">Nein</span><span class="sxs-lookup"><span data-stu-id="8ba7d-214">No</span></span><br/></td>
<td><span data-ttu-id="8ba7d-215">Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="8ba7d-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-216">Vertikalen Schriftarten wird in der Liste Schriftfamilie ein <strong>@-Symbol</strong> vorangehende.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="8ba7d-217">
<dt><span></span><span></span><strong></strong> (true)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-218">Standard.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-218">Default.</span></span> <span data-ttu-id="8ba7d-219">Zeigt die vertikalen Schriftarten an, die in <strong>der</strong> Systemsteuerung <strong>Schriftarten</strong> auf Anzeigen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="8ba7d-220"><dt><span></span><span></span><strong></strong> (false)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="8ba7d-221">Ermöglicht einer Anwendung, die keinen vertikalen Text unterstützt, alle vertikalen Schriftarten auszublenden, die <strong>in</strong> der Systemsteuerung <strong>Schriftarten</strong> auf Anzeigen festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="8ba7d-222">In Windows Vista bietet die <strong>Systemsteuerung</strong> Schriftarten keine Funktionen zum <strong>Ein-</strong> <strong>oder</strong> Ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="8ba7d-223">In diesem Fall muss das <em>ShowVerticalFonts-Attribut</em> auf festgelegt <code>False</code> werden.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8ba7d-224">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba7d-224">Child elements</span></span>

<span data-ttu-id="8ba7d-225">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="8ba7d-226">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8ba7d-226">Parent elements</span></span>



| <span data-ttu-id="8ba7d-227">Element</span><span class="sxs-lookup"><span data-stu-id="8ba7d-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="8ba7d-228">**ControlGroup**</span><span class="sxs-lookup"><span data-stu-id="8ba7d-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="8ba7d-229">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="8ba7d-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="8ba7d-230">**Menugroup**</span><span class="sxs-lookup"><span data-stu-id="8ba7d-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="8ba7d-231">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ba7d-231">Remarks</span></span>

<span data-ttu-id="8ba7d-232">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-232">Optional.</span></span>

<span data-ttu-id="8ba7d-233">Kann für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**Group- oder**](windowsribbon-element-group.md) [**MenuGroup-Element mindestens einmal**](windowsribbon-element-menugroup.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="8ba7d-234">Alle **im Markup deklarierten FontControl-Befehlsattribute,** z.B. [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) oder [**Command.TooltipTitle,**](windowsribbon-element-command-tooltiptitle.md)werden durch die Attribute der einzelnen Steuerelemente überschrieben, aus denen **fontControl besteht.**</span><span class="sxs-lookup"><span data-stu-id="8ba7d-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="8ba7d-235">Jeder Versuch, ein Farbmuster aus der Farbauswahl eines Schriftartsteuerfelds auszuwählen, kann zu einer Zugriffsverletzung führen, wenn dem Steuerelement kein Befehlshandler zugeordnet ist. [](windowsribbon-controls-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="8ba7d-236">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ba7d-236">Examples</span></span>

<span data-ttu-id="8ba7d-237">Im folgenden Beispiel wird das grundlegende Markup für die drei Typen von [Font Control veranschaulicht.](windowsribbon-controls-fontcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="8ba7d-238">Dieser Codeabschnitt zeigt die **Deklarationen des FontControl-Befehls** mit jeweils einer [**Gruppencontainerdeklaration.**](windowsribbon-element-group.md)</span><span class="sxs-lookup"><span data-stu-id="8ba7d-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



<span data-ttu-id="8ba7d-239">Dieser Codeabschnitt zeigt die **Deklarationen des** FontControl-Steuerelements, bei denen **jedes FontControl** und [**jede Gruppe**](windowsribbon-element-group.md) auf einer einzelnen Registerkarte deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="8ba7d-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a><span data-ttu-id="8ba7d-240">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="8ba7d-240">Element information</span></span>

* <span data-ttu-id="8ba7d-241">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ba7d-241">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="8ba7d-242">**Kann leer sein:** Ja</span><span class="sxs-lookup"><span data-stu-id="8ba7d-242">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="8ba7d-243">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ba7d-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba7d-244">Steuerelement "Schriftart"</span><span class="sxs-lookup"><span data-stu-id="8ba7d-244">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="8ba7d-245">Eigenschaften des Schriftartsteuersteuer steuerelements</span><span class="sxs-lookup"><span data-stu-id="8ba7d-245">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="8ba7d-246">FontControl-Beispiel</span><span class="sxs-lookup"><span data-stu-id="8ba7d-246">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





