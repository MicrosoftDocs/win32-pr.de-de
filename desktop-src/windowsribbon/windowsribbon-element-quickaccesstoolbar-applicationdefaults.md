---
title: QuickAccessToolbar.ApplicationDefaults-Eigenschaft
description: Stellt einen Container für Standardbefehle in der Schnellzugriffssymbolleiste (Quick Access Toolbar, QAT) dar.
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- QuickAccessToolbar.ApplicationDefaults-Eigenschaft Windows Menüband
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701a7c72e40b1efe9104d6794fa739c556b0fb4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473746"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>QuickAccessToolbar.ApplicationDefaults-Eigenschaft

Stellt einen Container für Standardbefehle in der [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md)dar.

## <a name="usage"></a>Verbrauch

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente




| Element | BESCHREIBUNG | 
|---------|-------------|
| <a href="windowsribbon-element-button.md"><strong>Schaltfläche</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><br /> | 
| <a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><br /> | 
| <a href="windowsribbon-element-combobox.md"><strong>Kombinationsfeld</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><blockquote>[!Note]<br />Windows 8 und neuer.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><blockquote>[!Note]<br />Windows 8 und neuer.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><blockquote>[!Note]<br />Windows 8 und neuer.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><blockquote>[!Note]<br />Windows 8 und neuer.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br /> | Muss mindestens einmal vorkommen.<br /><br /> | 




## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jede [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)auftreten.

Mindestens ein untergeordnetes Element muss angegeben werden.

Es können maximal 20 untergeordnete Elemente angegeben werden.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für [**quickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)veranschaulicht.

Dieser Codeabschnitt zeigt die **QuickAccessToolbar.ApplicationDefaults-Steuerelementdeklaration.**


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
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Symbolleisten-Steuerelement für den Schnellzugriff](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





