---
title: TabGroup-Element
description: Stellt einen kontextbezogenen Satz von Tabulatorsteuerelementen dar.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- TabGroup-Element Windows Menüband
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd2d2109abd92f791a14c5d2ba19fc7eaecd73e7f2718623100c6ec3eb0e1e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706870"
---
# <a name="tabgroup-element"></a>TabGroup-Element

Stellt einen kontextbezogenen Satz von [Tabulatorsteuerelementen](windowsribbon-controls-tabgroup.md) dar.

## <a name="usage"></a>Verbrauch

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
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
<th>attribute</th>
<th>type</th>
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



| Element                                             | Beschreibung                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**Registerkarte**](windowsribbon-element-tab.md)<br/> | Muss mindestens einmal auftreten.<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                                                 |
|-----------------------------------------------------------------------------------------|
| [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a>Hinweise

Erforderlich.

Muss mindestens einmal für jedes [**Ribbon.ContextualTabs-Element**](windowsribbon-element-ribbon-contextualtabs.md) auftreten.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **TabGroup-Element** veranschaulicht.

Dieser Codeabschnitt zeigt eine **TabGroup** Command-Deklaration mit zwei kontextbezogenen Registerkarten.


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



In diesem Codeabschnitt werden die entsprechenden **TabGroup-Steuerelementdeklarationen** angezeigt.


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="element-information"></a>Elementinformationen

- **Unterstütztes Mindestsystem:** Windows 7 
- **Kann leer sein:** Nein



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Registerkartengruppen-Steuerelement](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[Registersteuerelement](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





