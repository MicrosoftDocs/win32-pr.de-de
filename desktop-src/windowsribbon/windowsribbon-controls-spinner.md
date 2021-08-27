---
title: Spinner
description: Der Spinner ist ein zusammengesetztes Steuerelement, das aus einer Inkrementschaltfläche, einer Dekrementschaltfläche und einem Bearbeitungssteuerfeld besteht, die alle zum Bereitstellen von Dezimalwerten für die Anwendung verwendet werden.
ms.assetid: 63689ed3-7326-4f7a-b700-d89e9b501ef1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56103db221dfb8cc60783da20cf33a82c95ea17f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473766"
---
# <a name="spinner"></a>Spinner

Der Spinner ist ein zusammengesetztes Steuerelement, das aus einer Inkrementschaltfläche, einer Dekrementschaltfläche und einem Bearbeitungssteuerfeld besteht, die alle zum Bereitstellen von Dezimalwerten für die Anwendung verwendet werden.

-   [Details](#details)
-   [Spinnereigenschaften](#spinner-properties)
-   [Anmerkungen](#remarks)
-   [Zugehörige Themen](#related-topics)

## <a name="details"></a>Details

Der folgende Screenshot veranschaulicht das Menüband-Spinner.

![Screenshot eines Spinner-Steuerelements im Windows-Live-Moviemaker-Menüband.](images/controls/spinner.png)

## <a name="spinner-properties"></a>Spinnereigenschaften

Das Menübandframework definiert eine Auflistung von [Eigenschaftsschlüsseln](windowsribbon-reference-properties.md) für das Spinner-Steuerelement.

In der Regel wird eine Spinner-Eigenschaft in der Menübandbenutzeroberfläche aktualisiert, indem der befehl, der dem Steuerelement zugeordnet ist, durch einen Aufruf der [**IUIFramework::InvalidateUICommand-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) ungültig wird. Das Invalidierungsereignis wird von der [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) behandelt und die Eigenschaft aktualisiert.

Die [**IUICommandHandler::UpdateProperty-Rückrufmethode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) wird nicht ausgeführt, und die Anwendung fragt einen aktualisierten Eigenschaftswert ab, bis die Eigenschaft vom Framework benötigt wird. Beispielsweise, wenn eine Registerkarte aktiviert und ein Steuerelement auf der Menübandbenutzeroberfläche angezeigt wird oder wenn eine QuickInfo angezeigt wird.

> [!Note]  
> In einigen Fällen kann eine Eigenschaft über die [**IUIFramework::GetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) abgerufen und mit der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) festgelegt werden.

 

In der folgenden Tabelle sind die Eigenschaftenschlüssel aufgeführt, die dem Spinner-Steuerelement zugeordnet sind.




| Eigenschaftsschlüssel | Hinweise | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a><blockquote>[!Note]<br />Wenn der dem Steuerelement zugeordnete Befehl durch einen Aufruf von <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>ungültig gemacht wird, fragt das Framework diese Eigenschaft ab, wenn als Wert von flags übergeben <code>UI_INVALIDATIONS_VALUE</code> <em>wird.</em></blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Unterstützt <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> und <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty.</strong></a> | 
| <a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Kann nur durch Ungültigkeit aktualisiert werden. | 




 

Im folgenden Codeabschnitt wird veranschaulicht, wie verschiedene Eigenschaften des Spinner-Steuerelements in der [**IUICommandHandler::UpdateProperty-Methode aktualisiert**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) werden.


```C++
//
//  FUNCTION:    UpdateProperty()
//
//  PURPOSE:    Called by the Ribbon framework when a command property needs 
//                to be updated.
//
//  COMMENTS:    This function is used to provide new command property values for 
//                the spinner when requested by the Ribbon framework.  
//    
STDMETHODIMP CCommandHandler::UpdateProperty(
    UINT nCmdID,
    REFPROPERTYKEY key,
    const PROPVARIANT* ppropvarCurrentValue,
    PROPVARIANT* ppropvarNewValue)
{
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;

    if (nCmdID == IDR_CMD_SPINNER_RESIZE)
    {
        // Set the minimum value
        if (IsEqualPropertyKey(key, UI_PKEY_MinValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(-10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the maximum value
        else if (IsEqualPropertyKey(key, UI_PKEY_MaxValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the increment
        else if (IsEqualPropertyKey(key, UI_PKEY_Increment))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(2.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the number of decimal places
        else if (IsEqualPropertyKey(key, UI_PKEY_DecimalPlaces))
        {
            hr = InitPropVariantFromUInt32(1, ppropvarNewValue);
            hr = S_OK;
        }

        // Set the format string
        else if (IsEqualPropertyKey(key, UI_PKEY_FormatString))
        {
            hr = InitPropVariantFromString(L"px", ppropvarNewValue);
            hr = S_OK;
        }

        // Set the representative string
        else if (IsEqualPropertyKey(key, UI_PKEY_RepresentativeString))
        {
            hr = InitPropVariantFromString(L"AAAAAAA", ppropvarNewValue);
            hr = S_OK;
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Hinweise

Wenn der Mindestwert ([ \_ UI PKEY \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) eines Spinners mit 0,0 initialisiert wird, sollte die Anwendung sicherstellen, dass alle nachfolgenden Werte, die vom Steuerelement bereitgestellt werden, nicht gleich -0,0 (negative Null) sind. Wenn der Spinner den Wert -0,0 liefert, sollte die Anwendung diesen Wert mithilfe der [**IUIFramework::SetUICommandProperty-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) auf 0,0 (positive Null) zurücksetzen, wie im folgenden Beispiel einer [**IUICommandHandler::Execute-Methode**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) für ein Spinner-Steuerelement gezeigt.

> [!Note]  
> Wenn dieser Test nicht ausgeführt wird und der Wert unkorrektiert bleibt, zeigt das Bearbeitungsfeld des Steuerelements die Zeichenfolge "Auto" an.

 


```C++
//
//  FUNCTION:    Execute()
//
//  PURPOSE:    Called by the Ribbon framework when a command is executed by the user.  
//                For this sample, when an increment or decrement button is pressed or
//                a new value is entered in the Spinner edit field.
//
STDMETHODIMP CCommandHandler::Execute(
      UINT nCmdID,
      UI_EXECUTIONVERB verb,
      const PROPERTYKEY* key,
      const PROPVARIANT* ppropvarValue,
      IUISimplePropertySet* pCommandExecutionProperties)
{
    UNREFERENCED_PARAMETER(pCommandExecutionProperties);

    HRESULT hr = E_NOTIMPL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        RenderParam param;
        g_renderer.GetRenderParam(&param);

        if (nCmdID == IDR_CMD_SPINNER_RESIZE)
        {
            // Spinner value is negative.
            if (!(ppropvarValue->decVal.sign == 0))
            {
                // Check if the value supplied by the Spinner is -0
                // and correct the value if necessary.
                // If this value is left uncorrected, the edit field 
                // of the control will display the string "Auto" when 
                // UI_PKEY_MinValue is set to 0.
                if (ppropvarValue->decVal.Lo64 == 0)
                {
                    // Initialize a new PROPVARIANT structure.
                    PROPVARIANT m_varNewVal;
                    PropVariantInit(&m_varNewVal);

                    // The replacement DECIMAL value.
                    DECIMAL m_dVal;
                    hr = VarDecFromI4(0, &m_dVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                    
                    // Initialize the new DECIMAL value.
                    UIInitPropertyFromDecimal(UI_PKEY_DecimalValue, m_dVal, &m_varNewVal);

                    // Set the UI_PKEY_DecimalValue to the new DECIMAL value.
                    hr = g_pFramework->SetUICommandProperty(nCmdID, UI_PKEY_DecimalValue, m_varNewVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                }
                // Decrease size of shape in document space.
                param.iShapeSizeIncrement = -ppropvarValue->intVal;
            }
            // Spinner value is positive.
            else
            {
                // Increase size of shape in document space.
                param.iShapeSizeIncrement = ppropvarValue->intVal;
            }
        }
        g_renderer.UpdateRenderParam(param);
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Menüband-Framework-Steuerelementbibliothek](windowsribbon-controls-entry.md)
</dt> <dt>

[**Spinner-Markupelement**](windowsribbon-element-spinner.md)
</dt> </dl>

