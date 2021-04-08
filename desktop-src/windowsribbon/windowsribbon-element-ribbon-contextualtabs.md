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
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="5c9b4-104">Ribbon. contextualtabs (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5c9b4-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="5c9b4-105">Stellt einen Container für kontextabhängige Registerkarten dar.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="5c9b4-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="5c9b4-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="5c9b4-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="5c9b4-107">Attributes</span></span>

<span data-ttu-id="5c9b4-108">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="5c9b4-109">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c9b4-109">Child elements</span></span>



| <span data-ttu-id="5c9b4-110">Element</span><span class="sxs-lookup"><span data-stu-id="5c9b4-110">Element</span></span>                                                       | <span data-ttu-id="5c9b4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c9b4-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="5c9b4-112">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="5c9b4-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="5c9b4-113">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="5c9b4-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="5c9b4-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5c9b4-114">Parent elements</span></span>



| <span data-ttu-id="5c9b4-115">Element</span><span class="sxs-lookup"><span data-stu-id="5c9b4-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="5c9b4-116">**Menüband**</span><span class="sxs-lookup"><span data-stu-id="5c9b4-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="5c9b4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c9b4-117">Remarks</span></span>

<span data-ttu-id="5c9b4-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-118">Optional.</span></span>

<span data-ttu-id="5c9b4-119">Kann höchstens einmal für jedes [**Menüband**](windowsribbon-element-ribbon.md)auftreten.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="5c9b4-120">Kontext Registerkarten sind nützlich zum Anzeigen von Funktionen, die nur für einen bestimmten Anwendungskontext relevant sind, z. b. eine Registerkarte für die Bild Formatierung in einem Text-Editor, der nur angezeigt wird, wenn ein Bild hervorgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="5c9b4-121">Kontext Registerkarten werden in der Regel erst angezeigt, wenn ein bestimmter Anwendungskontext auftritt, und die Anwendung benachrichtigt das Menüband-Framework.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="5c9b4-122">Wenn Sie angezeigt werden, sind Kontext Registerkarten farblich codiert, um Sie von regulären Registerkarten zu unterscheiden</span><span class="sxs-lookup"><span data-stu-id="5c9b4-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="5c9b4-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c9b4-123">Examples</span></span>

<span data-ttu-id="5c9b4-124">Im folgenden Beispiel wird das grundlegende Markup für das **Ribbon. contextualtabs** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="5c9b4-125">Dieser Code Abschnitt zeigt eine [**TabGroup**](windowsribbon-element-tabgroup.md) -Befehls Deklaration und zwei kontextabhängige [**Register**](windowsribbon-element-tab.md) Karten-Befehls Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="5c9b4-126">In diesem Code Abschnitt wird die Steuerelement Deklaration " **Ribbon. contextualtabs** " mit einer [**TabGroup**](windowsribbon-element-tabgroup.md) und zwei kontextbezogenen [**Register**](windowsribbon-element-tab.md) Karten-Steuerelementen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5c9b4-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5c9b4-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c9b4-127">Requirements</span></span>



| <span data-ttu-id="5c9b4-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c9b4-128">Requirement</span></span> | <span data-ttu-id="5c9b4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="5c9b4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5c9b4-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c9b4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9b4-131">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c9b4-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5c9b4-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c9b4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9b4-133">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c9b4-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c9b4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c9b4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9b4-135">**Menüband. Registerkarten**</span><span class="sxs-lookup"><span data-stu-id="5c9b4-135">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





