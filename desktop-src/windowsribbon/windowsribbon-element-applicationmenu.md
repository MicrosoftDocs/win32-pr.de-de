---
title: ApplicationMenu-Element
description: Stellt das Anwendungsmenü dar. | ApplicationMenu-Element
ms.assetid: 815e0462-ea45-44b1-81bf-f5797b22e920
keywords:
- ApplicationMenu-Element Windows Menüband
topic_type:
- apiref
api_name:
- ApplicationMenu
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fcf64d3fa3b618a4e66777b8fd4c0d831a33126
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626126"
---
# <a name="applicationmenu-element"></a>ApplicationMenu-Element

Stellt das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)dar.

## <a name="usage"></a>Verwendung

``` syntax
<ApplicationMenu
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu>
```

## <a name="attributes"></a>Attribute



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Typ</th>
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
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                             | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/>      |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                                     | Kann ein oder mehrere Male auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                   |
|-------------------------------------------------------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss für jedes [**Menüband.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)genau einmal auftreten.

Die untergeordneten Elemente des **ApplicationMenu-Elements** müssen in der angegebenen Reihenfolge auftreten:

1.  [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md)
2.  [**Menugroup**](windowsribbon-element-menugroup.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das [Anwendungsmenü](windowsribbon-controls-applicationmenu.md)veranschaulicht.

Dieser Codeabschnitt zeigt die ApplicationMenu-Befehlsdeklarationen. 


```XML
<!-- Command declarations for the Application Menu. -->
<Command Name="cmdFileMenu"
         Symbol="ID_FILE_MENU"
         Id="25000" />
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
<!-- Command declarations for Application Menu items. -->
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
<Command Name="cmdPrint"
         Symbol="ID_FILE_PRINT"
         Comment="Save"
         Id="25004"
         LabelTitle="Print" />
<Command Name="cmdExit"
         Symbol="ID_FILE_EXIT"
         Comment="Exit"
         Id="25005"
         LabelTitle="Exit" />
```



Dieser Codeabschnitt zeigt die **ApplicationMenu-Steuerelementdeklarationen.**


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="element-information"></a>Elementinformationen

* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Anwendungsmenü-Steuerelement](windowsribbon-controls-applicationmenu.md)
</dt> </dl>

 

 





