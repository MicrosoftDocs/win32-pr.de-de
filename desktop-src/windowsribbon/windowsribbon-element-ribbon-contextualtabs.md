---
title: Ribbon. contextualtabs (Eigenschaft)
description: Stellt einen Container für kontextabhängige Registerkarten dar.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Menüband. contextualtabs-Eigenschaften Fenster (Menüband)
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740536"
---
# <a name="ribboncontextualtabs-property"></a>Ribbon. contextualtabs (Eigenschaft)

Stellt einen Container für kontextabhängige Registerkarten dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                       | BESCHREIBUNG                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/> | Muss mindestens einmal vorkommen<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                                   |
|-----------------------------------------------------------|
| [**Menüband**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist optional.

Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.

Kontext Registerkarten sind nützlich zum Anzeigen von Funktionen, die nur für einen bestimmten Anwendungskontext relevant sind, z. b. eine Registerkarte für die Bild Formatierung in einem Text-Editor, der nur angezeigt wird, wenn ein Bild hervorgehoben wird. Kontext Registerkarten werden in der Regel erst angezeigt, wenn ein bestimmter Anwendungskontext auftritt, und die Anwendung benachrichtigt das Menüband-Framework.

Wenn Sie angezeigt werden, sind Kontext Registerkarten farblich codiert, um Sie von regulären Registerkarten zu unterscheiden

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird das grundlegende Markup für das **Ribbon. contextualtabs** -Element veranschaulicht.

Dieser Code Abschnitt zeigt eine [**TabGroup**](windowsribbon-element-tabgroup.md) -Befehls Deklaration und zwei kontextabhängige [**Register**](windowsribbon-element-tab.md) Karten-Befehls Deklarationen.


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



In diesem Code Abschnitt wird die Steuerelement Deklaration " **Ribbon. contextualtabs** " mit einer [**TabGroup**](windowsribbon-element-tabgroup.md) und zwei kontextbezogenen [**Register**](windowsribbon-element-tab.md) Karten-Steuerelementen angezeigt.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Menüband. Registerkarten**](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





