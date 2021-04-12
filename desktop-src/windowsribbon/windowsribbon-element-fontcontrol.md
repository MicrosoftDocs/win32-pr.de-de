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
# <a name="fontcontrol-element"></a>FontControl-Element

Stellt ein [Schriftart Steuer](windowsribbon-controls-fontcontrol.md)Element dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente handelt, die für die Schriftart Bearbeitung

## <a name="usage"></a>Verbrauch

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

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>type</th>
<th>Erforderlich</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Fonttype</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte: <br/> <br/>
<dt><span></span><span></span><strong></strong> (Fontonly)<br/> </dt> <dd> Standard. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Durch Festlegen des Attributs " <em>fonttype</em> " auf werden <code>FontOnly</code> die folgenden Funktionen aktiviert:<br/>
<ul>
<li>Kombinations Feld " <strong>Schriftfamilie</strong> ".</li>
<li>Kombinations Feld " <strong>Schriftgröße</strong> ".</li>
<li><p>Die UMSCHALT Flächen <strong>Fett</strong>, <strong>kursiv</strong>, unter <strong>Strichen</strong>und <strong>durch</strong> gestrichen.</p>
<blockquote>
[!Note]<br />
Die UMSCHALT Flächen " <strong>durch</strong> gestrichen" und "unter <strong>streichen</strong> " werden standardmäßig angezeigt. Sie können jedoch ausgeblendet werden, indem Sie die Attribute " <em>isstrikeflowbuttonvisible</em> " und " <em>isunderlinebuttonvisible</em> " auf festlegen <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Fontwithcolor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Durch Festlegen des Attributs " <em>fonttype</em> " auf werden <code>FontWithColor</code> die folgenden Funktionen aktiviert:<br/>
<ul>
<li>Kombinations Feld " <strong>Schriftfamilie</strong> ".</li>
<li>Kombinations Feld " <strong>Schriftgröße</strong> ".</li>
<li><strong>Vergrößern Sie Schriftart</strong> , und <strong>verkleinern</strong> Sie die Schriftart für die Schriftgröße und die Dekrement-Schaltflächen</li>
<li><p>Die UMSCHALT Flächen <strong>Fett</strong>, <strong>kursiv</strong>, unter <strong>Strichen</strong>und <strong>durch</strong> gestrichen.</p>
<blockquote>
[!Note]<br />
Die UMSCHALT Flächen " <strong>durch</strong> gestrichen" und "unter <strong>streichen</strong> " werden standardmäßig angezeigt. Sie können jedoch ausgeblendet werden, indem Sie die Attribute " <em>isstrikeflowbuttonvisible</em> " und " <em>isunderlinebuttonvisible</em> " auf festlegen <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Farbfarb Auswahl für <strong>Text</strong> .</li>
<li><p><strong>Farbauswahl für Text Hervorhebung</strong> .</p>
<blockquote>
[!Note]<br />
Dieses Steuerelement ist standardmäßig ausgeblendet, kann jedoch angezeigt werden, indem das <em>ishighlightbuttonvisible</em> -Attribut auf festgelegt wird <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Richfont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Durch Festlegen des Attributs " <em>fonttype</em> " auf werden <code>RichFont</code> die folgenden Funktionen aktiviert:<br/>
<ul>
<li>Kombinations Feld " <strong>Schriftfamilie</strong> ".</li>
<li>Kombinations Feld " <strong>Schriftgröße</strong> ".</li>
<li><strong>Vergrößern Sie Schriftart</strong> , und <strong>verkleinern</strong> Sie die Schriftart für die Schriftgröße und die Dekrement-Schaltflächen</li>
<li><p>Die UMSCHALT Flächen <strong>Fett</strong>, <strong>kursiv</strong>, unter <strong>Strichen</strong>und <strong>durch</strong> gestrichen.</p>
<blockquote>
[!Note]<br />
Die UMSCHALT Flächen " <strong>durch</strong> gestrichen" und "unter <strong>streichen</strong> " werden standardmäßig angezeigt und können nicht ausgeblendet werden, indem die Attribute " <em>isstrikeflowbuttonvisible</em> " und " <em>isunderlinebuttonvisible</em> " auf festgelegt werden <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Farbfarb Auswahl für <strong>Text</strong> .</li>
<li><p><strong>Farbauswahl für Text Hervorhebung</strong> .</p>
<blockquote>
[!Note]<br />
Dieses Steuerelement wird standardmäßig angezeigt und kann nicht ausgeblendet werden, indem das <em>ishighlightbuttonvisible</em> -Attribut auf festgelegt wird <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>UMSCHALT Flächen für das Tief <strong>gestellte und das</strong> <strong>SuperScript</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Isgrowshrinkbuttongroupvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td><strong>Windows 8 und höher</strong><br/> Beschränkt auf einen der folgenden Werte: <br/>
<blockquote>
[!Note]<br />
Die Schaltflächen vergrößern/verkleinern werden nie in der <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>angezeigt.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standardwert, wenn der Wert von " <em>fonttype</em> " <code>FontWithColor</code> oder ist <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Standardwert, wenn der Wert von " <em>fonttype</em> " ist <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Ishighlightbuttonvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig): <br/>
<blockquote>
[!Note]<br />
Die Farb Hervorhebung ist nur von einem <strong>FontControl</strong> -Element verfügbar, wenn der Wert des <em>fonttype</em> -Attributs <code>FontWithColor</code> oder entspricht <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standardwert, wenn der Wert von " <em>fonttype</em> " <code>FontWithColor</code> oder ist <code>RichFont</code> .<br/> Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontWithColor</code> oder ist <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Standardwert, wenn der Wert von " <em>fonttype</em> " ist <code>FontOnly</code> .<br/> Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontOnly</code> oder ist <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Isstrikethrough buttonvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig): <br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontOnly</code> oder ist <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Isunderlinebuttonvisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig): <br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Nur gültig, wenn der Wert von " <em>fonttype</em> " <code>FontOnly</code> oder ist <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Maximumfontsize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die maximale anzuzeigende Punktgröße.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 1 und 9999 (einschließlich).<br/> Der Standardwert ist <strong>9999</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die minimale anzuzeigende Punktgröße.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positivin teger)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 1 und 9999 (einschließlich).<br/> Der Standardwert ist <strong>1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Showtruetypinonly</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Zeigt nur TrueType-und OpenType-Schriftarten an. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Standard. Der Typ der angezeigten Schriftarten wird nicht eingeschränkt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Showverticalfonts</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Auf einen der folgenden Werte beschränkt (0 und 1 sind ungültig):<br/>
<blockquote>
[!Note]<br />
Vertikalen Schriftarten wird ein @-Symbol in der <strong>Schriftfamilien</strong> Liste vorangestellt.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> Fall<br/> </dt> <dd> Standard. Zeigt die vertikalen Schriftarten an, die in der Systemsteuerung der <strong>Schriftarten</strong> <strong>angezeigt</strong> werden. <br/> </dd> <dt><span></span><span></span><strong></strong> Alarm<br/> </dt> <dd> Ermöglicht es einer Anwendung, die vertikalen Text nicht unterstützt, vertikale Schriftarten auszublenden, die in der Systemsteuerung der <strong>Schriftarten</strong> <strong>angezeigt</strong> werden.<br/>
<blockquote>
[!Note]<br />
In Windows Vista bietet die Systemsteuerung für <strong>Schriftarten</strong> keine Funktionen zum <strong>anzeigen</strong> oder <strong>Ausblenden</strong> . In diesem Fall muss das <em>showverticalfonts</em> -Attribut auf festgelegt werden <code>False</code> .
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                               |
|-----------------------------------------------------------------------|
| [**Controlgroup**](windowsribbon-element-controlgroup.md)<br/> |
| [**Gruppe**](windowsribbon-element-group.md)<br/>               |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes Element der Gruppe " [**controlgroup**](windowsribbon-element-controlgroup.md)", " [**Group**](windowsribbon-element-group.md)" oder " [**MenuGroup**](windowsribbon-element-menugroup.md) " auftreten.

Alle im Markup deklarierten **FontControl** -Befehls Attribute, z [**. b. Command. labeltitle**](windowsribbon-element-command-labeltitle.md) oder [**Command. ToolTipTitle**](windowsribbon-element-command-tooltiptitle.md), werden von den Attributen der einzelnen Steuerelemente, aus denen das **FontControl**-Element besteht, überschrieben.

Jeder Versuch, ein Farbmuster aus der Farbauswahl eines [Schriftart Steuer](windowsribbon-controls-fontcontrol.md) Elements auszuwählen, kann zu einer Zugriffsverletzung führen, wenn dem Steuerelement kein Befehls Handler zugeordnet ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die drei Arten von [Schriftart Steuer](windowsribbon-controls-fontcontrol.md)Elementen veranschaulicht.

In diesem Code Abschnitt werden die **FontControl** -Befehls Deklarationen angezeigt, die jeweils über eine [**Gruppen**](windowsribbon-element-group.md) Container Deklaration verfügen.


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



Dieser Code Abschnitt zeigt die **FontControl** -Steuerelement Deklarationen, in denen jedes **FontControl** und jede [**Gruppe**](windowsribbon-element-group.md) auf einer einzelnen Registerkarte deklariert wird.


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



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Schriftart Steuerelement Steuerelement](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Schriftart Steuerelement-Eigenschaften](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[FontControl-Beispiel](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





