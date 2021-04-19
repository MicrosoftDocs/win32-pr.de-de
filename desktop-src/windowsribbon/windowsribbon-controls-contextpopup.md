---
title: Kontext-Popup
description: Ein Kontext-Popup ist das Prinzipal Steuerelement in der contextpopup-Ansicht des Windows-Menüband-Frameworks.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339283"
---
# <a name="context-popup"></a><span data-ttu-id="492d7-103">Kontext-Popup</span><span class="sxs-lookup"><span data-stu-id="492d7-103">Context Popup</span></span>

<span data-ttu-id="492d7-104">Ein Kontext-Popup ist das Prinzipal Steuerelement in der [**contextpopup-Ansicht**](windowsribbon-element-contextpopup.md) des Windows-Menüband-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="492d7-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="492d7-105">Es handelt sich um ein umfangreiches Kontextmenü System, das nur vom Framework als Erweiterung einer Multifunktionsleisten-Implementierung verfügbar gemacht wird – das Framework macht das Kontext-Popup nicht als unabhängiges Steuerelement verfügbar.</span><span class="sxs-lookup"><span data-stu-id="492d7-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="492d7-106">Komponenten des Kontext-Popups</span><span class="sxs-lookup"><span data-stu-id="492d7-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="492d7-107">Implementieren des Kontext-Popups</span><span class="sxs-lookup"><span data-stu-id="492d7-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="492d7-108">Markup</span><span class="sxs-lookup"><span data-stu-id="492d7-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="492d7-109">Code</span><span class="sxs-lookup"><span data-stu-id="492d7-109">Code</span></span>](#code)
-   [<span data-ttu-id="492d7-110">Kontext-Popup Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="492d7-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="492d7-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="492d7-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="492d7-112">Komponenten des Kontext-Popups</span><span class="sxs-lookup"><span data-stu-id="492d7-112">Components of the Context Popup</span></span>

<span data-ttu-id="492d7-113">Das Kontext-Popup ist ein logischer Container für das Kontextmenü und Mini-Toolbar unter Steuerelemente, die über das [**ContextMenu**](windowsribbon-element-contextmenu.md) -bzw. das [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Markup Element verfügbar gemacht werden:</span><span class="sxs-lookup"><span data-stu-id="492d7-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="492d7-114">Das [**ContextMenu-Objekt**](windowsribbon-element-contextmenu.md) stellt ein Menü mit Befehlen und Galerien bereit.</span><span class="sxs-lookup"><span data-stu-id="492d7-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="492d7-115">Die [**MiniToolbar**](windowsribbon-element-minitoolbar.md) macht eine unverankerte Symbolleiste verschiedener Befehle, Galerien und komplexer Steuerelemente verfügbar, wie z. b. das [Schriftart-Steuer](windowsribbon-controls-fontcontrol.md) Element und das Kombinations [Feld](windowsribbon-controls-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="492d7-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="492d7-116">Jede unter Kontrolle kann höchstens einmal in einem Kontext-Popup vorkommen.</span><span class="sxs-lookup"><span data-stu-id="492d7-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="492d7-117">Der folgende Screenshot veranschaulicht das Kontext-Popup und seine zugehörigen untergeordneten Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="492d7-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![Screenshot mit Legenden, die die Kontextmenü-Komponenten der Multifunktionsleiste anzeigen.](images/controls/contextpopup.png)

<span data-ttu-id="492d7-119">Das Kontext-Popup ist rein konzeptionell und macht keine Benutzeroberflächen Funktionen selbst verfügbar, wie z. b. Positionierung oder Größenanpassung.</span><span class="sxs-lookup"><span data-stu-id="492d7-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="492d7-120">Das Kontext-Popup Fenster wird in der Regel angezeigt, wenn Sie mit der rechten Maustaste auf die Maus (oder über die Tastenkombination UMSCHALT + F10) für ein interessantes Objekt klicken.</span><span class="sxs-lookup"><span data-stu-id="492d7-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="492d7-121">Die Schritte, die zum Anzeigen des Kontext-Popup erforderlich sind, werden jedoch von der Anwendung definiert.</span><span class="sxs-lookup"><span data-stu-id="492d7-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="492d7-122">Implementieren des Kontext-Popups</span><span class="sxs-lookup"><span data-stu-id="492d7-122">Implement the Context Popup</span></span>

<span data-ttu-id="492d7-123">Ähnlich wie andere Steuerelemente des Windows-Menüband-Frameworks wird das Kontext-Popup über eine Markup Komponente implementiert, die die Darstellungs Details und eine Code Komponente angibt, die ihre Funktionalität regelt.</span><span class="sxs-lookup"><span data-stu-id="492d7-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="492d7-124">In der folgenden Tabelle sind die Steuerelemente aufgelistet, die von den einzelnen Kontext-Popup unter Steuerelementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="492d7-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="492d7-125">Control</span><span class="sxs-lookup"><span data-stu-id="492d7-125">Control</span></span>                                                                  | <span data-ttu-id="492d7-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="492d7-126">Mini-Toolbar</span></span> | <span data-ttu-id="492d7-127">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="492d7-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="492d7-128">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="492d7-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="492d7-129">x</span><span class="sxs-lookup"><span data-stu-id="492d7-129">x</span></span>            | <span data-ttu-id="492d7-130">x</span><span class="sxs-lookup"><span data-stu-id="492d7-130">x</span></span>            |
| [<span data-ttu-id="492d7-131">Kontrollkästchen</span><span class="sxs-lookup"><span data-stu-id="492d7-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="492d7-132">x</span><span class="sxs-lookup"><span data-stu-id="492d7-132">x</span></span>            | <span data-ttu-id="492d7-133">x</span><span class="sxs-lookup"><span data-stu-id="492d7-133">x</span></span>            |
| [<span data-ttu-id="492d7-134">Kombinations Feld</span><span class="sxs-lookup"><span data-stu-id="492d7-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="492d7-135">x</span><span class="sxs-lookup"><span data-stu-id="492d7-135">x</span></span>            |              |
| [<span data-ttu-id="492d7-136">Dropdown Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="492d7-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="492d7-137">x</span><span class="sxs-lookup"><span data-stu-id="492d7-137">x</span></span>            | <span data-ttu-id="492d7-138">x</span><span class="sxs-lookup"><span data-stu-id="492d7-138">x</span></span>            |
| [<span data-ttu-id="492d7-139">Dropdown-Farbauswahl</span><span class="sxs-lookup"><span data-stu-id="492d7-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="492d7-140">x</span><span class="sxs-lookup"><span data-stu-id="492d7-140">x</span></span>            | <span data-ttu-id="492d7-141">x</span><span class="sxs-lookup"><span data-stu-id="492d7-141">x</span></span>            |
| [<span data-ttu-id="492d7-142">Dropdown-Katalog</span><span class="sxs-lookup"><span data-stu-id="492d7-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="492d7-143">x</span><span class="sxs-lookup"><span data-stu-id="492d7-143">x</span></span>            | <span data-ttu-id="492d7-144">x</span><span class="sxs-lookup"><span data-stu-id="492d7-144">x</span></span>            |
| [<span data-ttu-id="492d7-145">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="492d7-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="492d7-146">x</span><span class="sxs-lookup"><span data-stu-id="492d7-146">x</span></span>            |              |
| [<span data-ttu-id="492d7-147">Hilfe Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="492d7-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="492d7-148">In-Ribbon-Katalog</span><span class="sxs-lookup"><span data-stu-id="492d7-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="492d7-149">Spinner</span><span class="sxs-lookup"><span data-stu-id="492d7-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="492d7-150">Trenn Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="492d7-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="492d7-151">x</span><span class="sxs-lookup"><span data-stu-id="492d7-151">x</span></span>            | <span data-ttu-id="492d7-152">x</span><span class="sxs-lookup"><span data-stu-id="492d7-152">x</span></span>            |
| [<span data-ttu-id="492d7-153">Split Button-Katalog</span><span class="sxs-lookup"><span data-stu-id="492d7-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="492d7-154">x</span><span class="sxs-lookup"><span data-stu-id="492d7-154">x</span></span>            | <span data-ttu-id="492d7-155">x</span><span class="sxs-lookup"><span data-stu-id="492d7-155">x</span></span>            |
| [<span data-ttu-id="492d7-156">UMSCHALT Fläche</span><span class="sxs-lookup"><span data-stu-id="492d7-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="492d7-157">x</span><span class="sxs-lookup"><span data-stu-id="492d7-157">x</span></span>            | <span data-ttu-id="492d7-158">x</span><span class="sxs-lookup"><span data-stu-id="492d7-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="492d7-159">Markup</span><span class="sxs-lookup"><span data-stu-id="492d7-159">Markup</span></span>

<span data-ttu-id="492d7-160">Jedes Kontext-Popup-unter Steuerelement muss einzeln im Markup deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="492d7-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="492d7-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="492d7-161">Mini-Toolbar</span></span>

<span data-ttu-id="492d7-162">Beim Hinzufügen von Steuerelementen zu einem Kontext-Popup Mini Symbol Toolbar sollten die folgenden beiden Empfehlungen berücksichtigt werden:</span><span class="sxs-lookup"><span data-stu-id="492d7-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="492d7-163">Steuerelemente sollten stark erkennbar sein und offensichtliche Funktionen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="492d7-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="492d7-164">Vertrautheit ist Schlüssel, da Bezeichnungen und Quick Infos nicht für Mini-Toolbar Steuerelemente verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="492d7-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="492d7-165">Jeder von einem Steuerelement bereitgestellte Befehl sollte an anderer Stelle in der Menüband-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="492d7-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="492d7-166">Der Mini-Toolbar unterstützt keine Tastaturnavigation.</span><span class="sxs-lookup"><span data-stu-id="492d7-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="492d7-167">Im folgenden Beispiel wird das grundlegende Markup für ein [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Element veranschaulicht, das drei [Schalt](windowsribbon-controls-button.md) Flächen-Steuerelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="492d7-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="492d7-168">Ein [**MenuGroup**](windowsribbon-element-menugroup.md) -Element wird für jede Zeile von Steuerelementen in der Mini Symbolleiste angegeben.</span><span class="sxs-lookup"><span data-stu-id="492d7-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="492d7-169">Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="492d7-169">Context Menu</span></span>

<span data-ttu-id="492d7-170">Im folgenden Beispiel wird das grundlegende Markup für ein [**ContextMenu**](windowsribbon-element-contextmenu.md) -Element veranschaulicht, das drei [Schalt](windowsribbon-controls-button.md) Flächen-Steuerelemente enthält.</span><span class="sxs-lookup"><span data-stu-id="492d7-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="492d7-171">Jede Gruppe von Steuerelementen im [**MenuGroup**](windowsribbon-element-menugroup.md) -Element wird durch einen horizontalen Balken im Kontextmenü getrennt.</span><span class="sxs-lookup"><span data-stu-id="492d7-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="492d7-172">Obwohl ein Kontext-Popup höchstens eine der untergeordneten Steuerelemente enthalten kann, sind mehrere [**ContextMenu**](windowsribbon-element-contextmenu.md) -und [**MiniToolbar**](windowsribbon-element-minitoolbar.md) -Element Deklarationen im Menüband-Markup gültig.</span><span class="sxs-lookup"><span data-stu-id="492d7-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="492d7-173">Dadurch kann eine Anwendung verschiedene Kombinationen von Kontextmenü und Mini-Toolbar Steuerelementen basierend auf den von der Anwendung definierten Kriterien (z. b. Arbeitsbereichs Kontext) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="492d7-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="492d7-174">Weitere Informationen finden Sie unter dem [**contextmap**](windowsribbon-element-contextmap.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="492d7-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="492d7-175">Im folgenden Beispiel wird das grundlegende Markup für das [**contextpopup**](windowsribbon-element-contextpopup.md) -Element veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="492d7-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a><span data-ttu-id="492d7-176">Code</span><span class="sxs-lookup"><span data-stu-id="492d7-176">Code</span></span>

<span data-ttu-id="492d7-177">Zum Aufrufen eines Kontext-Popups wird die [**iuicontextualui:: showatlocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) -Methode aufgerufen, wenn das Fenster der Multifunktionsleiste auf oberster Ebene eine WM- \_ ContextMenu-Benachrichtigung empfängt.</span><span class="sxs-lookup"><span data-stu-id="492d7-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="492d7-178">In diesem Beispiel wird veranschaulicht, wie die WM- \_ ContextMenu-Benachrichtigung in der WndProc ()-Methode der Multifunktionsleistenanwendung behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="492d7-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="492d7-179">Im folgenden Beispiel wird veranschaulicht, wie eine Multifunktionsleistenanwendung das Kontext-Popup an einer bestimmten Bildschirmposition mithilfe der Methode [**iuicontextualui:: showatlocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="492d7-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="492d7-180">GetCurrentContext () hat den Wert, `cmdContextMap` wie im vorangehenden Markup Beispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="492d7-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="492d7-181">g \_ papplication ist ein Verweis auf die [**iuiframework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="492d7-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



<span data-ttu-id="492d7-182">Der Verweis auf [**iuicontextualui**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) kann freigegeben werden, bevor das Kontext-Popup verworfen wird, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="492d7-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="492d7-183">Allerdings muss der Verweis zu einem bestimmten Zeitpunkt freigegeben werden, um Speicher Verluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="492d7-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="492d7-184">Der Mini-Toolbar verfügt über einen integrierten Ausblend Effekt, der auf der Nähe des Mauszeigers basiert.</span><span class="sxs-lookup"><span data-stu-id="492d7-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="492d7-185">Aus diesem Grund empfiehlt es sich, die Mini-Toolbar so nah wie möglich mit dem Mauszeiger anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="492d7-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="492d7-186">Andernfalls werden die Mini-Toolbar aufgrund der in Konflikt stehenden Anzeige Mechanismen möglicherweise nicht wie erwartet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="492d7-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="492d7-187">Kontext-Popup Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="492d7-187">Context Popup Properties</span></span>

<span data-ttu-id="492d7-188">Dem Kontext-Popup Steuerelement sind keine Eigenschaften Schlüssel zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="492d7-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="492d7-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="492d7-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="492d7-190">Windows-Menüband-Steuerelement Bibliothek</span><span class="sxs-lookup"><span data-stu-id="492d7-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="492d7-191">Contextpopup-Beispiel</span><span class="sxs-lookup"><span data-stu-id="492d7-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 