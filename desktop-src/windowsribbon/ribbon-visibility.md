---
title: Anzeigen des Menübands
description: Das Windows Menübandframework macht einen Satz von Eigenschaften verfügbar, mit denen eine Anwendung angeben kann, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Windows Menüband, Anpassen von Farben
- Menüband, Anpassen von Farben
- Anpassen von Windows Menübandfarben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b61bae9bae5620d556f26f6c7103ef222f14892c8ce12acd21289dd7bc53b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964433"
---
# <a name="displaying-the-ribbon"></a>Anzeigen des Menübands

Das Windows Menübandframework macht einen Satz von Eigenschaften verfügbar, mit denen eine Anwendung angeben kann, wie die Menüband-Benutzeroberfläche zur Laufzeit angezeigt wird.

-   [Introduction (Einführung)](#introduction)
-   [Minimieren des Menübands](#minimize-the-ribbon)
-   [Ausblenden des Menübands](#hide-the-ribbon)
-   [Beispiel](#example)
-   [Zugehörige Themen](#related-topics)

## <a name="introduction"></a>Einführung

Um den für den Dokumentbereich (oder Ansichtsport) einer Menübandframeworkanwendung verfügbaren Bereich zu maximieren, kann eine Anwendung angeben, ob die Menübandbenutzeroberfläche sichtbar oder ausgeblendet ist und ob sich das Menüband in einem erweiterten oder reduzierten Zustand befindet, wenn es angezeigt wird.

Die [in der folgenden Tabelle](windowsribbon-reference-properties-framework.md) aufgeführten Framework-Eigenschaftsschlüssel werden verwendet, um die Anzeigemerkmale der Menübandbenutzeroberfläche in einer Menübandframeworkanwendung explizit fest zu legen. Diese Eigenschaften haben keine Auswirkungen auf die Anzeige des [Kontext-Popup-Steuerelements.](windowsribbon-controls-contextpopup.md)



| Anzeigezustand         | Menüband-Eigenschaftsschlüssel                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| Erweitert oder reduziert | [UI \_ PKEY \_ Minimiert](windowsribbon-reference-properties-uipkey-minimized.md) |
| Sichtbar oder ausgeblendet     | [UI \_ PKEY \_ Viewable](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a>Minimieren des Menübands

Eine Menübandframeworkanwendung kann den minimierten Zustand der Menübandbefehlsleiste dynamisch festlegen, indem  der Wert des [ \_ \_ PKEY-Eigenschaftsschlüssels](windowsribbon-reference-properties-uipkey-minimized.md) für die Benutzeroberfläche auf TRUE oder FALSE festgelegt **wird.**



| Anzeigezustand | Eigenschaftsschlüsselwert |
|---------------|--------------------|
| Expanded      | **false**          |
| Reduziert     | **true**           |



 

Wenn sich die Menübandbenutzeroberfläche in einem minimierten Zustand befindet, bleibt die Registerkartenzeile des Menübands sichtbar und voll funktionsfähig.

Der folgende Screenshot zeigt das Menüband im minimierten Zustand.

![Screenshot mit minimierter Menübandbenutzeroberfläche.](images/overviews/ribbon-minimized.png)

> [!Note]  
> Das Menübandframework macht diese Funktionalität dem Endbenutzer über die Auswahl "Menüband minimieren" des Menübandkontextmenüs verfügbar.

 

## <a name="hide-the-ribbon"></a>Ausblenden des Menübands

Eine Menübandframeworkanwendung kann den anzeigebaren Zustand der Menübandbefehlsleiste dynamisch festlegen, indem der Wert des [ \_ PKEY \_ Viewable-Eigenschaftsschlüssels](windowsribbon-reference-properties-uipkey-viewable.md) der Benutzeroberfläche auf **true** oder **false festgelegt wird.**



| Anzeigezustand | Eigenschaftsschlüsselwert |
|---------------|--------------------|
| Sichtbar       | **false**          |
| Ausgeblendet        | **true**           |



 

Im Gegensatz zur [ \_ \_ PKEY-Minimiert-Eigenschaft](windowsribbon-reference-properties-uipkey-minimized.md) der Benutzeroberfläche wird die Menübandbenutzeroberfläche durch Festlegen von [UI \_ PKEY \_ Viewable](windowsribbon-reference-properties-uipkey-viewable.md) auf **FALSE** unsichtbar und für einen Endbenutzer vollständig unbrauchbar.

Der folgende Screenshot zeigt das Menüband im ausgeblendeten Zustand.

![Screenshot der ausgeblendeten Menübandbenutzeroberfläche.](images/overviews/ribbon-viewable.png)

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie der Zustand der Menübandbenutzeroberfläche zur Laufzeit festgelegt wird.

In diesem Fall wird die [**IUICommandHandler::Execute-Funktion**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) verwendet, um die Menübandbenutzeroberfläche basierend auf dem Umschaltzustand einer Umschaltfläche zu erweitern [oder zu reduzieren.](windowsribbon-controls-togglebutton.md)


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

[Menübandeigenschaften](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 