---
title: ContextMenu-Element
description: Stellt ein Kontextmenüsteuerelement dar.
ms.assetid: 08cc0514-0795-4e6b-b80c-33d920783032
keywords:
- ContextMenu-Element Windows Menüband
topic_type:
- apiref
api_name:
- ContextMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fb061c08635cff46ca80d803089ebc01c48c19cdcc9136b1052c5a0ef2c3a1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707433"
---
# <a name="contextmenu-element"></a>ContextMenu-Element

Stellt ein Kontextmenüsteuerelement dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ContextMenu
  Name = "xs:string">
  child elements
</ContextMenu>
```

## <a name="attributes"></a>Attribute



| attribute           | type                 | Erforderlich       | Beschreibung                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Name**<br/> | xs:string<br/> | Ja<br/> | <dt> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | Beschreibung                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/> | Muss mindestens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jede [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)auftreten.

> [!IMPORTANT]
> **Ein ContextMenu** kann keine [Kombinationsfeld-](windowsribbon-controls-combobox.md) oder [Spinner-Steuerelemente](windowsribbon-controls-spinner.md) hosten.

 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für eine [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) veranschaulicht.

Dieser Codeabschnitt zeigt einen Satz von **ContextMenu-Steuerelementdeklarationen.**


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Kontext-Popup-Steuerelement](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





