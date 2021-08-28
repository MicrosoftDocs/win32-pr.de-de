---
title: Menübandelement
description: Stellt das Menüband-Steuerelement in der Menübandansicht dar.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Menübandelement Windows Menüband
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70841866ec656dc840fb467d598cc42bf919283b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630916"
---
# <a name="ribbon-element"></a>Menübandelement

Stellt das Menüband-Steuerelement in der Menübandansicht dar.

## <a name="usage"></a>Verwendung

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
<td><strong>GroupSpacing</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td><dt><span></span><span></span><strong></strong> (Klein)<br/> </dt> <dd> Standard. <br/> </dd> <dt><span></span><span></span><strong></strong> (Mittel)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Groß)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Name</strong><br/></td>
<td>xs:string<br/></td>
<td>Nein<br/></td>
<td>Wird verwendet, um das Befehlselement mit Anmerkungen zu kommentieren.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Eine beliebige Sequenz von null oder mehr Zeichen.<br/> Die maximale Länge ist ungebunden.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                                         | Beschreibung                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Ribbon.ApplicationMenu**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Kann nur einmal auftreten.<br/> <br/> |
| [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Kann nur einmal auftreten.<br/> <br/> |
| [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Kann nur einmal auftreten.<br/> <br/> |
| [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Kann nur einmal auftreten.<br/> <br/> |
| [**Ribbon.SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Kann nur einmal auftreten.<br/> <br/> |
| [**Ribbon.Tabs**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Kann nur einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                         |
|---------------------------------------------------------------------------------|
| [**Application.Views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss genau einmal für jedes [**Application.Views-Element**](windowsribbon-element-application-views.md) auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für eine **Menübandansicht** veranschaulicht.


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




* **Unterstütztes Mindestsystem:** Windows 7
* **Kann leer sein:** Nein



 

 





