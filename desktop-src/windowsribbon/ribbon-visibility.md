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
# <a name="displaying-the-ribbon"></a>Anzeigen des Menübands

Das Windows-Menüband-Framework macht eine Reihe von Eigenschaften verfügbar, die es einer Anwendung ermöglichen, anzugeben, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.

-   [Introduction (Einführung)](#introduction)
-   [Minimieren der Multifunktionsleiste](#minimize-the-ribbon)
-   [Ausblenden der Multifunktionsleiste](#hide-the-ribbon)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Um den Bereich zu maximieren, der für den Dokumentbereich (oder den Ansichts Port) einer Multifunktionsleisten-Framework-Anwendung verfügbar ist, kann eine Anwendung angeben, ob die Multifunktionsleisten-Benutzeroberfläche sichtbar oder ausgeblendet ist, und wenn Sie sichtbar ist, ob das Menüband in einem erweiterten oder reduzierten Zustand

Die in der folgenden Tabelle aufgeführten [Frameworks](windowsribbon-reference-properties-framework.md) -Eigenschaften Schlüssel werden verwendet, um die Anzeigeeigenschaften der Menüband-Benutzeroberfläche in einer Multifunktionsleisten-Framework-Anwendung explizit festzulegen. Diese Eigenschaften haben keine Auswirkung auf die Anzeige des [Kontext-Popup](windowsribbon-controls-contextpopup.md) Steuer Elements.



| Anzeige Zustand         | Menüband-Eigenschaften Schlüssel                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Erweitert oder reduziert | [UI- \_ pkey \_ minimiert](windowsribbon-reference-properties-uipkey-minimized.md) |
| Sichtbar oder ausgeblendet     | [UI- \_ pkey kann angezeigt werden. \_](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Minimieren der Multifunktionsleiste

Eine Menüband-Framework-Anwendung kann den minimierten Zustand der Multifunktionsleisten-Befehlsleiste dynamisch festlegen, indem Sie den Wert des minimierten Eigenschafts Schlüssels der [UI \_ \_ pkey](windowsribbon-reference-properties-uipkey-minimized.md) auf **true** oder **false** festlegt.



| Anzeige Zustand | Eigenschafts Schlüsselwert |
|---------------|--------------------|
| Expanded      | **false**          |
| Reduziert     | **true**           |



 

Wenn sich die Multifunktionsleisten-Benutzeroberfläche in einem minimierten Zustand befindet, bleibt die Menüband-Registerkarte sichtbar und voll funktionsfähig.

Der folgende Screenshot zeigt das Menüband im minimierten Zustand.

![Screenshot der minimierten Multifunktionsleisten-Benutzeroberfläche](images/overviews/ribbon-minimized.png)

> [!Note]  
> Das Menüband-Framework macht diese Funktionalität für den Endbenutzer über die Option "Minimieren der Multifunktionsleiste" des Menü Band Kontextmenüs verfügbar.

 

## <a name="hide-the-ribbon"></a>Ausblenden der Multifunktionsleiste

Eine Menüband-Framework-Anwendung kann den anzeigbaren Zustand der Multifunktionsleisten-Befehlsleiste dynamisch festlegen, indem Sie den Wert des Benutzeroberflächen- [ \_ pkey \_](windowsribbon-reference-properties-uipkey-viewable.md) -Eigenschafts Schlüssels auf **true** oder **false** festlegt.



| Anzeige Zustand | Eigenschafts Schlüsselwert |
|---------------|--------------------|
| Sichtbar       | **false**          |
| Ausgeblendet        | **true**           |



 

Im Gegensatz zur [ \_ \_ minimierten Eigenschaft UI pkey](windowsribbon-reference-properties-uipkey-minimized.md) wird durch Festlegen von [UI \_ pkey \_](windowsribbon-reference-properties-uipkey-viewable.md) auf **false** die Multifunktionsleisten-Benutzeroberfläche unsichtbar und vollständig für einen Endbenutzer unbrauchbar.

Der folgende Screenshot zeigt das Menüband im ausgeblendeten Zustand.

![Screenshot, in dem die Menüband-Benutzeroberfläche ausgeblendet ist](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie der Zustand der Menüband-Benutzeroberfläche zur Laufzeit festgelegt wird.

In diesem Fall wird die [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Funktion verwendet, um die Menüband-Benutzeroberfläche basierend auf dem UMSCHALT Zustand einer [UMSCHALT Fläche](windowsribbon-controls-togglebutton.md)zu erweitern oder zu reduzieren.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Menü Band Eigenschaften](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 