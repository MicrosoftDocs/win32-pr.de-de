---
title: Anzeigen kontextbezogener Registerkarten
description: In einer Windows-Menü Band Framework-Anwendung ist eine Kontext Registerkarte ein ausgeblendetes Registerkarten-Steuerelement, das in der Registerkarten Zeile angezeigt wird, wenn ein Objekt im Anwendungs Arbeitsbereich (z. b. ein Bild) ausgewählt oder markiert
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Windows-Multifunktionsleiste, Kontext Registerkarten
- Menüband, kontextbezogene Registerkarten
- Anzeigen von kontextbezogenen Windows-Menüband
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727368"
---
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="f3b16-106">Anzeigen kontextbezogener Registerkarten</span><span class="sxs-lookup"><span data-stu-id="f3b16-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="f3b16-107">In einer Windows-Menü Band Framework-Anwendung ist eine Kontext Registerkarte ein ausgeblendetes [Register](windowsribbon-controls-tab.md) Karten-Steuerelement, das in der Registerkarten Zeile angezeigt wird, wenn ein Objekt im Anwendungs Arbeitsbereich (z. b. ein Bild) ausgewählt oder markiert</span><span class="sxs-lookup"><span data-stu-id="f3b16-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="f3b16-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="f3b16-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="f3b16-109">Implementieren kontextbezogener Registerkarten</span><span class="sxs-lookup"><span data-stu-id="f3b16-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="f3b16-110">Markup</span><span class="sxs-lookup"><span data-stu-id="f3b16-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="f3b16-111">Code</span><span class="sxs-lookup"><span data-stu-id="f3b16-111">Code</span></span>](#code)
-   [<span data-ttu-id="f3b16-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3b16-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="f3b16-113">Einführung</span><span class="sxs-lookup"><span data-stu-id="f3b16-113">Introduction</span></span>

<span data-ttu-id="f3b16-114">Im Gegensatz zu Kern Registerkarten, die verschiedene allgemeine Befehle enthalten, die unabhängig vom Arbeitsbereichs Kontext relevant sind, enthalten kontextabhängige Registerkarten in der Regel mindestens einen Befehl, der nur für ein ausgewähltes oder hervorgehobenes Objekt anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="f3b16-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="f3b16-115">Wenn ein Objekt ausgewählt oder im Arbeitsbereich Anwendung hervorgehoben wird, sind für den Typ und den Kontext des Objekts möglicherweise unterschiedliche Befehle erforderlich, die auf einer Kontext Registerkarte keine Organisations-oder funktionale Bedeutung haben. In diesen Fällen sind möglicherweise mehrere kontextabhängige Registerkarten, die in einer [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md)enthalten sind, erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f3b16-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="f3b16-116">Wenn Sie z. b. ein Bild auswählen, das in einer Tabellenzelle enthalten ist, sind möglicherweise zwei Kontext Registerkarten erforderlich, auf denen sowohl die Tabellen-</span><span class="sxs-lookup"><span data-stu-id="f3b16-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="f3b16-117">Zusätzlich zu mehreren kontextbezogenen Registerkarten unterstützt das Menüband-Framework auch mehrere Registerkarten- [Gruppen](windowsribbon-controls-tabgroup.md) Steuerelemente in einem Menüband.</span><span class="sxs-lookup"><span data-stu-id="f3b16-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="f3b16-118">Beim Anzeigen kontextbezogener Registerkarten erzwingt das Menüband-Framework einen grundlegenden Satz von Verhalten, die Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="f3b16-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="f3b16-119">Kontext Registerkarten werden in der Reihenfolge positioniert, in der Sie deklariert werden, und rechts von den Haupt Registerkarten in der Zeile der Multifunktionsleiste.</span><span class="sxs-lookup"><span data-stu-id="f3b16-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="f3b16-120">Wenn die Größe des Menübands geändert wird, werden Registerkarten skaliert und Registerkarten Bezeichnungen abgeschnitten, wenn der Speicherplatz erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f3b16-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="f3b16-121">Sichtbare Kontext Registerkarten erhalten jedoch eine höhere Anzeige Priorität, in der Sie zuletzt skaliert und abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="f3b16-122">Die Bezeichnung für eine [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md) wird in der Titelleiste der Anwendung angezeigt und umfasst alle zugeordneten Kontext Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="f3b16-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="f3b16-123">Wenn mehrere [Register](windowsribbon-controls-tabgroup.md) Karten-Gruppen Steuerelemente gleichzeitig angezeigt werden, wird eine von fünf eindeutigen Farben dem Hintergrund der einzelnen Registerkarten Gruppen in der Titelleiste der Anwendung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="f3b16-124">Diese Farbe wird auch als Hervorhebungs Farbe für die Kontext Registerkarten in der Registerkarten Gruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3b16-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="f3b16-125">Die Farb Zuweisung der [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md) basiert auf der Reihenfolge, in der die Registerkarten Gruppenelemente im Markup deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="f3b16-126">Die Farben werden durch das Framework definiert und können nicht von der Anwendung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="f3b16-127">Die vom Framework definierten Registerkarten- [Gruppen](windowsribbon-controls-tabgroup.md) Farben können indirekt über die Eigenschaften Schlüssel der [Frameworkeigenschaften](windowsribbon-reference-properties-framework.md) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="f3b16-128">Weitere Informationen finden Sie unter [Anpassen von Menüband-Farben](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="f3b16-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="f3b16-129">Wenn zu einem beliebigen Zeitpunkt mehr als fünf Registerkarten- [Gruppen](windowsribbon-controls-tabgroup.md) Steuerelemente angezeigt werden, werden die zugeordneten Farben von dem Framework in den einzelnen Zyklen</span><span class="sxs-lookup"><span data-stu-id="f3b16-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="f3b16-130">Die maximale Anzahl von [Register](windowsribbon-controls-tab.md) Karten-Steuerelementen in einem Menüband ist auf 100 beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f3b16-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="f3b16-131">Dies schließt kontextabhängige Registerkarten ein, die sichtbar sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f3b16-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="f3b16-132">Der folgende Screenshot zeigt eine Kontext Registerkarte aus Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="f3b16-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![Screenshot, der ein Kontext abhängiges Registerkarten-Steuerelement anzeigt.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="f3b16-134">Implementieren kontextbezogener Registerkarten</span><span class="sxs-lookup"><span data-stu-id="f3b16-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="f3b16-135">In diesem Abschnitt werden die Implementierungsdetails der Kontext Registerkarten des Menübands erläutert und erläutert, wie Sie in eine Menü Bandanwendung integriert werden.</span><span class="sxs-lookup"><span data-stu-id="f3b16-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="f3b16-136">Markup</span><span class="sxs-lookup"><span data-stu-id="f3b16-136">Markup</span></span>

<span data-ttu-id="f3b16-137">In den folgenden Beispielen wird das grundlegende Markup für ein [**TabGroup**](windowsribbon-element-tabgroup.md) -Element veranschaulicht, das zwei kontextabhängige Registerkarten enthält.</span><span class="sxs-lookup"><span data-stu-id="f3b16-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="f3b16-138">In diesem Code Abschnitt werden die Befehls Deklarationen [**TabGroup**](windowsribbon-element-tabgroup.md) und [Tab](windowsribbon-controls-tab.md) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f3b16-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="f3b16-139">In diesem Code Abschnitt werden die Steuerelement Deklarationen veranschaulicht, die erforderlich sind, um zwei Kontext Registerkarten innerhalb einer [**TabGroup**](windowsribbon-element-tabgroup.md)anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f3b16-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


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



### <a name="code"></a><span data-ttu-id="f3b16-140">Code</span><span class="sxs-lookup"><span data-stu-id="f3b16-140">Code</span></span>

<span data-ttu-id="f3b16-141">[Benutzeroberfläche \_ Pkey \_ contextavailable](windowsribbon-reference-properties-uipkey-contextavailable.md) ist der einzige Eigenschafts Schlüssel, der durch das Framework definiert wird, um die Sichtbarkeit und den Zustand von kontextbezogenen Registerkarten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3b16-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="f3b16-142">Wenn ein Objekt im Anwendungs Arbeitsbereich ausgewählt wird, kann dieser Eigenschaft einer von drei Werten aus der [**UI \_ contextavailability**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) -Enumeration zugewiesen werden, die festlegt, ob eine kontextabhängige Registerkarte vorhanden ist, und wenn dies der Fall ist, ob Sie als aktive Registerkarte angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f3b16-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="f3b16-143">Eine Anwendung fordert ein Update der [Registerkarten Gruppe](windowsribbon-controls-tabgroup.md) an, indem Sie die [UI \_ pkey \_ contextavailable](windowsribbon-reference-properties-uipkey-contextavailable.md) -Eigenschaft für ungültig erklärt und aktualisiert, wenn der Arbeitsbereichs Kontext geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f3b16-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="f3b16-144">In den folgenden Code Abschnitten wird veranschaulicht, wie eine Kontext Registerkarte angezeigt wird, wenn ein Bild in einem Anwendungs Arbeitsbereich ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="f3b16-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f3b16-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3b16-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b16-146">Multifunktionsleisten-Benutzeroberflächen Richtlinien</span><span class="sxs-lookup"><span data-stu-id="f3b16-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="f3b16-147">Menüband-Entwurfsprozess</span><span class="sxs-lookup"><span data-stu-id="f3b16-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 