---
title: FontControl-Element
description: Stellt ein Schriftart Steuerelement dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente handelt, die für die Schriftart Bearbeitung
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
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2020
ms.locfileid: "104390115"
---
# <a name="fontcontrol-element"></a><span data-ttu-id="841e8-104">FontControl-Element</span><span class="sxs-lookup"><span data-stu-id="841e8-104">FontControl element</span></span>

<span data-ttu-id="841e8-105">Stellt ein [Schriftart Steuer](windowsribbon-controls-fontcontrol.md)Element dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente handelt, die für die Schriftart Bearbeitung</span><span class="sxs-lookup"><span data-stu-id="841e8-105">Represents a [Font Control](windowsribbon-controls-fontcontrol.md), which is a specialized container of individual controls dedicated to font manipulation.</span></span>

## <a name="usage"></a><span data-ttu-id="841e8-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="841e8-106">Usage</span></span>

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

## <a name="attributes"></a><span data-ttu-id="841e8-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="841e8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="841e8-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="841e8-108">Attribute</span></span></th>
<th><span data-ttu-id="841e8-109">type</span><span class="sxs-lookup"><span data-stu-id="841e8-109">Type</span></span></th>
<th><span data-ttu-id="841e8-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="841e8-110">Required</span></span></th>
<th><span data-ttu-id="841e8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="841e8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="841e8-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="841e8-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="841e8-114">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-114">No</span></span><br/></td>
<td><span data-ttu-id="841e8-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="841e8-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="841e8-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="841e8-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="841e8-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="841e8-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="841e8-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="841e8-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="841e8-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="841e8-120"><strong>Fonttype</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-120"><strong>FontType</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="841e8-121">xs:string</span></span><br/></td>
<td><span data-ttu-id="841e8-122">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-122">No</span></span><br/></td>
<td><span data-ttu-id="841e8-123">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="841e8-123">Restricted to one of the following values:</span></span> <br/> <br/><span data-ttu-id="841e8-124">
<dt><span></span><span></span><strong></strong> (Fontonly)</span><span class="sxs-lookup"><span data-stu-id="841e8-124">
<dt><span></span><span></span><strong></strong> (FontOnly)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-125">Standard.</span><span class="sxs-lookup"><span data-stu-id="841e8-125">Default.</span></span> <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> <span data-ttu-id="841e8-126">Durch Festlegen des Attributs " <em>fonttype</em> " auf werden <code>FontOnly</code> die folgenden Funktionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="841e8-126">Setting the <em>FontType</em> attribute to <code>FontOnly</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="841e8-127">Kombinations Feld " <strong>Schriftfamilie</strong> ".</span><span class="sxs-lookup"><span data-stu-id="841e8-127"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="841e8-128">Kombinations Feld " <strong>Schriftgröße</strong> ".</span><span class="sxs-lookup"><span data-stu-id="841e8-128"><strong>Font Size</strong> combo box.</span></span></li>
<li><p><span data-ttu-id="841e8-129">Die UMSCHALT Flächen <strong>Fett</strong>, <strong>kursiv</strong>, unter <strong>Strichen</strong>und <strong>durch</strong> gestrichen.</span><span class="sxs-lookup"><span data-stu-id="841e8-129"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-130">Die UMSCHALT Flächen " <strong>durch</strong> gestrichen" und "unter <strong>streichen</strong> " werden standardmäßig angezeigt. Sie können jedoch ausgeblendet werden, indem Sie die Attribute " <em>isstrikeflowbuttonvisible</em> " und " <em>isunderlinebuttonvisible</em> " auf festlegen <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-130">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="841e8-131"><dt><span></span><span></span><strong></strong> (Fontwithcolor)</span><span class="sxs-lookup"><span data-stu-id="841e8-131"><dt><span></span><span></span><strong></strong> (FontWithColor)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> <span data-ttu-id="841e8-132">Durch Festlegen des Attributs " <em>fonttype</em> " auf werden <code>FontWithColor</code> die folgenden Funktionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="841e8-132">Setting the <em>FontType</em> attribute to <code>FontWithColor</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="841e8-133">Kombinations Feld " <strong>Schriftfamilie</strong> ".</span><span class="sxs-lookup"><span data-stu-id="841e8-133"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="841e8-134">Kombinations Feld " <strong>Schriftgröße</strong> ".</span><span class="sxs-lookup"><span data-stu-id="841e8-134"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="841e8-135"><strong>Vergrößern Sie Schriftart</strong> , und <strong>verkleinern</strong> Sie die Schriftart für die Schriftgröße und die Dekrement-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="841e8-135"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="841e8-136">Die UMSCHALT Flächen <strong>Fett</strong>, <strong>kursiv</strong>, unter <strong>Strichen</strong>und <strong>durch</strong> gestrichen.</span><span class="sxs-lookup"><span data-stu-id="841e8-136"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-137">Die UMSCHALT Flächen " <strong>durch</strong> gestrichen" und "unter <strong>streichen</strong> " werden standardmäßig angezeigt. Sie können jedoch ausgeblendet werden, indem Sie die Attribute " <em>isstrikeflowbuttonvisible</em> " und " <em>isunderlinebuttonvisible</em> " auf festlegen <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-137">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default but can be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="841e8-138">Farbfarb Auswahl für <strong>Text</strong> .</span><span class="sxs-lookup"><span data-stu-id="841e8-138"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="841e8-139"><strong>Farbauswahl für Text Hervorhebung</strong> .</span><span class="sxs-lookup"><span data-stu-id="841e8-139"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-140">Dieses Steuerelement ist standardmäßig ausgeblendet, kann jedoch angezeigt werden, indem das <em>ishighlightbuttonvisible</em> -Attribut auf festgelegt wird <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-140">This control is hidden by default but can be displayed by setting the <em>IsHighlightButtonVisible</em> attribute to <code>true</code>.</span></span>
</blockquote>
<p><br/></p></li>
</ul>
</dd> <span data-ttu-id="841e8-141"><dt><span></span><span></span><strong></strong> (Richfont)</span><span class="sxs-lookup"><span data-stu-id="841e8-141"><dt><span></span><span></span><strong></strong> (RichFont)</span></span><br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> <span data-ttu-id="841e8-142">Durch Festlegen des Attributs " <em>fonttype</em> " auf werden <code>RichFont</code> die folgenden Funktionen aktiviert:</span><span class="sxs-lookup"><span data-stu-id="841e8-142">Setting the <em>FontType</em> attribute to <code>RichFont</code> enables the following functionality:</span></span><br/>
<ul>
<li><span data-ttu-id="841e8-143">Kombinations Feld " <strong>Schriftfamilie</strong> ".</span><span class="sxs-lookup"><span data-stu-id="841e8-143"><strong>Font family</strong> combo box.</span></span></li>
<li><span data-ttu-id="841e8-144">Kombinations Feld " <strong>Schriftgröße</strong> ".</span><span class="sxs-lookup"><span data-stu-id="841e8-144"><strong>Font size</strong> combo box.</span></span></li>
<li><span data-ttu-id="841e8-145"><strong>Vergrößern Sie Schriftart</strong> , und <strong>verkleinern</strong> Sie die Schriftart für die Schriftgröße und die Dekrement-Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="841e8-145"><strong>Grow font</strong> and <strong>Shrink font</strong> font size increment and decrement buttons.</span></span></li>
<li><p><span data-ttu-id="841e8-146">Die UMSCHALT Flächen <strong>Fett</strong>, <strong>kursiv</strong>, unter <strong>Strichen</strong>und <strong>durch</strong> gestrichen.</span><span class="sxs-lookup"><span data-stu-id="841e8-146"><strong>Bold</strong>, <strong>Italic</strong>, <strong>Underline</strong>, and <strong>Strikethrough</strong> toggle buttons.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-147">Die UMSCHALT Flächen " <strong>durch</strong> gestrichen" und "unter <strong>streichen</strong> " werden standardmäßig angezeigt und können nicht ausgeblendet werden, indem die Attribute " <em>isstrikeflowbuttonvisible</em> " und " <em>isunderlinebuttonvisible</em> " auf festgelegt werden <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-147">The <strong>Strikethrough</strong> and <strong>Underline</strong> toggle buttons are displayed by default and cannot be hidden by setting the <em>IsStrikethroughButtonVisible</em> and <em>IsUnderlineButtonVisible</em> attributes to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="841e8-148">Farbfarb Auswahl für <strong>Text</strong> .</span><span class="sxs-lookup"><span data-stu-id="841e8-148"><strong>Text color</strong> color picker.</span></span></li>
<li><p><span data-ttu-id="841e8-149"><strong>Farbauswahl für Text Hervorhebung</strong> .</span><span class="sxs-lookup"><span data-stu-id="841e8-149"><strong>Text highlight color</strong> color picker.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-150">Dieses Steuerelement wird standardmäßig angezeigt und kann nicht ausgeblendet werden, indem das <em>ishighlightbuttonvisible</em> -Attribut auf festgelegt wird <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-150">This control is displayed by default and cannot be hidden by setting the <em>IsHighlightButtonVisible</em> attribute to <code>false</code>.</span></span>
</blockquote>
<p><br/></p></li>
<li><span data-ttu-id="841e8-151">UMSCHALT Flächen für das Tief <strong>gestellte und das</strong> <strong>SuperScript</strong> .</span><span class="sxs-lookup"><span data-stu-id="841e8-151"><strong>Subscript</strong> and <strong>Superscript</strong> toggle buttons.</span></span></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="841e8-152"><strong>Isgrowshrinkbuttongroupvisible</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-152"><strong>IsGrowShrinkButtonGroupVisible</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-153">Boolesch</span><span class="sxs-lookup"><span data-stu-id="841e8-153">Boolean</span></span><br/></td>
<td><span data-ttu-id="841e8-154">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-154">No</span></span><br/></td>
<td><span data-ttu-id="841e8-155"><strong>Windows 8 und höher</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-155"><strong>Windows 8 and newer</strong></span></span><br/> <span data-ttu-id="841e8-156">Beschränkt auf einen der folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="841e8-156">Restricted to one of the following values:</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-157">Die Schaltflächen vergrößern/verkleinern werden nie in der <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>angezeigt.</span><span class="sxs-lookup"><span data-stu-id="841e8-157">The Grow/Shrink buttons are never displayed in the <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="841e8-158">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="841e8-158">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-159">Standardwert, wenn der Wert von " <em>fonttype</em> " <code>FontWithColor</code> oder ist <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-159">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="841e8-160"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="841e8-160"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-161">Standardwert, wenn der Wert von " <em>fonttype</em> " ist <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-161">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="841e8-162"><strong>Ishighlightbuttonvisible</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-162"><strong>IsHighlightButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-163">Boolesch</span><span class="sxs-lookup"><span data-stu-id="841e8-163">Boolean</span></span><br/></td>
<td><span data-ttu-id="841e8-164">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-164">No</span></span><br/></td>
<td><span data-ttu-id="841e8-165">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="841e8-165">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-166">Die Farb Hervorhebung ist nur von einem <strong>FontControl</strong> -Element verfügbar, wenn der Wert des <em>fonttype</em> -Attributs <code>FontWithColor</code> oder entspricht <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-166">Color highlighting is available only from a <strong>FontControl</strong> when the value of the <em>FontType</em> attribute equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="841e8-167">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="841e8-167">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-168">Standardwert, wenn der Wert von " <em>fonttype</em> " <code>FontWithColor</code> oder ist <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-168">Default when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> <span data-ttu-id="841e8-169">Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontWithColor</code> oder ist <code>RichFont</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-169">Valid only when the value of <em>FontType</em> equals <code>FontWithColor</code> or <code>RichFont</code>.</span></span><br/> </dd> <span data-ttu-id="841e8-170"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="841e8-170"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-171">Standardwert, wenn der Wert von " <em>fonttype</em> " ist <code>FontOnly</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-171">Default when the value of <em>FontType</em> equals <code>FontOnly</code>.</span></span><br/> <span data-ttu-id="841e8-172">Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontOnly</code> oder ist <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-172">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="841e8-173"><strong>Isstrikethrough buttonvisible</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-173"><strong>IsStrikethroughButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-174">Boolesch</span><span class="sxs-lookup"><span data-stu-id="841e8-174">Boolean</span></span><br/></td>
<td><span data-ttu-id="841e8-175">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-175">No</span></span><br/></td>
<td><span data-ttu-id="841e8-176">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="841e8-176">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="841e8-177">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="841e8-177">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-178">Standard.</span><span class="sxs-lookup"><span data-stu-id="841e8-178">Default.</span></span> <br/> </dd> <span data-ttu-id="841e8-179"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="841e8-179"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-180">Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontOnly</code> oder ist <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-180">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="841e8-181"><strong>Isunderlinebuttonvisible</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-181"><strong>IsUnderlineButtonVisible</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-182">Boolesch</span><span class="sxs-lookup"><span data-stu-id="841e8-182">Boolean</span></span><br/></td>
<td><span data-ttu-id="841e8-183">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-183">No</span></span><br/></td>
<td><span data-ttu-id="841e8-184">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="841e8-184">Restricted to one of the following values (0 and 1 are not valid):</span></span> <br/> <br/><span data-ttu-id="841e8-185">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="841e8-185">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-186">Standard.</span><span class="sxs-lookup"><span data-stu-id="841e8-186">Default.</span></span> <br/> </dd> <span data-ttu-id="841e8-187"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="841e8-187"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-188">Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontOnly</code> oder ist <code>FontWithColor</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-188">Valid only when the value of <em>FontType</em> equals <code>FontOnly</code> or <code>FontWithColor</code>.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="841e8-189"><strong>Maximumfontsize</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-189"><strong>MaximumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-190">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="841e8-190">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="841e8-191">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-191">No</span></span><br/></td>
<td><span data-ttu-id="841e8-192">Die maximale anzuzeigende Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="841e8-192">The maximum point size to display.</span></span><br/> <br/><span data-ttu-id="841e8-193">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="841e8-193">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-194">Ein ganzzahliger Wert zwischen 1 und 9999 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="841e8-194">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="841e8-195">Der Standardwert ist <strong>9999</strong>.</span><span class="sxs-lookup"><span data-stu-id="841e8-195">Default is <strong>9999</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="841e8-196"><strong>MinimumFontSize</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-196"><strong>MinimumFontSize</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-197">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="841e8-197">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="841e8-198">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-198">No</span></span><br/></td>
<td><span data-ttu-id="841e8-199">Die minimale anzuzeigende Punktgröße.</span><span class="sxs-lookup"><span data-stu-id="841e8-199">The minimum point size to display.</span></span><br/> <br/><span data-ttu-id="841e8-200">
<dt><span></span><span></span><strong></strong> (xs: positivin teger)</span><span class="sxs-lookup"><span data-stu-id="841e8-200">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-201">Ein ganzzahliger Wert zwischen 1 und 9999 (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="841e8-201">An integer value between 1 and 9999, inclusive.</span></span><br/> <span data-ttu-id="841e8-202">Der Standardwert ist <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="841e8-202">Default is <strong>1</strong>.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="841e8-203"><strong>Showtruetypinonly</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-203"><strong>ShowTrueTypeOnly</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-204">Boolesch</span><span class="sxs-lookup"><span data-stu-id="841e8-204">Boolean</span></span><br/></td>
<td><span data-ttu-id="841e8-205">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-205">No</span></span><br/></td>
<td><span data-ttu-id="841e8-206">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="841e8-206">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="841e8-207">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="841e8-207">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-208">Zeigt nur TrueType-und OpenType-Schriftarten an.</span><span class="sxs-lookup"><span data-stu-id="841e8-208">Displays TrueType and OpenType fonts only.</span></span> <br/> </dd> <span data-ttu-id="841e8-209"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="841e8-209"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-210">Standard.</span><span class="sxs-lookup"><span data-stu-id="841e8-210">Default.</span></span> <span data-ttu-id="841e8-211">Der Typ der angezeigten Schriftarten wird nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="841e8-211">No restriction is placed on the type of fonts displayed.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="841e8-212"><strong>Showverticalfonts</strong></span><span class="sxs-lookup"><span data-stu-id="841e8-212"><strong>ShowVerticalFonts</strong></span></span><br/></td>
<td><span data-ttu-id="841e8-213">Boolesch</span><span class="sxs-lookup"><span data-stu-id="841e8-213">Boolean</span></span><br/></td>
<td><span data-ttu-id="841e8-214">Nein</span><span class="sxs-lookup"><span data-stu-id="841e8-214">No</span></span><br/></td>
<td><span data-ttu-id="841e8-215">Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):</span><span class="sxs-lookup"><span data-stu-id="841e8-215">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-216">Vertikalen Schriftarten wird ein @-Symbol in der <strong>Schriftfamilien</strong> Liste vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="841e8-216">Vertical fonts are preceded by an @ symbol in the <strong>Font family</strong> list.</span></span>
</blockquote>
<br/> <br/><span data-ttu-id="841e8-217">
<dt><span></span><span></span><strong></strong> Fall</span><span class="sxs-lookup"><span data-stu-id="841e8-217">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-218">Standard.</span><span class="sxs-lookup"><span data-stu-id="841e8-218">Default.</span></span> <span data-ttu-id="841e8-219">Zeigt die vertikalen Schriftarten an, die in der Systemsteuerung der <strong>Schriftarten</strong> <strong>angezeigt</strong> werden.</span><span class="sxs-lookup"><span data-stu-id="841e8-219">Displays the vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span> <br/> </dd> <span data-ttu-id="841e8-220"><dt><span></span><span></span><strong></strong> Alarm</span><span class="sxs-lookup"><span data-stu-id="841e8-220"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd> <span data-ttu-id="841e8-221">Ermöglicht es einer Anwendung, die vertikalen Text nicht unterstützt, vertikale Schriftarten auszublenden, die in der Systemsteuerung der <strong>Schriftarten</strong> <strong>angezeigt</strong> werden.</span><span class="sxs-lookup"><span data-stu-id="841e8-221">Allows an application that does not support vertical text to hide any vertical fonts that are set to <strong>Show</strong> in the <strong>Fonts</strong> control panel.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="841e8-222">In Windows Vista bietet die Systemsteuerung für <strong>Schriftarten</strong> keine Funktionen zum <strong>anzeigen</strong> oder <strong>Ausblenden</strong> .</span><span class="sxs-lookup"><span data-stu-id="841e8-222">In Windows Vista, the <strong>Fonts</strong> control panel does not offer <strong>Show</strong> or <strong>Hide</strong> functionality.</span></span> <span data-ttu-id="841e8-223">In diesem Fall muss das <em>showverticalfonts</em> -Attribut auf festgelegt werden <code>False</code> .</span><span class="sxs-lookup"><span data-stu-id="841e8-223">In this case, the <em>ShowVerticalFonts</em> attribute must be set to <code>False</code>.</span></span>
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="841e8-224">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="841e8-224">Child elements</span></span>

<span data-ttu-id="841e8-225">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="841e8-225">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="841e8-226">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="841e8-226">Parent elements</span></span>



| <span data-ttu-id="841e8-227">Element</span><span class="sxs-lookup"><span data-stu-id="841e8-227">Element</span></span>                                                               |
|-----------------------------------------------------------------------|
| [<span data-ttu-id="841e8-228">**Controlgroup**</span><span class="sxs-lookup"><span data-stu-id="841e8-228">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/> |
| [<span data-ttu-id="841e8-229">**Gruppe**</span><span class="sxs-lookup"><span data-stu-id="841e8-229">**Group**</span></span>](windowsribbon-element-group.md)<br/>               |
| [<span data-ttu-id="841e8-230">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="841e8-230">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a><span data-ttu-id="841e8-231">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="841e8-231">Remarks</span></span>

<span data-ttu-id="841e8-232">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="841e8-232">Optional.</span></span>

<span data-ttu-id="841e8-233">Kann höchstens einmal für jedes Element der Gruppe " [**controlgroup**](windowsribbon-element-controlgroup.md)", " [**Group**](windowsribbon-element-group.md)" oder " [**MenuGroup**](windowsribbon-element-menugroup.md) " auftreten.</span><span class="sxs-lookup"><span data-stu-id="841e8-233">May occur at most once for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), or [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="841e8-234">Alle im Markup deklarierten **FontControl** -Befehls Attribute, z [**. b. Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md), werden von den Attributen der einzelnen Steuerelemente, aus denen das **FontControl**-Element besteht, überschrieben.</span><span class="sxs-lookup"><span data-stu-id="841e8-234">Any **FontControl** Command attributes declared in markup, such as [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) or [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), are overridden by the attributes of the individual controls that comprise the **FontControl**.</span></span>

<span data-ttu-id="841e8-235">Jeder Versuch, ein Farbmuster aus der Farbauswahl eines [Schriftart Steuer](windowsribbon-controls-fontcontrol.md) Elements auszuwählen, kann zu einer Zugriffsverletzung führen, wenn dem Steuerelement kein Befehls Handler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="841e8-235">Any attempt to select a color swatch from the color picker of a [Font Control](windowsribbon-controls-fontcontrol.md) may result in an access violation if no Command handler is associated with the control.</span></span>

## <a name="examples"></a><span data-ttu-id="841e8-236">Beispiele</span><span class="sxs-lookup"><span data-stu-id="841e8-236">Examples</span></span>

<span data-ttu-id="841e8-237">Im folgenden Beispiel wird das grundlegende Markup für die drei Arten von [Schriftart Steuer](windowsribbon-controls-fontcontrol.md)Elementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="841e8-237">The following example demonstrates the basic markup for the three types of [Font Control](windowsribbon-controls-fontcontrol.md).</span></span>

<span data-ttu-id="841e8-238">In diesem Code Abschnitt werden die **FontControl** -Befehls Deklarationen angezeigt, die jeweils über eine [**Gruppen**](windowsribbon-element-group.md) Container Deklaration verfügen.</span><span class="sxs-lookup"><span data-stu-id="841e8-238">This section of code shows the **FontControl** Command declarations, each with a [**Group**](windowsribbon-element-group.md) container declaration.</span></span>


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



<span data-ttu-id="841e8-239">Dieser Code Abschnitt zeigt die **FontControl** -Steuerelement Deklarationen, in denen jedes **FontControl** und jede [**Gruppe**](windowsribbon-element-group.md) auf einer einzelnen Registerkarte deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="841e8-239">This section of code shows the **FontControl** control declarations where each **FontControl** and [**Group**](windowsribbon-element-group.md) is declared in a single Tab.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="841e8-240">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="841e8-240">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="841e8-241">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="841e8-241">Minimum supported system</span></span><br/> | <span data-ttu-id="841e8-242">Windows 7</span><span class="sxs-lookup"><span data-stu-id="841e8-242">Windows 7</span></span> |
| <span data-ttu-id="841e8-243">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="841e8-243">Can be empty</span></span>                        | <span data-ttu-id="841e8-244">Ja</span><span class="sxs-lookup"><span data-stu-id="841e8-244">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="841e8-245">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="841e8-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841e8-246">Schriftart Steuerelement Steuerelement</span><span class="sxs-lookup"><span data-stu-id="841e8-246">Font Control control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="841e8-247">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="841e8-247">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="841e8-248">FontControl-Beispiel</span><span class="sxs-lookup"><span data-stu-id="841e8-248">FontControl Sample</span></span>](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





