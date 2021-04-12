---
title: TabGroup-Element
description: Stellt eine Kontext Gruppe von Registerkarten-Steuerelementen dar.
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
ms.openlocfilehash: fcbe0760c850f37c6a7bf348c38e48aa7cf54ddc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104208365"
---
# <a name="tabgroup-element"></a><span data-ttu-id="fc406-104">TabGroup-Element</span><span class="sxs-lookup"><span data-stu-id="fc406-104">TabGroup element</span></span>

<span data-ttu-id="fc406-105">Stellt eine Kontext Gruppe von [Register](windowsribbon-controls-tabgroup.md) Karten-Steuerelementen dar.</span><span class="sxs-lookup"><span data-stu-id="fc406-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="fc406-106">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="fc406-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="fc406-107">Attribute</span><span class="sxs-lookup"><span data-stu-id="fc406-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc406-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="fc406-108">Attribute</span></span></th>
<th><span data-ttu-id="fc406-109">type</span><span class="sxs-lookup"><span data-stu-id="fc406-109">Type</span></span></th>
<th><span data-ttu-id="fc406-110">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fc406-110">Required</span></span></th>
<th><span data-ttu-id="fc406-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc406-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fc406-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="fc406-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="fc406-113">xs: positiveingeteger oder xs: String</span><span class="sxs-lookup"><span data-stu-id="fc406-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="fc406-114">Nein</span><span class="sxs-lookup"><span data-stu-id="fc406-114">No</span></span><br/></td>
<td><span data-ttu-id="fc406-115">Ordnet das-Element einem <a href="windowsribbon-element-command.md"><strong>Befehl</strong></a>zu.</span><span class="sxs-lookup"><span data-stu-id="fc406-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="fc406-116">
<dt><span></span><span></span><strong></strong> (xs: positiveingeteger oder xs: String)</span><span class="sxs-lookup"><span data-stu-id="fc406-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fc406-117">Eine Zeichenfolge, ein ganzzahliger Wert zwischen 2 und 59999, einschließlich, oder ein Hexadezimalwert zwischen 0x2 und 0xea5f (einschließlich).</span><span class="sxs-lookup"><span data-stu-id="fc406-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="fc406-118">Der Wert muss innerhalb des Menüband-XML-Dokuments eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="fc406-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="fc406-119">Maximale Länge: 100 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="fc406-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fc406-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc406-120">Child elements</span></span>



| <span data-ttu-id="fc406-121">Element</span><span class="sxs-lookup"><span data-stu-id="fc406-121">Element</span></span>                                             | <span data-ttu-id="fc406-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc406-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="fc406-123">**Registerkarte**</span><span class="sxs-lookup"><span data-stu-id="fc406-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="fc406-124">Muss mindestens einmal vorkommen</span><span class="sxs-lookup"><span data-stu-id="fc406-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fc406-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc406-125">Parent elements</span></span>



| <span data-ttu-id="fc406-126">Element</span><span class="sxs-lookup"><span data-stu-id="fc406-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc406-127">**Menüband. contextualtabs**</span><span class="sxs-lookup"><span data-stu-id="fc406-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fc406-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc406-128">Remarks</span></span>

<span data-ttu-id="fc406-129">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fc406-129">Required.</span></span>

<span data-ttu-id="fc406-130">Für jedes [**Ribbon. contextualtabs**](windowsribbon-element-ribbon-contextualtabs.md) -Element muss mindestens einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fc406-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="fc406-131">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc406-131">Examples</span></span>

<span data-ttu-id="fc406-132">Im folgenden Beispiel wird das grundlegende Markup für das **TabGroup** -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fc406-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="fc406-133">In diesem Code Abschnitt wird eine **TabGroup** -Befehls Deklaration mit zwei kontextbezogenen Registerkarten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc406-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


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



<span data-ttu-id="fc406-134">In diesem Code Abschnitt werden die entsprechenden **TabGroup** -Steuerelement Deklarationen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fc406-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="fc406-135">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="fc406-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="fc406-136">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="fc406-136">Minimum supported system</span></span><br/> | <span data-ttu-id="fc406-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc406-137">Windows 7</span></span> |
| <span data-ttu-id="fc406-138">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="fc406-138">Can be empty</span></span>                        | <span data-ttu-id="fc406-139">Nein</span><span class="sxs-lookup"><span data-stu-id="fc406-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="fc406-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fc406-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc406-141">Registerkarten-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fc406-141">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="fc406-142">Registersteuerelement</span><span class="sxs-lookup"><span data-stu-id="fc406-142">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





