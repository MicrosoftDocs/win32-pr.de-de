---
title: Anzeigen des Menübands
description: Das Windows-Menüband-Framework macht eine Reihe von Eigenschaften verfügbar, die es einer Anwendung ermöglichen, anzugeben, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Windows-Menüband, Anpassen von Farben
- Multifunktionsleiste, Anpassen von Farben
- Anpassen von Windows-Menü Band Farben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039282"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="5c3b4-106">Anzeigen des Menübands</span><span class="sxs-lookup"><span data-stu-id="5c3b4-106">Displaying the Ribbon</span></span>

<span data-ttu-id="5c3b4-107">Das Windows-Menüband-Framework macht eine Reihe von Eigenschaften verfügbar, die es einer Anwendung ermöglichen, anzugeben, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="5c3b4-108">Introduction (Einführung)</span><span class="sxs-lookup"><span data-stu-id="5c3b4-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="5c3b4-109">Minimieren der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="5c3b4-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="5c3b4-110">Ausblenden der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="5c3b4-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="5c3b4-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5c3b4-111">Example</span></span>](#example)
-   [<span data-ttu-id="5c3b4-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c3b4-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="5c3b4-113">Einführung</span><span class="sxs-lookup"><span data-stu-id="5c3b4-113">Introduction</span></span>

<span data-ttu-id="5c3b4-114">Um den Bereich zu maximieren, der für den Dokumentbereich (oder den Ansichts Port) einer Multifunktionsleisten-Framework-Anwendung verfügbar ist, kann eine Anwendung angeben, ob die Multifunktionsleisten-Benutzeroberfläche sichtbar oder ausgeblendet ist, und wenn Sie sichtbar ist, ob das Menüband in einem erweiterten oder reduzierten Zustand</span><span class="sxs-lookup"><span data-stu-id="5c3b4-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="5c3b4-115">Die in der folgenden Tabelle aufgeführten [Frameworks](windowsribbon-reference-properties-framework.md) -Eigenschaften Schlüssel werden verwendet, um die Anzeigeeigenschaften der Menüband-Benutzeroberfläche in einer Multifunktionsleisten-Framework-Anwendung explizit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="5c3b4-116">Diese Eigenschaften haben keine Auswirkung auf die Anzeige des [Kontext-Popup](windowsribbon-controls-contextpopup.md) Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="5c3b4-117">Anzeige Zustand</span><span class="sxs-lookup"><span data-stu-id="5c3b4-117">Display State</span></span>         | <span data-ttu-id="5c3b4-118">Menüband-Eigenschaften Schlüssel</span><span class="sxs-lookup"><span data-stu-id="5c3b4-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5c3b4-119">Erweitert oder reduziert</span><span class="sxs-lookup"><span data-stu-id="5c3b4-119">Expanded or collapsed</span></span> | [<span data-ttu-id="5c3b4-120">UI- \_ pkey \_ minimiert</span><span class="sxs-lookup"><span data-stu-id="5c3b4-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="5c3b4-121">Sichtbar oder ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="5c3b4-121">Visible or hidden</span></span>     | [<span data-ttu-id="5c3b4-122">UI- \_ pkey kann angezeigt werden. \_</span><span class="sxs-lookup"><span data-stu-id="5c3b4-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="5c3b4-123">Minimieren der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="5c3b4-123">Minimize the Ribbon</span></span>

<span data-ttu-id="5c3b4-124">Eine Menüband-Framework-Anwendung kann den minimierten Zustand der Multifunktionsleisten-Befehlsleiste dynamisch festlegen, indem Sie den Wert des minimierten Eigenschafts Schlüssels der [UI \_ \_ pkey](windowsribbon-reference-properties-uipkey-minimized.md) auf **true** oder **false** festlegt.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="5c3b4-125">Anzeige Zustand</span><span class="sxs-lookup"><span data-stu-id="5c3b4-125">Display State</span></span> | <span data-ttu-id="5c3b4-126">Eigenschafts Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="5c3b4-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="5c3b4-127">Expanded</span><span class="sxs-lookup"><span data-stu-id="5c3b4-127">Expanded</span></span>      | <span data-ttu-id="5c3b4-128">**false**</span><span class="sxs-lookup"><span data-stu-id="5c3b4-128">**false**</span></span>          |
| <span data-ttu-id="5c3b4-129">Reduziert</span><span class="sxs-lookup"><span data-stu-id="5c3b4-129">Collapsed</span></span>     | <span data-ttu-id="5c3b4-130">**true**</span><span class="sxs-lookup"><span data-stu-id="5c3b4-130">**true**</span></span>           |



 

<span data-ttu-id="5c3b4-131">Wenn sich die Multifunktionsleisten-Benutzeroberfläche in einem minimierten Zustand befindet, bleibt die Menüband-Registerkarte sichtbar und voll funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="5c3b4-132">Der folgende Screenshot zeigt das Menüband im minimierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![Screenshot der minimierten Multifunktionsleisten-Benutzeroberfläche](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="5c3b4-134">Das Menüband-Framework macht diese Funktionalität für den Endbenutzer über die Option "Minimieren der Multifunktionsleiste" des Menü Band Kontextmenüs verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="5c3b4-135">Ausblenden der Multifunktionsleiste</span><span class="sxs-lookup"><span data-stu-id="5c3b4-135">Hide the Ribbon</span></span>

<span data-ttu-id="5c3b4-136">Eine Menüband-Framework-Anwendung kann den anzeigbaren Zustand der Multifunktionsleisten-Befehlsleiste dynamisch festlegen, indem Sie den Wert des Benutzeroberflächen- [ \_ pkey \_](windowsribbon-reference-properties-uipkey-viewable.md) -Eigenschafts Schlüssels auf **true** oder **false** festlegt.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="5c3b4-137">Anzeige Zustand</span><span class="sxs-lookup"><span data-stu-id="5c3b4-137">Display State</span></span> | <span data-ttu-id="5c3b4-138">Eigenschafts Schlüsselwert</span><span class="sxs-lookup"><span data-stu-id="5c3b4-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="5c3b4-139">Sichtbar</span><span class="sxs-lookup"><span data-stu-id="5c3b4-139">Visible</span></span>       | <span data-ttu-id="5c3b4-140">**false**</span><span class="sxs-lookup"><span data-stu-id="5c3b4-140">**false**</span></span>          |
| <span data-ttu-id="5c3b4-141">Ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="5c3b4-141">Hidden</span></span>        | <span data-ttu-id="5c3b4-142">**true**</span><span class="sxs-lookup"><span data-stu-id="5c3b4-142">**true**</span></span>           |



 

<span data-ttu-id="5c3b4-143">Im Gegensatz zur [ \_ \_ minimierten Eigenschaft UI pkey](windowsribbon-reference-properties-uipkey-minimized.md) wird durch Festlegen von [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-viewable.md) auf **false** die Multifunktionsleisten-Benutzeroberfläche unsichtbar und vollständig für einen Endbenutzer unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="5c3b4-144">Der folgende Screenshot zeigt das Menüband im ausgeblendeten Zustand.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![Screenshot, in dem die Menüband-Benutzeroberfläche ausgeblendet ist](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="5c3b4-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5c3b4-146">Example</span></span>

<span data-ttu-id="5c3b4-147">Im folgenden Beispiel wird veranschaulicht, wie der Zustand der Menüband-Benutzeroberfläche zur Laufzeit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="5c3b4-148">In diesem Fall wird die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Funktion verwendet, um die Menüband-Benutzeroberfläche basierend auf dem UMSCHALT Zustand einer [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md)zu erweitern oder zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="5c3b4-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="5c3b4-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c3b4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c3b4-150">Menü Band Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5c3b4-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 