---
title: MiniToolbar-Element
description: Stellt eine kontextbezogene Symbolleiste dar.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- MiniToolbar-Element Windows Menüband
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e47fee9fbf2b6b0bc95153fd512f6484129dc7f3edebd56e1d97664ecc2bbef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881740"
---
# <a name="minitoolbar-element"></a>MiniToolbar-Element

Stellt eine kontextbezogene Symbolleiste dar.

## <a name="usage"></a>Verbrauch

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a>Attribute



| attribute           | type                 | Erforderlich       | BESCHREIBUNG                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Name**<br/> | xs:string<br/> | Ja<br/> | <dt> (xs:string)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Sequenz von Zeichen besteht, einschließlich Leerzeichen und Zeilenunterbrechungszeichen.<br/> </dd> </dl> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                         | BESCHREIBUNG                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/> | Muss mindestens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a>Hinweise

Optional.

Kann ein oder mehrere Male für jede [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)auftreten.

Im Gegensatz zum [**ContextMenu-Element**](windowsribbon-element-contextmenu.md) bleibt die **MiniToolbar** sichtbar, wenn auf ein Element auf der Symbolleiste geklickt wird.

Wenn die **Minitoolleiste** ohne [**ContextMenu**](windowsribbon-element-contextmenu.md)angezeigt wird, wird sie ausgeblendet, wenn der Mauszeiger entfernt wird.

> [!Note]  
> Aufgrund dieses verblassenden Verhaltens sollte ein [**ContextMenu**](windowsribbon-element-contextmenu.md) in unmittelbarer Nähe zum Mauszeiger angezeigt werden.

 

Da Auf Steuerelemente in der **MiniToolbar** nicht über die Tastatur zugegriffen werden kann, sollten die verfügbar gemachten Befehle an anderer Stelle auf der Menübandbenutzeroberfläche verfügbar sein.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für eine [**ContextPopup-Ansicht**](windowsribbon-element-contextpopup.md) veranschaulicht.

Dieser Codeabschnitt zeigt eine Reihe von **MiniToolbar-Steuerelementdeklarationen.**


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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kontext-Popup-Steuerelement](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





