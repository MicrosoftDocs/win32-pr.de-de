---
title: FontControl-Element
description: Stellt ein Schriftartsteuerelement dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente für die Schriftartbearbeitung handelt.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- FontControl-Element Windows Menüband
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7b068246da9b26a4b3547e27abd1a9b60c8fd70de10e4edd2438463a156633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202519"
---
# <a name="fontcontrol-element"></a>FontControl-Element

Stellt ein [Schriftartsteuerelement](windowsribbon-controls-fontcontrol.md)dar, bei dem es sich um einen speziellen Container einzelner Steuerelemente für die Schriftartbearbeitung handelt.

## <a name="usage"></a>Verwendung

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

## <a name="attributes"></a>Attributes



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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger oder xs:string<br/></td>
<td>Nein<br/></td>
<td>Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999( einschließlich) oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich. <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte: <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Standard. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Das Festlegen des <em>FontType-Attributs</em> auf <code>FontOnly</code> ermöglicht die folgende Funktionalität:<br/>
<ul>
<li><strong>Kombinationsfeld der Schriftfamilie.</strong></li>
<li><strong>Kombinationsfeld "Schriftgrad".</strong></li>
<li><p><strong>Fette,</strong> <strong>kursiv formatierte,</strong> <strong>unterstrichene</strong>und <strong>durchgestrichene</strong> Umschaltflächen.</p>
<blockquote>
[!Note]<br />
Die Umschaltflächen <strong>Durchstreich</strong> und <strong>Unterstreichung</strong> werden standardmäßig angezeigt, können jedoch ausgeblendet werden, indem sie die Attribute <em>IsStrikethroughButtonVisible</em> und <em>IsUnderlineButtonVisible</em> auf <code>false</code> festlegen.
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Das Festlegen des <em>FontType-Attributs</em> auf <code>FontWithColor</code> ermöglicht die folgende Funktionalität:<br/>
<ul>
<li><strong>Kombinationsfeld der Schriftfamilie.</strong></li>
<li><strong>Kombinationsfeld "Schriftgrad".</strong></li>
<li>Schaltflächen <strong>"Schriftart</strong> vergrößern" und <strong>"Schriftgrad verkleinern"</strong> inkrementieren und verringern.</li>
<li><p><strong>Fette,</strong> <strong>kursiv formatierte,</strong> <strong>unterstrichene</strong>und <strong>durchgestrichene</strong> Umschaltflächen.</p>
<blockquote>
[!Note]<br />
Die Umschaltflächen <strong>Durchstreich</strong> und <strong>Unterstreichung</strong> werden standardmäßig angezeigt, können jedoch ausgeblendet werden, indem sie die Attribute <em>IsStrikethroughButtonVisible</em> und <em>IsUnderlineButtonVisible</em> auf <code>false</code> festlegen.
</blockquote>
<p><br/></p></li>
<li><strong>Farbauswahl für Textfarbe.</strong></li>
<li><p><strong>Farbauswahl für Textmarkierung.</strong></p>
<blockquote>
[!Note]<br />
Dieses Steuerelement ist standardmäßig ausgeblendet, kann jedoch durch Festlegen des <em>IsHighlightButtonVisible-Attributs</em> auf angezeigt <code>true</code> werden.
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Das Festlegen des <em>FontType-Attributs</em> auf <code>RichFont</code> ermöglicht die folgende Funktionalität:<br/>
<ul>
<li><strong>Kombinationsfeld der Schriftfamilie.</strong></li>
<li><strong>Kombinationsfeld "Schriftgrad".</strong></li>
<li>Schaltflächen <strong>"Schriftart</strong> vergrößern" und <strong>"Schriftgrad verkleinern"</strong> inkrementieren und verringern.</li>
<li><p><strong>Fette,</strong> <strong>kursiv formatierte,</strong> <strong>unterstrichene</strong>und <strong>durchgestrichene</strong> Umschaltflächen.</p>
<blockquote>
[!Note]<br />
Die Umschaltflächen <strong>Durchstreichen</strong> und <strong>Unterstrichen</strong> werden standardmäßig angezeigt und können nicht ausgeblendet werden, indem die Attribute <em>IsStrikethroughButtonVisible</em> und <em>IsUnderlineButtonVisible</em> auf festgelegt <code>false</code> werden.
</blockquote>
<p><br/></p></li>
<li><strong>Farbauswahl für Textfarbe.</strong></li>
<li><p><strong>Farbauswahl für Textmarkierung.</strong></p>
<blockquote>
[!Note]<br />
Dieses Steuerelement wird standardmäßig angezeigt und kann nicht ausgeblendet werden, indem das <em>IsHighlightButtonVisible-Attribut</em> auf festgelegt <code>false</code> wird.
</blockquote>
<p><br/></p></li>
<li><strong>Umschaltflächen "Tiefgestellt"</strong> und <strong>"Superscript".</strong></li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td><strong>Windows 8 und neuer</strong><br/> Beschränkt auf einen der folgenden Werte: <br/>
<blockquote>
[!Note]<br />
Die Schaltflächen Vergrößern/Verkleinern werden nie in der <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>angezeigt.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontWithColor</code> oder <code>RichFont</code> ist.<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> ist.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig): <br/>
<blockquote>
[!Note]<br />
Die Farbhervorhebung ist nur über <strong>ein FontControl</strong> verfügbar, wenn der Wert des <em>FontType-Attributs</em> <code>FontWithColor</code> gleich oder <code>RichFont</code> ist.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontWithColor</code> oder <code>RichFont</code> ist.<br/> Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontWithColor</code> oder <code>RichFont</code> ist.<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Standardwert, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> ist.<br/> Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> oder <code>FontWithColor</code> ist.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> oder <code>FontWithColor</code> ist. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Nur gültig, wenn der Wert von <em>FontType</em> gleich <code>FontOnly</code> oder <code>FontWithColor</code> ist. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die maximale anzuzeigende Punktgröße.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 1 und 9999(einschließlich).<br/> Der Standardwert ist <strong>9999.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Nein<br/></td>
<td>Die minimale anzuzeigende Punktgröße.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Ein ganzzahliger Wert zwischen 1 und 9999(einschließlich).<br/> Der Standardwert ist <strong>1.</strong><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Zeigt nur TrueType- und OpenType-Schriftarten an. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Standard. Der angezeigte Schriftarttyp wird nicht eingeschränkt.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolesch<br/></td>
<td>Nein<br/></td>
<td>Beschränkt auf einen der folgenden Werte (0 und 1 sind ungültig):<br/>
<blockquote>
[!Note]<br />
Vertikalen Schriftarten wird in der Liste <strong>Schriftfamilie</strong> ein @-Symbol vorangestellt.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Standard. Zeigt die vertikalen Schriftarten an, die in der Systemsteuerung <strong>Schriftarten</strong> auf <strong>Anzeigen</strong> festgelegt sind. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Ermöglicht einer Anwendung, die vertikalen Text nicht unterstützt, vertikale Schriftarten auszublenden, die in der Systemsteuerung <strong>Schriftarten</strong> auf <strong>Anzeigen</strong> festgelegt sind.<br/>
<blockquote>
[!Note]<br />
In Windows Vista bietet die Systemsteuerung <strong>Schriftarten</strong> keine Funktionen <strong>zum Ein-</strong> oder <strong>Ausblenden.</strong> In diesem Fall muss das <em>ShowVerticalFonts-Attribut</em> auf festgelegt <code>False</code> werden.
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
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/> |
| [**Gruppe**](windowsribbon-element-group.md)<br/>               |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jedes [**ControlGroup-,**](windowsribbon-element-controlgroup.md) [**Group-**](windowsribbon-element-group.md)oder [**MenuGroup-Element**](windowsribbon-element-menugroup.md) auftreten.

Alle im Markup deklarierten FontControl-Befehlsattribute, z. B. [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) oder [**Command.TooltipTitle,**](windowsribbon-element-command-tooltiptitle.md)werden durch die Attribute der einzelnen Steuerelemente überschrieben, aus denen das **FontControl** besteht. 

Jeder Versuch, eine Farbüberwachung aus der Farbauswahl eines [Schriftartsteuerelements](windowsribbon-controls-fontcontrol.md) auszuwählen, kann zu einer Zugriffsverletzung führen, wenn dem Steuerelement kein Befehlshandler zugeordnet ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die drei Typen des [Schriftartsteuerelements](windowsribbon-controls-fontcontrol.md)veranschaulicht.

In diesem Codeabschnitt  werden die FontControl-Befehlsdeklarationen mit jeweils einer [**Group-Containerdeklaration**](windowsribbon-element-group.md) angezeigt.


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



Dieser Codeabschnitt zeigt die **FontControl-Steuerelementdeklarationen,** in denen jedes **FontControl** und jede [**Gruppe**](windowsribbon-element-group.md) auf einer einzigen Registerkarte deklariert wird.


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

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Ja



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Steuerelement "Schriftartensteuerelement"](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Eigenschaften des Schriftartsteuerelements](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[FontControl-Beispiel](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





