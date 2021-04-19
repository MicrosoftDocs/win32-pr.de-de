---
title: Ribbon-Element
description: Stellt das Menüband-Steuerelement in der Menü Band Ansicht dar.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Menüband Element Windows-Menüband
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76ce73735d05b3d8c8cfa686f53570fd08ae6f1c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342312"
---
# <a name="ribbon-element"></a>Ribbon-Element

Stellt das Menüband-Steuerelement in der Menü Band Ansicht dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
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
<td><strong>Groupspacing</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> Zuletzt<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> Mittelalter<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Viele<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Name</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wird verwendet, um das Command-Element mit Anmerkungen zu versehen.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Eine beliebige Sequenz von NULL oder mehr Zeichen.<br/> Die maximale Länge ist unbegrenzt.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                         | BESCHREIBUNG                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Menü Band. applicationmenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Menüband. contextualtabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Menüband. HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Menüband. quickaccesstoolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Ribbon. sizedefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Kann höchstens einmal vorkommen<br/> <br/> |
| [**Menüband. Registerkarten**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Kann höchstens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss für jedes [**Application. views**](windowsribbon-element-application-views.md) -Element genau einmal auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für eine Menü **Band** Ansicht veranschaulicht.


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



 

 





