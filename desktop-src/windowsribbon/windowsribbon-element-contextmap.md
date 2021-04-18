---
title: Contextmap-Element
description: Stellt eine ContextMenu-und MiniToolbar-paar Zuordnung dar.
ms.assetid: 84379578-24c6-4bf7-8dcf-8e21e5665d29
keywords:
- Windows-Menüband für contextmap-Element
topic_type:
- apiref
api_name:
- ContextMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e2ddcc8bdea16f5e00974b2b2e58934941e44c68
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "106340681"
---
# <a name="contextmap-element"></a>Contextmap-Element

Stellt eine [**ContextMenu**](windowsribbon-element-contextmenu.md) -und [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -paar Zuordnung dar.

## <a name="usage"></a>Verbrauch

``` syntax
<ContextMap
  CommandName = "xs:positiveInteger or xs:string"
  MiniToolbar = "xs:string"
  ContextMenu = "xs:string"/>
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
<td><strong>ContextMenu</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Muss einem vorhandenen <a href="windowsribbon-element-contextmenu.md"><strong>ContextMenu</strong></a> - <em>Namen</em>entsprechen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MiniToolbar</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Muss einem vorhandenen <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a> - <em>Namen</em>entsprechen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine Zeichenfolge, die aus einer beliebigen Zeichen Sequenz besteht, einschließlich Leerzeichen und Zeilenumbruch Zeichen.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                       |
|-----------------------------------------------------------------------------------------------|
| [**Contextpopup. contextmaps**](windowsribbon-element-contextpopup-contextmaps.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann für jede " [**contextpopup. contextmaps**](windowsribbon-element-contextpopup-contextmaps.md)" einmal oder mehrmals vorkommen.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für eine [**contextpopup**](windowsribbon-element-contextpopup.md) -Ansicht veranschaulicht.

Dieser Code Abschnitt zeigt einen Satz von **contextmap** -Steuerelement Deklarationen.


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



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Ja       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kontext-Popup Steuerelement](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





