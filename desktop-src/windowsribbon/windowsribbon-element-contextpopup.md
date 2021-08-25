---
title: ContextPopup-Element
description: Stellt das Kontext-Popup-Steuerelement in der ContextPopup-Ansicht dar.
ms.assetid: b955be16-803e-47b5-a72d-f993180fbf14
keywords:
- ContextPopup-Element Windows Menüband
topic_type:
- apiref
api_name:
- ContextPopup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8fddda30a765eb314c7a29934c9fcdd12404647de9f1e480275f8fa685b50827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840790"
---
# <a name="contextpopup-element"></a>ContextPopup-Element

Stellt das [Kontext-Popup-Steuerelement](windowsribbon-controls-contextpopup.md) in der ContextPopup-Ansicht dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ContextPopup>
  child elements
</ContextPopup>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                         | Beschreibung                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**ContextPopup.ContextMaps**](windowsribbon-element-contextpopup-contextmaps.md)<br/>   | Kann höchstens einmal auftreten.<br/> <br/> |
| [**ContextPopup.ContextMenus**](windowsribbon-element-contextpopup-contextmenus.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |
| [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Application.Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann höchstens einmal für jede [**Application.Views-Datei**](windowsribbon-element-application-views.md)auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für eine **ContextPopup-Ansicht** veranschaulicht.


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

 

 





