---
title: TabGroup-Element
description: Stellt einen kontextbezogenen Satz von Tabulatorsteuerelementen dar.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- TabGroup-Element Windows-Menüband
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4c18db72d6b0161842bfde9d5a836d14189c6a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444061"
---
# <a name="tabgroup-element"></a><span data-ttu-id="2d06e-104">TabGroup-Element</span><span class="sxs-lookup"><span data-stu-id="2d06e-104">TabGroup element</span></span>

<span data-ttu-id="2d06e-105">Stellt einen kontextbezogenen Satz von [Tabulatorsteuerelementen](windowsribbon-controls-tabgroup.md) dar.</span><span class="sxs-lookup"><span data-stu-id="2d06e-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="2d06e-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="2d06e-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="2d06e-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="2d06e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2d06e-108">attribute</span><span class="sxs-lookup"><span data-stu-id="2d06e-108">Attribute</span></span></th>
<th><span data-ttu-id="2d06e-109">Typ</span><span class="sxs-lookup"><span data-stu-id="2d06e-109">Type</span></span></th>
<th><span data-ttu-id="2d06e-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2d06e-110">Required</span></span></th>
<th><span data-ttu-id="2d06e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d06e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2d06e-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2d06e-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2d06e-113">xs:positiveInteger oder xs:string</span><span class="sxs-lookup"><span data-stu-id="2d06e-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2d06e-114">Nein</span><span class="sxs-lookup"><span data-stu-id="2d06e-114">No</span></span><br/></td>
<td><span data-ttu-id="2d06e-115">Ordnet das Element einem <a href="windowsribbon-element-command.md"><strong>Command zu.</strong></a></span><span class="sxs-lookup"><span data-stu-id="2d06e-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2d06e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger oder xs:string)</span><span class="sxs-lookup"><span data-stu-id="2d06e-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2d06e-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999 einschließlich oder ein Hexadezimalwert zwischen 0x2 und 0xea5f einschließlich.</span><span class="sxs-lookup"><span data-stu-id="2d06e-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2d06e-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2d06e-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2d06e-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2d06e-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2d06e-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d06e-120">Child elements</span></span>



| <span data-ttu-id="2d06e-121">Element</span><span class="sxs-lookup"><span data-stu-id="2d06e-121">Element</span></span>                                             | <span data-ttu-id="2d06e-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2d06e-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2d06e-123">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="2d06e-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="2d06e-124">Muss mindestens einmal auftreten.</span><span class="sxs-lookup"><span data-stu-id="2d06e-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2d06e-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2d06e-125">Parent elements</span></span>



| <span data-ttu-id="2d06e-126">Element</span><span class="sxs-lookup"><span data-stu-id="2d06e-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d06e-127">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="2d06e-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2d06e-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d06e-128">Remarks</span></span>

<span data-ttu-id="2d06e-129">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d06e-129">Required.</span></span>

<span data-ttu-id="2d06e-130">Muss mindestens einmal für jedes [**Ribbon.ContextualTabs-Element**](windowsribbon-element-ribbon-contextualtabs.md) auftreten.</span><span class="sxs-lookup"><span data-stu-id="2d06e-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="2d06e-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d06e-131">Examples</span></span>

<span data-ttu-id="2d06e-132">Im folgenden Beispiel wird das grundlegende Markup für das **TabGroup-Element** veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="2d06e-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="2d06e-133">Dieser Codeabschnitt zeigt eine **TabGroup-Befehlsdeklaration** mit zwei kontextbezogenen Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="2d06e-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


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



<span data-ttu-id="2d06e-134">Dieser Codeabschnitt zeigt die entsprechenden **TabGroup-Steuerelementdeklarationen.**</span><span class="sxs-lookup"><span data-stu-id="2d06e-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="2d06e-135">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="2d06e-135">Element information</span></span>

- <span data-ttu-id="2d06e-136">**Unterstütztes Mindestsystem:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d06e-136">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="2d06e-137">**Kann leer sein:** Nein</span><span class="sxs-lookup"><span data-stu-id="2d06e-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="2d06e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d06e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d06e-139">Registerkartengruppen-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2d06e-139">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="2d06e-140">Registersteuerelement</span><span class="sxs-lookup"><span data-stu-id="2d06e-140">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





