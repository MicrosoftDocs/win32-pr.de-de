---
title: Quickaccesstoolbar. ApplicationDefaults (Eigenschaft)
description: Stellt einen Container für Standard Befehle in der Symbolleiste für den schnell Zugriff (QAT) dar.
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Quickaccesstoolbar. ApplicationDefaults-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337912"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>Quickaccesstoolbar. ApplicationDefaults (Eigenschaft)

Stellt einen Container für Standard Befehle in der [Symbolleiste für den schnell Zugriff (QAT)](windowsribbon-controls-quickaccesstoolbar.md)dar.

## <a name="usage"></a>Verbrauch

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-button.md"><strong>Schaltfläche</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/>
<blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>Dropdown Gallery</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/>
<blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>Inribbongallery</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/>
<blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>Splitbuttongallery</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/>
<blockquote>
[!Note]<br />
Windows 8 und höher.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>Muss mindestens einmal vorkommen.<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**Quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jede [**quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md)auftreten.

Es muss mindestens ein untergeordnetes Element angegeben werden.

Es können maximal 20 untergeordnete Elemente angegeben werden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für die [**quickaccesstoolbar**](windowsribbon-element-quickaccesstoolbar.md)veranschaulicht.

In diesem Code Abschnitt wird die Deklaration des **quickaccesstoolbar. ApplicationDefaults** -Steuer Elements veranschaulicht.


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Symbolleisten-Steuerelement schnell Zugriff](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





