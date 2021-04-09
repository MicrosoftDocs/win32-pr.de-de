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
# <a name="tab-element"></a>Registerkartenelement

Stellt eine [zentrale](windowsribbon-controls-tab.md) oder [kontextabhängige](windowsribbon-controls-tabgroup.md) Registerkarte dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
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
<td><strong>Applicationmodes</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Nur gültig, wenn <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> das übergeordnete Element ist.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die eine durch Trennzeichen getrennte Liste mit ganzen Zahlen zwischen 0 und 31 enthält.<br/> Leerraum ist gültig und wird ignoriert.<br/> Maximale Länge: 250 Zeichen. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveingeteger oder xs: String<br/></td>
<td>Nein<br/></td>
<td>Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)<br/> </dt> <dd> Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich). <br/> Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein. <br/> Maximale Länge: 100 Zeichen. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                         | BESCHREIBUNG                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**Gruppe**](windowsribbon-element-group.md)<br/>                         | Kann ein-oder mehrmals vorkommen<br/> <br/> |
| [**Tab. scalingpolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>      |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                             |
|---------------------------------------------------------------------|
| [**Menüband. Registerkarten**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss mindestens einmal für jedes [**Ribbon. Tabs**](windowsribbon-element-ribbon-tabs.md) -oder [**TabGroup**](windowsribbon-element-tabgroup.md) -Element vorkommen.

**Registerkarte** unterstützt [Anwendungsmodi](ribbon-applicationmodes.md).

Wenn [**scalingpolicy. ideal sizes**](windowsribbon-element-scalingpolicy-idealsizes.md) für das **Tab** -Element vorhanden ist, wird ein Eintrag für jedes [**Group**](windowsribbon-element-group.md) -Element und seine ideale Größe unter **scalingpolicy. idealsizes** benötigt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **Register** Karten-Element veranschaulicht.

In diesem Code Abschnitt werden die **Register** Karten Befehls Deklarationen für eine Registerkarte **Home** angezeigt.


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



In diesem Code Abschnitt werden die Deklarationen des **Register** Steuer Elements dargestellt.


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



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Registersteuerelement](windowsribbon-controls-tab.md)
</dt> <dt>

[Registerkarten-Steuerelement](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**Setmodes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

